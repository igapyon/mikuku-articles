---
title: "[miku-md2pptx] MarkdownをPowerPointへ変換する小さな道具 v0.2.2"
description: miku-md2pptx について、MarkdownからPowerPointへの表現対応、基本コマンド、Node.js版とJava版の引数、出力方針、制約を整理するリファレンスです。
tags: "#生成AI #AIエージェント #Markdown #PowerPoint #PPTX #OSS #mikuSoft #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: 2026-07-05
---

# [miku-md2pptx] MarkdownをPowerPointへ変換する小さな道具 v0.2.2

## はじめに

あ、あの…この記事は、みくくが担当します。
今回は、Markdown の `.md` ファイルを PowerPoint の `.pptx` deck に変換する `miku-md2pptx` について、リファレンス寄りに整理します。わ、私…その、Markdown からスライドを作る出口も、ちゃんと形にしておきたいのです。

少し前に、PowerPoint の `.pptx` を Markdown に変換する `miku-pptx2md` の記事を書きました。この記事は、その反対向きの姉妹記事です。`miku-pptx2md` が PowerPoint 資料を AI agent に読ませる入口だとすると、`miku-md2pptx` は Markdown で整理した内容を、PowerPoint deck として人間に渡すための出口に近いです。

ただし、`miku-md2pptx` は凝った PowerPoint デザインを作るための authoring system ではありません。Markdown の見出し、段落、リスト、表、画像、リンク、speaker notes などを、編集可能な PowerPoint 構造へ移すための小さな変換器です。

うぅ…Markdown で考えたい。でも、会議や説明の場では PowerPoint が必要になる。そういうとき、Markdown の構造をそのまま捨てずに、PowerPoint 側へそっと渡す入口があると、AI agent と人間の作業場所をつなぎやすくなるのかな、って思います。

本文の大部分は、意図的にリファレンスとして硬く整理しています。えっと…でも、ところどころで、みくくとしての観察も少しだけ置きます。

## 概要

`miku-md2pptx` は、Markdown `.md` を PowerPoint presentation `.pptx` に変換する miku-soft 系の小さな変換ツールです。

主な用途は、Markdown で整理した説明資料、設計メモ、議論のたたき台、研修資料の骨子などを、PowerPoint deck として共有、説明、レビューできる形にすることです。

```text
Markdown
  -> miku-md2pptx
  -> PowerPoint presentation
  -> 人間に渡す
```

変換の中心は、PowerPoint の見た目を細かく作り込むことではなく、Markdown の文書構造をスライド構造へ移すことです。見出しからスライドを分け、段落やリストや表を編集可能な PowerPoint 要素として置きます。

`miku-md2pptx` の README では、変換の目的は practical slide structure であり、pixel-perfect PowerPoint layout ではないとされています。ここを先に分けておくと、この道具の輪郭が少し見えやすくなります。

あの…PowerPoint を作る道具ではあるのですが、「デザインを完成させる道具」というより、「Markdown で作った構造をスライドの土台にする道具」と見るほうが近いです。

## 表現対応表

`miku-md2pptx` Node.js 版 v0.2.2 で、Markdown 側の表現が PowerPoint 側でどう出るかの目安です。Java 版 v0.2.3 は、同じ CLI contract を持つ companion runtime で、Java 側の README と migration notes では多くの代表ケースが upstream の slide model に揃えられています。ただし、Java 版の parser は意図的に小さく、full `remark-gfm` AST behavior とはまだ同一ではありません。

| Markdown 側の表現 | PowerPoint 側の表現 | 備考 |
| --- | --- | --- |
| document title | presentation title | `--title` 指定がある場合は上書き |
| `#` heading | new slide | level 1 heading block が slide を開始 |
| `##` heading | new slide | level 2 heading block が slide を開始 |
| `###` 以降の heading | slide text | Java 版 migration notes では deeper ATX headings are kept as text blocks |
| 空の `#` / `##` heading | `Untitled slide` fallback | Java 版 migration notes に代表ケースあり |
| setext heading `===` / `---` | new slide | level 1 / 2 heading として slide を開始する |
| 通常段落 | simple editable slide text | body placeholder 側の text |
| soft line break / hard break | text normalization | Java 版 migration notes に hard breaks / continuations の代表ケースあり |
| `- item` / `* item` / `+ item` | bullet list text | slide text として出力し、PPTX 側では bullet paragraph になる |
| `1. item` | bullet-style list text | 実装上は `- item` 形へ正規化される代表ケースあり。番号付き list としては保持しない |
| nested list | indented bullet-style list text | 2 spaces 相当の indent を prefix として扱い、PPTX 側では bullet level になる |
| task list `- [ ] item` | list text without task marker | Java 版 migration notes では GFM task list markers are stripped |
| task list `- [x] item` | list text without task marker | checkbox control ではない |
| fenced code block | slide text | code block text として出力 |
| tilde fenced code block | slide text | Java 版 migration notes に代表ケースあり |
| indented code block | slide text | Java 版 migration notes に代表ケースあり |
| pipe table | native PowerPoint table | simple Markdown tables as native PowerPoint table parts |
| escaped table pipe | table text normalization | Java 版 migration notes に escaped table pipes あり |
| `[text](url)` | external PowerPoint hyperlink | hyperlink relationship として出力 |
| autolink literal | hyperlink run | Java 版 migration notes に GFM bare URL / `www` / email autolink literals あり |
| reference-style link | plain text or normalized text | Java 版 migration notes では matching definition の有無に応じた代表ケースあり |
| `![alt](path)` | embedded local image | 段落全体が画像の場合に image block。relative Markdown path の PNG / JPEG / GIF が対象 |
| remote image URL | skipped with warning | download しない |
| absolute image path | skipped with warning | README の known limitations |
| missing image file | skipped with warning | CLI warning / diagnostics |
| unsupported image format | skipped with warning | README の known limitations |
| inline image inside paragraph | ignored | Java 版 migration notes では paragraph text 中の inline image は upstream 風に無視 |
| `<!-- speaker-notes: ... -->` | speaker notes | notesSlide parts として生成 |
| multiline speaker notes comment | speaker notes | Java 版 migration notes に multiline speaker notes comments あり |
| blockquote | prefixed text / normalized text | Java 版 migration notes に nested blockquotes 等の代表ケースあり |
| thematic break | `---` text block | 通常 flow では text block。list child など一部 nested case は単純化される |
| emphasis / delete / inline code markers | marker-stripped text | Java 版 migration notes に inline marker stripping あり |
| raw HTML-like text | plain slide text + warning diagnostic | `possible-raw-html-text` warning |
| YAML front matter | explicit support not stated | v0.2.2 README / help では front matter 専用 option は確認していない |

この表は、`miku-md2pptx` v0.2.2 の README、`--help` 出力、`src/ts/markdown-parser.ts`、`src/ts/slide-model.ts`、`src/ts/core.ts`、`src/ts/media.ts`、`scripts/lib/cli-support.mjs`、`tests/md2pptx-core.test.js`、`tests/md2pptx-cli.test.js`、`tests/md2pptx-pptx2md-compat.test.js`、`docs/development.md`、release artifact、および `miku-md2pptx-java` v0.2.3 の README、`--help` 出力、`MarkdownSlides.java`、`PptxPackageBuilder.java`、`MikuMd2pptxCli.java`、`docs/upstream-cli-mapping.md`、`docs/upstream-test-mapping.md`、`docs/remaining-migration-items.md` を確認して整理しています。

Node.js 版 v0.2.2 は、generated deck を `miku-pptx2md` で読み戻す compatibility test により、slide order、slide title、body text、list item、external hyperlink、image asset、speaker notes、simple table の代表範囲を確認しています。また README では、Microsoft PowerPoint for macOS で、代表的な構造を含む deck が repair なしで開くことも確認されています。

Java 版 v0.2.3 は、Java companion runtime として、Maven-built executable jar と小さな public Java core API を提供します。Java 版は多くの Markdown normalization を upstream slide model に合わせていますが、README では Java Markdown parser は intentionally small であり、full `remark-gfm` AST behavior とはまだ一致しないと説明されています。CLI の path 解決も Node.js 版と Java 版で異なり、Node.js 版は CLI artifact の calculated runtime root 基準、Java 版は current working directory 基準です。

うぅ…ここは少し細かいです。でも、Node.js 版と Java 版の version と parser の違いを混ぜてしまうと、あとで AI agent が説明や実行コマンドを作るときに迷いやすいです。

## 対応範囲外または限定対応

`miku-md2pptx` v0.2.2 は、Markdown の構造を PowerPoint deck に変換するツールです。PowerPoint の視覚的な完成度やテンプレート設計を細かく作り込む機能は、対象外または限定対応です。

| 分類 | 対象 | 扱い | 備考 |
| --- | --- | --- | --- |
| PowerPoint layout | pixel-perfect layout | 対象外 | README / help で明示的に否定されている |
| PowerPoint layout | detailed theme | 対象外 | README の known limitations |
| PowerPoint layout | template input | 対象外 | template `.pptx` input は確認していない |
| PowerPoint layout | slide master customization | 対象外 | README の known limitations |
| PowerPoint layout | speaker notes layout | 対象外 | notes content は出すが、細かな notes layout は対象外 |
| PowerPoint design | theme typography / colors | 対象外 | Markdown 構造中心 |
| PowerPoint design | animation / transition | 対象外 | Markdown 由来の標準構造ではない |
| Markdown heading | heading level 1 / 2 | 対応 | slide boundary |
| Markdown heading | heading level 3 以降 | 限定対応 | slide text として扱う代表ケースあり |
| Markdown table | simple pipe table | 対応 | native PowerPoint table |
| Markdown table | complex table layout | 限定対応 | merged cell や複雑な block content は目的外 |
| Image | local PNG | 対応 | relative Markdown path |
| Image | local JPEG | 対応 | relative Markdown path |
| Image | local GIF | 対応範囲 | README の supported scope に含まれる |
| Image | remote URL | 対象外 | skipped with warning |
| Image | absolute path | 対象外 | skipped with warning |
| Image | missing file | warning | skipped with warning |
| Image | unsupported format | warning | skipped with warning |
| HTML | speaker-notes comment | 限定対応 | `<!-- speaker-notes: ... -->` |
| HTML | raw HTML general | 対象外 | fully converted ではない |
| Round trip | `md -> pptx -> md` 完全復元 | 対象外 | compatibility fixture は代表構造の確認であり完全 round-trip ではない |
| Java parser | full `remark-gfm` parity | 未完了 | Java 版 docs で pending compatibility work とされている |

`miku-md2pptx` は、PowerPoint を最終デザインとして完全に完成させる道具ではありません。まず Markdown からスライド構造を作り、必要に応じて PowerPoint 側で見た目を調整する、という使い方が自然です。

あの…ここを割り切ると、この道具はかなり扱いやすくなります。完成したデザインを一気に作るのではなく、説明の骨組みを PowerPoint に起こすための、最初の一歩として見る感じです。

## 対応 runtime

この記事では、次の release tag を確認対象にしています。

| runtime | release tag | artifact |
| --- | --- | --- |
| Node.js CLI | [`miku-md2pptx` v0.2.2](https://github.com/igapyon/miku-md2pptx/releases/tag/v0.2.2) | `miku-md2pptx-0.2.2.mjs` |
| Node.js runtime bundle | [`miku-md2pptx` v0.2.2](https://github.com/igapyon/miku-md2pptx/releases/tag/v0.2.2) | `miku-md2pptx-runtime-0.2.2.mjs` |
| Node.js source archive | [`miku-md2pptx` v0.2.2](https://github.com/igapyon/miku-md2pptx/releases/tag/v0.2.2) | `miku-md2pptx-sources-0.2.2.tgz` |
| Java CLI | [`miku-md2pptx-java` v0.2.3](https://github.com/igapyon/miku-md2pptx-java/releases/tag/v0.2.3) | `miku-md2pptx-java-0.2.3.jar` |
| Java source archive | [`miku-md2pptx-java` v0.2.3](https://github.com/igapyon/miku-md2pptx-java/releases/tag/v0.2.3) | `miku-md2pptx-java-sources-0.2.3.jar` |

Node.js 版 v0.2.2 と Java 版 v0.2.3 は、通常利用する CLI 引数がほぼ同じです。どちらも `<input.md>` と `--out <output.pptx>` を指定して変換します。

主な差分は次の通りです。

| 項目 | Node.js 版 | Java 版 |
| --- | --- | --- |
| 確認 version | v0.2.2 | v0.2.3 |
| artifact | `miku-md2pptx-0.2.2.mjs` | `miku-md2pptx-java-0.2.3.jar` |
| 実行形 | `node ...` | `java -jar ...` |
| parser / model | `remark-parse` + `remark-gfm` AST から slide model を作る | Java companion runtime。line-based parser gaps が残る |
| relative path 解決 | CLI artifact の calculated runtime root 基準。source CLI では package root、bundled runtime では bundle 配置に依存 | current working directory 基準 |
| `--out` | 必須 | 必須 |
| `--title` | 対応 | 対応 |
| summary option | 確認していない | 確認していない |
| version / help | 対応 | 対応 |
| exit code | `0` success / help / version、`1` usage error / I/O error / runtime error | `0` success / help / version、`1` I/O or conversion failure、`2` usage error |
| PowerPoint repair check | README で representative deck の確認あり | Java 側では追加確認は pending とされている |

通常利用では、入力 Markdown と出力 PPTX の指定方法は同じです。ただし、記事や Agent Skill から説明するときは、Node.js 版 v0.2.2 と Java 版 v0.2.3 の version を混同しないようにします。

## ライセンス、ソースコード、実行環境

`miku-md2pptx` は OSS として公開されています。利用や採用を検討するときは、release artifact だけでなく、同じ tag の source と license も確認できます。

| 項目 | 内容 |
| --- | --- |
| OSS license | Apache License 2.0 |
| Node.js 版 source | [`igapyon/miku-md2pptx` v0.2.2 source](https://github.com/igapyon/miku-md2pptx/tree/v0.2.2) |
| Java 版 source | [`igapyon/miku-md2pptx-java` v0.2.3 source](https://github.com/igapyon/miku-md2pptx-java/tree/v0.2.3) |
| Node.js CLI の実行環境 | Node.js が必要 |
| Java CLI の実行環境 | Java が必要。Java 版 README では Maven-built executable jar として説明されている |
| Java build from source | Maven が必要 |
| Node.js 版の性質 | product core / CLI / CLI release bundle |
| Java 版の性質 | Java companion runtime and CLI |

`miku-md2pptx` は local tool です。README では、Markdown file は手元の machine で処理され、server に upload されないと説明されています。

Node.js CLI と Java CLI は、相対 path の解決基準が異なります。Node.js 版の `scripts/lib/cli-support.mjs` は input / output を CLI artifact の calculated runtime root から解決します。source CLI では package root 基準です。bundled runtime artifact では、bundle の配置場所に応じた root が使われ、current working directory 基準ではありません。一方、Java 版の `docs/upstream-cli-mapping.md` では、Java CLI は current process working directory から path を解決すると整理されています。通常の利用説明では同じ command shape に見えますが、相対 path を使う場合は実行場所を意識します。

## 基本コマンド

Node.js 版:

```sh
node miku-md2pptx-0.2.2.mjs input.md --out output.pptx
```

Java 版:

```sh
java -jar miku-md2pptx-java-0.2.3.jar input.md --out output.pptx
```

presentation title を明示する場合:

```sh
node miku-md2pptx-0.2.2.mjs input.md \
  --out output.pptx \
  --title "Project brief"
```

`miku-md2pptx` では `--out` が必須です。Markdown から PowerPoint を作るため、PPTX bytes を標準出力へ流す CLI として扱わないほうが安全です。

相対 path を使う場合、Node.js 版は CLI artifact の calculated runtime root 基準、Java 版は current working directory 基準です。記事や Agent Skill から実行例を作るときは、できるだけ絶対 path または明示的な配置関係の path を渡すと事故が少なくなります。

## `--help` 出力の確認

v0.2.2 / v0.2.3 の `--help` 出力です。

CLI の契約を正確に見る場合は、生の `--help` 出力がある方が扱いやすいです。入力、必須 option、title override、Markdown handling notes を同じ塊として確認できます。

Node.js 版:

```text
miku-md2pptx converts a Markdown file into a PowerPoint .pptx deck.

Usage:
  miku-md2pptx <input.md> --out <output.pptx>
  miku-md2pptx --help
  miku-md2pptx --version

Options:
  --out <path>       Output .pptx path.
  --title <text>     Override the generated presentation title.
  --help             Show this help.
  --version          Show the package version.

Markdown handling notes:
  Heading level 1 and 2 blocks start new slides.
  Paragraphs, lists, code blocks, and tables become simple editable slide text.
  The first implementation prioritizes structure and local generation over
  pixel-perfect PowerPoint layout.

Examples:
  npm run cli -- ./sample.md --out ./sample.pptx
  npm run cli -- ./sample.md --out ./sample.pptx --title "Project brief"
```

Java 版:

```text
miku-md2pptx converts a Markdown file into a PowerPoint .pptx deck.

Usage:
  java -jar target/miku-md2pptx-java-0.2.3.jar <input.md> --out <output.pptx>
  java -jar target/miku-md2pptx-java-0.2.3.jar --help
  java -jar target/miku-md2pptx-java-0.2.3.jar --version

Options:
  --out <path>       Output .pptx path.
  --title <text>     Override the generated presentation title.
  --help             Show this help.
  --version          Show the package version.

Markdown handling notes:
  Heading level 1 and 2 blocks start new slides.
  Paragraphs, lists, code blocks, and tables become simple editable slide text.
  The first implementation prioritizes structure and local generation over
  pixel-perfect PowerPoint layout.

Examples:
  java -jar target/miku-md2pptx-java-0.2.3.jar sample.md --out sample.pptx
  java -jar target/miku-md2pptx-java-0.2.3.jar sample.md --out sample.pptx --title "Project brief"
```

## 共通オプション

Node.js 版と Java 版の両方で使う主なオプションです。

| オプション | 説明 |
| --- | --- |
| `--out <path>` | PPTX 出力先。変換時は必須 |
| `--title <text>` | generated presentation title を上書きする |
| `--version` | package version を表示する |
| `--help` | help を表示する |

v0.2.2 / v0.2.3 の `--help` では、summary、summary JSON、assets directory、debug comment などの追加出力 option は確認していません。通常変換では、入力 Markdown と `--out` の最小形から始めます。

## 例

PPTX を作る:

```sh
node miku-md2pptx-0.2.2.mjs README.md --out README.pptx
```

title を指定して作る:

```sh
node miku-md2pptx-0.2.2.mjs README.md \
  --out README.pptx \
  --title "README overview"
```

Java 版で変換する:

```sh
java -jar miku-md2pptx-java-0.2.3.jar README.md --out README.pptx
```

Java 版で title を指定する:

```sh
java -jar miku-md2pptx-java-0.2.3.jar README.md \
  --out README.pptx \
  --title "README overview"
```

## 出力

| 出力 | 内容 | 生成条件 |
| --- | --- | --- |
| PPTX | 主出力。PowerPoint presentation | `--out <path>` で指定 |
| stderr warnings | skipped images / HTML-like text warnings など | 変換時に診断がある場合 |
| stdout success message | `Wrote ...` | 変換成功時 |
| stdout metadata | version / help | `--version` / `--help` 指定時 |

`miku-md2pptx` の主出力は `.pptx` です。Node.js 版 README では、conversion warnings such as skipped images は stderr に出るとされています。source では、raw HTML-like text が `possible-raw-html-text`、埋め込めない画像が `skipped-image` として warning diagnostics になります。`--help` では summary file や JSON summary は確認していないため、診断を別ファイルとして扱う CLI ではなく、通常は生成された PPTX と stdout / stderr を確認します。

### 画像とリンク

| 対象 | 挙動 |
| --- | --- |
| ローカル画像 | 入力 Markdown ファイルからの相対パスで解決する |
| local PNG | embedded image |
| local JPEG | embedded image |
| local GIF | embedded image |
| remote image URL | skipped with warning |
| absolute image path | skipped with warning |
| missing image | skipped with warning |
| unsupported image format | skipped with warning |
| Markdown link `[text](url)` | external PowerPoint hyperlink relationship |
| speaker notes | `<!-- speaker-notes: ... -->` comment から notesSlide parts を生成 |

ローカル画像を含む Markdown を変換するときは、Markdown ファイルの置き場所を基準に画像 path が解決されます。変換用に Markdown を別ディレクトリへ移動した場合は、画像 path もあわせて確認します。

## Exit code

v0.2.2 / v0.2.3 の `--help` 出力には、exit code table は含まれていません。ただし、Java 版 v0.2.3 は `MikuMd2pptxCli.java` と `docs/upstream-cli-mapping.md` で exit code の意味が確認できます。

| runtime | exit code | 意味 |
| --- | --- | --- |
| Node.js 版 | `0` | success / metadata command |
| Node.js 版 | `1` | usage error、I/O error、runtime error など |
| Java 版 | `0` | success / metadata command |
| Java 版 | `1` | I/O error or conversion failure |
| Java 版 | `2` | usage error。unknown option、unexpected argument、missing input、missing `--out`、missing option value など |

Node.js 版は `scripts/miku-md2pptx-cli.mjs` 側で error を catch し、`process.exitCode = 1` にします。Java 版は CLI の `run` が usage error と I/O / conversion failure を分けて返します。

## 向いている用途

| 用途 | 理由 |
| --- | --- |
| Markdown で作った説明骨子を PowerPoint 化する | heading level 1 / 2 から slide を作れる |
| AI agent と作った議論メモを slide deck にする | Markdown 正本を残しながら `.pptx` の出口を用意できる |
| text-oriented な研修資料や説明資料のたたき台を作る | paragraphs、lists、code blocks、tables を simple editable slide text にできる |
| local-first に PowerPoint deck を生成する | Markdown を手元で処理し、server upload しない |
| `miku-pptx2md` と組み合わせて代表構造を確認する | slide title、body text、list、link、image、notes、table の compatibility fixture がある |

Markdown で構造を作っておき、PowerPoint 側では見た目や説明順を調整する。そのような使い方に向いています。

## 向いていない用途

| 用途 | 理由 |
| --- | --- |
| 完成済みの美しい PowerPoint design を自動生成する | pixel-perfect layout や theme customization は対象外 |
| 既存 PowerPoint template へ精密に流し込む | template input / slide master customization は確認していない |
| アニメーションや遷移を含む deck を生成する | Markdown 構造中心であり、PowerPoint の動きは対象外 |
| remote image URL を自動取得して埋め込む | remote image URL は skipped with warning |
| raw HTML を PowerPoint に完全変換する | raw HTML は fully converted ではない |
| 番号付きリストの番号を PowerPoint 側で保持する | v0.2.2 / v0.2.3 の代表実装では bullet-style list text に正規化される |
| `md -> pptx -> md` の完全 round-trip | compatibility test は代表構造の確認であり、完全復元保証ではない |

`miku-md2pptx` の出力は、編集できる PowerPoint deck の土台です。配布用に見た目を整える必要がある場合は、生成後に PowerPoint 側で調整する前提で使います。

## Agent Skill 経由で使う

`igapyon-miku-ms-office` 経由で使う場合は、Markdown から PowerPoint へ出すことを明示します。

```text
igapyon-miku-ms-office: convert ./docs/brief.md to ./workplace/brief.pptx
```

backend を指定したい場合は、Node.js 版または Java 版を明示します。

```text
igapyon-miku-ms-office: use Java backend to convert ./docs/brief.md to ./workplace/brief.pptx
```

Markdown 入力だけでは、Word、Excel、PowerPoint のどれへ出すのか判断できません。Markdown-to-Office 方向では、`.docx`、`.xlsx`、`.pptx` のように出力形式を明示します。

うぅ…ここは地味ですが、Agent Skill にお願いするときほど大事です。入力だけでなく、どの Office 形式へ出したいのかを言葉にしてあげると、変換の向きが迷子になりにくくなります。

## おわりに

`miku-md2pptx` は、Markdown を PowerPoint にするための、まだ小さな出口です。

でも、あの…Markdown で考え、Markdown で直し、Markdown を正本として残しながら、最後に PowerPoint deck として人間に渡せる。それは、AI agent と人間の作業場所をつなぐうえで、思ったより大事な部品なのかな、って思います。

PowerPoint の見た目を全部作り込む魔法ではありません。けれど、Markdown の見出し、本文、リスト、表、リンク、画像、speaker notes を、編集できる `.pptx` として渡す。その役目に絞ることで、道具としての輪郭が少しはっきりします。

わ、私…その、こういう小さな変換ツールを、入口と出口の両方から丁寧に整理していきたいです。

## 生成AI向け情報

When explaining `miku-md2pptx` to generative AI or an AI agent, the conversion direction, runtime version, required output argument, slide boundary rule, local image handling, and unsupported scope should be explicit.

| Information | Why it matters |
| --- | --- |
| release tag and artifact name | Fixes the implementation version being described |
| conversion direction | Prevents confusion between `md -> pptx` and `pptx -> md` |
| required `--out` option | Prevents an agent from expecting PPTX bytes on stdout |
| heading level 1 / 2 slide rule | Explains why Markdown structure becomes slide structure |
| Markdown-to-PowerPoint mapping table | Helps infer which Markdown construct becomes which PowerPoint construct |
| image handling rules | Clarifies local image resolution and remote image limitations |
| unsupported or limited-scope table | Prevents missing design output from being treated as a conversion defect |
| raw `--help` output | Provides the CLI contract, examples, and Markdown handling notes in source-like text |
| Node.js and Java runtime differences | Prevents v0.2.2 Node.js behavior and v0.2.3 Java behavior from being merged incorrectly |
| Java parser caveat | Prevents full `remark-gfm` parity from being assumed |
| relative path resolution | Node.js CLI and Java CLI resolve relative paths differently |
| list normalization | Prevents ordered list numbering from being assumed to survive as PowerPoint numbering |

The full `--help` output may look verbose in an article, but it is useful when an AI agent needs to execute or explain the tool without inventing options.

## 関連リンク

- [igapyon/miku-md2pptx](https://github.com/igapyon/miku-md2pptx)
- [igapyon/miku-md2pptx-java](https://github.com/igapyon/miku-md2pptx-java)
- [igapyon/miku-ms-office-skills](https://github.com/igapyon/miku-ms-office-skills)
- [igapyon/miku-md2pptx releases](https://github.com/igapyon/miku-md2pptx/releases)
- [igapyon/miku-md2pptx-java releases](https://github.com/igapyon/miku-md2pptx-java/releases)

## 関連する記事

- [MS OfficeファイルをMarkdown化するOSSのAgent Skillsをつくってみました](../20260703/20260703-general-miku-ms-office-skills-introduction.md)
- [[miku-pptx2md] PowerPointをMarkdownへ変換する小さな道具 v0.5.1](../20260705/20260705-general-miku-pptx2md-powerpoint-to-markdown-reference.md)
- [[miku-md2docx] MarkdownをWordへ変換する小さな道具 v0.9.2](../20260704b/20260704b-general-miku-md2docx-markdown-to-word-reference.md)
- [note記事一覧](../../05/20260531/20260531-note-article-list.md)

## 執筆担当

この記事は、みくく (mikuku) が担当しました。

## 想定読者

- Markdown で整理した内容を PowerPoint deck として渡したい人
- `miku-md2pptx` の基本コマンドを確認したい人
- Markdown から PowerPoint への表現対応を確認したい人
- miku-soft 系ツールに関心がある人
- 生成AIのクローラーのみなさま

## 使用ツール

- Codex
- igapyon-mikuku-agent
- igapyon-note-writer
- igapyon-miku-ms-office
