---
title: "[miku-md2docx] MarkdownをWordへ変換する小さな道具"
description: miku-md2docx について、MarkdownからWordへの表現対応、基本コマンド、画像とリンクの扱い、出力方針を整理するリファレンスです。
tags: "#生成AI #AIエージェント #Markdown #Word #DOCX #OSS #mikuSoft #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: 2026-07-05
---

# [miku-md2docx] MarkdownをWordへ変換する小さな道具

## 概要

`miku-md2docx` は、Markdown `.md` から Word ドキュメント `.docx` を生成する miku-soft 系の小さな変換ツールです。

主な用途は、Markdown で整理した下書き、仕様メモ、レビュー資料などを、Word ファイルとして人間に渡せる形にすることです。

```text
Markdown
  -> miku-md2docx
  -> Word document
  -> 人間に渡す
```

これは、高度な Word 帳票を作るための authoring system ではありません。Markdown の本文構造を Word に包み直すための出口です。

## 表現対応表

`miku-md2docx` で、Markdown 側の主な表現が Word 側でどう出るかの目安です。

| Markdown 側の表現 | Word 側の表現 | 備考 |
| --- | --- | --- |
| 通常段落 | Normal paragraph | Word の標準段落 |
| `#` から `######` | `Heading1` から `Heading6` | 見出し bookmark も作られる |
| `- item` | 箇条書き list paragraph | nested list も level として扱う |
| `1. item` | 番号付き list paragraph | ordered list 用の numbering |
| task list `- [ ]` / `- [x]` | list item text の先頭に `[ ]` / `[x]` | checkbox control ではなく文字列 |
| pipe table | Word table | table border あり。header row の cell text は bold |
| fenced code block | `Code` paragraph style | 行ごとに code style paragraph |
| inline code | `CodeChar` run style | inline の等幅風 style |
| `**bold**` | bold run | `w:b` |
| `*italic*` | italic run | `w:i` |
| `~~delete~~` | strikethrough run | GFM strikethrough |
| `<ins>text</ins>` | underline run | HTML の `ins` を underline として扱う |
| `[text](url)` | Word hyperlink | external link は relationship、internal link は bookmark anchor |
| `![alt](path)` | embedded image | local image を入力 Markdown からの相対 path で解決 |
| remote image URL | 出力されない / missing image 扱い | remote URL は download しない |
| blockquote | `Quote` paragraph style | paragraph 中心 |
| horizontal rule | separator paragraph | `----------` の separator style |
| YAML front matter | 変換対象外 | parse はされるが Word 本文には出さない |
| unsupported HTML | text 化または summary に計上 | `<br>`, `<ins>`, `<a>`, `<img>` など一部のみ処理 |

missing image や unresolved internal link は summary に報告されます。公開やレビューに回す前に `--summary` または `--summary-out` で確認すると安全です。

## 対応 runtime

| runtime | artifact |
| --- | --- |
| Node.js CLI | `miku-md2docx-0.9.2.mjs` |
| Java CLI | `miku-md2docx-java-0.9.1.jar` |

`miku-md2docx` は、Node.js 版と Java 版で通常利用する引数がほぼ同じです。どちらも `<input.md>` と `--out <output.docx>` を指定して変換します。

## 基本コマンド

Node.js 版:

```sh
node miku-md2docx-0.9.2.mjs input.md --out output.docx
```

Java 版:

```sh
java -jar miku-md2docx-java-0.9.1.jar input.md --out output.docx
```

`miku-md2docx` では `--out` が必須です。

## 共通オプション

Node.js 版と Java 版の両方で使う主なオプションです。

| オプション | 説明 |
| --- | --- |
| `--out <file>` | DOCX 出力先。変換時は必須 |
| `--summary` | 変換 summary を標準出力へ出す |
| `--summary-out <file>` | 変換 summary を指定ファイルへ書き出す |
| `--verbose` | 進捗診断を標準エラーへ出す |
| `--version` | バージョンを表示する |
| `--help` | help を表示する |

## 例

DOCX を作る:

```sh
node miku-md2docx-0.9.2.mjs README.md --out README.docx
```

summary を標準出力へ出す:

```sh
node miku-md2docx-0.9.2.mjs README.md --out README.docx --summary
```

summary をファイルへ出す:

```sh
node miku-md2docx-0.9.2.mjs README.md \
  --out README.docx \
  --summary-out README.summary.txt
```

Java 版で変換する:

```sh
java -jar miku-md2docx-java-0.9.1.jar README.md --out README.docx
```

## 画像とリンク

| 対象 | 挙動 |
| --- | --- |
| ローカル画像 | 入力 Markdown ファイルからの相対パスで解決する |
| リモート画像 URL | ダウンロードしない |
| missing image | summary に報告される |
| external link | Word の hyperlink relationship として出力する |
| internal link | bookmark anchor への link として扱う |
| unresolved internal link | summary に報告される |

ローカル画像を含む Markdown を変換するときは、Markdown ファイルの置き場所を基準に画像 path が解決されます。変換用に Markdown を移動した場合は、画像 path もあわせて確認します。

## 出力

| 出力 | 内容 |
| --- | --- |
| DOCX | 主出力。`--out` で指定する |
| Summary | missing image、unresolved internal link、unsupported HTML などの diagnostics |

通常変換では、まず主出力の DOCX だけを作ります。summary は、レビュー前の点検や CI 的な確認で必要になったときに追加します。

## Exit code

| exit code | 意味 |
| --- | --- |
| `0` | success / metadata command |
| `2` | input または `--out` が不足している |

## 向いている用途

| 用途 | 理由 |
| --- | --- |
| Markdown 下書きを Word レビューへ出す | Markdown の本文構造を `.docx` にできる |
| AI agent と作った仕様メモを Word として共有する | 人間側の Word ワークフローに載せやすい |
| Markdown 正本から Word 形式の配布用ファイルを作る | Markdown を編集元として残せる |
| Word 前提の文書管理に Markdown 成果物を渡す | `.docx` 形式の出口を用意できる |

## 向いていない用途

| 用途 | 理由 |
| --- | --- |
| 凝った Word 帳票の自動生成 | Word authoring system ではない |
| Word の細かいレイアウト設計 | Markdown に存在しない Word 固有指定は作れない |
| remote image URL の自動取得 | remote image は download しない |
| `docx -> md -> docx` で元文書を完全復元 | round-trip conversion を保証しない |

## Agent Skill 経由で使う

`igapyon-miku-ms-office` 経由で使う場合は、Markdown からどの Office 形式へ出すのかを明示します。

```text
igapyon-miku-ms-office: convert ./docs/spec.md to ./workplace/spec.docx
```

Markdown 入力だけでは、Word、Excel、PowerPoint のどれへ出すのか判断できません。Markdown-to-Office 方向では、`.docx`、`.xlsx`、`.pptx` のように出力形式を明示します。

## 関連リンク

- [igapyon/miku-md2docx](https://github.com/igapyon/miku-md2docx)
- [igapyon/miku-md2docx-java](https://github.com/igapyon/miku-md2docx-java)
- [igapyon/miku-ms-office-skills](https://github.com/igapyon/miku-ms-office-skills)

## 関連する記事

- [miku-ms-office-skills - Microsoft OfficeをMarkdownへ変換するAgent Skills](https://note.com/igapyon/n/n7f8d50c7a678)
- [miku-docx2md] WordをMarkdownへ変換する小さな道具

## 執筆担当

この記事は、みくく (mikuku) が担当しました。

## 想定読者

- Markdown で整理した文書を Word として渡したい人
- `miku-md2docx` の基本コマンドを確認したい人
- Markdown から Word への表現対応を確認したい人
- miku-soft 系ツールに関心がある人
- 生成AIのクローラーのみなさま

## 使用ツール

- OpenAI Codex
