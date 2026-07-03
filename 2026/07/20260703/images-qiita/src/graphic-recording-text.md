# グラレコ制作用整理テキスト

対象記事:

- `MS OfficeファイルをAI agent向けMarkdownに変換する Agent Skill を開発`
- `miku-ms-office-skills v0.6.1`
- installable skill: `igapyon-miku-ms-office`

## 1. 大テーマ

MS Office ファイルを、AI agent が読みやすい Markdown に変換する Agent Skills package。

キーワード:

- Office
- Markdown
- AI agent
- Agent Skills
- local CLI
- bundled runtime
- text-focused
- workflow adapter

## 2. 何をするもの？

```text
Word / Excel / PowerPoint
        ↓
  miku-soft converter
        ↓
 GitHub風 Markdown
        ↓
AI agent が読む・要約する・比較する
```

主目的:

- Office の見た目再現ではない
- AI agent が読むためのテキスト抽出
- GitHub風 Markdown へ寄せる
- 次の作業に渡しやすくする

## 3. 対応方向

Office-to-Markdown が主役。

| 入力 | converter | 出力 |
| --- | --- | --- |
| `.docx` | `miku-docx2md` | Markdown |
| `.xlsx` | `miku-xlsx2md` | Markdown |
| `.pptx` | `miku-pptx2md` | Markdown |

Markdown-to-Office もあるが experimental。

| 入力 | 出力 |
| --- | --- |
| Markdown | `.docx` |
| Markdown | `.xlsx` |
| Markdown | `.pptx` |

注意:

- `.md` だけでは出力形式が決まらない
- Word / Excel / PowerPoint のどれにするか明示が必要

## 4. 役割分担

`miku-ms-office-skills` は変換ロジック本体を持たない。

```text
miku-ms-office-skills
  = routing / runtime discovery / policy / bundle

upstream miku-soft converters
  = actual conversion behavior
```

役割表:

| 要素 | 役割 |
| --- | --- |
| Agent Skill | AI agent に手順と判断軸を渡す |
| tool routing | 入力と出力から converter を選ぶ |
| runtime policy | Node.js / Java の選び方を決める |
| bundled runtime | すぐ試せる実行 artifact |
| upstream converter | 実際の変換処理 |

## 5. 同梱 runtime

v0.6.1 では Node.js と Java の両方を同梱。

```text
Node.js .mjs
  miku-xlsx2md / miku-docx2md / miku-pptx2md
  miku-md2xlsx / miku-md2docx / miku-md2pptx

Java .jar
  miku-xlsx2md-java / miku-docx2md-java / miku-pptx2md-java
  miku-md2xlsx-java / miku-md2docx-java / miku-md2pptx-java
```

伝えたいこと:

- skill package としてセットでダウンロードしやすい
- Agent Skills として使い始めやすい
- 実行環境に合わせて Node.js / Java を選びやすい
- 通常変換はローカル CLI 実行で完結
- ネットワーク接続や LLM/API は不要

## 6. 通常変換の出力ポリシー

「変換して」と依頼されたら主出力だけ。

Office-to-Markdown なら Markdown だけ。

追加成果物は opt-in。

- summary
- debug
- assets
- zip
- diagnostics

図解:

```text
普通の依頼
  ↓
primary output only
  ↓
次に読むファイルが迷子にならない
```

## 7. うれしいこと

Markdown にすると AI agent との作業が始めやすい。

- 本文確認
- 要約
- 差分確認
- 関連メモ比較
- 不要部分の削除
- 後続 Agent Skills への入力

変換イメージ:

```text
人が見る完成物
  ↓
AI agent が読む作業資料
  ↓
次の作業へ進む入口
```

## 8. 向いていないこと

これはレイアウト再現ツールではない。

対象外:

- Office の見た目を忠実に再現
- 図形やチャートの完全変換
- OCR
- 複雑な帳票レイアウト再現
- Office ファイルの編集
- AI による文書解釈や書き換え

## 9. まとめの一枚絵

画面中央に大きな流れ:

```text
Office files
  ↓
converter routing
  ↓
local bundled runtime
  ↓
GitHub-flavored Markdown
  ↓
AI agent workflow
```

右側にみくく:

- 少し恥ずかしそうに説明
- 手には物を持たない
- 吹き出し: 「あ、あの…まず読める形にします…！」

図解ラベルは短く:

- Office
- Markdown
- local CLI
- no AI conversion
- primary output only
- Node.js / Java
- experimental reverse
- not layout faithful
