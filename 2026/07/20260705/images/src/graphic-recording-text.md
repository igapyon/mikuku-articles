# miku-pptx2md グラレコ制作用整理テキスト

## 1. 何の道具？

- PowerPoint `.pptx`
- Markdown `.md`
- AI agent が読みやすい形へ
- 見た目再現ではなく、読める構造化

```text
PowerPoint
  -> miku-pptx2md
  -> Markdown
  -> AI agent / 検索 / 要約
```

## 2. 中心メッセージ

- スライドを「読む入口」に変える
- スライド順、タイトル、本文、表、ノート、コメントを残す
- 変換できない見た目要素は diagnostics で見える化
- 完全再現より、次の作業へ渡しやすいテキスト

## 3. 役割分担

| 要素 | 役割 |
| --- | --- |
| `.pptx` | 元のプレゼン資料 |
| `miku-pptx2md` | 文字情報と構造を抽出 |
| Markdown | AI agent が読みやすい主出力 |
| summary / summary JSON | 変換結果の把握 |
| assets dir / manifest | 画像参照の管理 |
| diagnostics | 未対応要素の見える化 |

## 4. 対応するもの

- slide order
- slide title
- body text
- bullet / ordered list
- nested list
- bold / italic / underline
- table
- external hyperlink
- image reference
- speaker notes
- comments
- front matter

## 5. 対応しない、または限定対応

- exact layout
- z-order
- visual line wrapping
- theme typography / color
- animation / transition
- SmartArt / chart
- connector routing
- video / audio / OLE
- round-trip 復元

## 6. 使い方の流れ

```text
最小変換
  input.pptx --out output.md
必要に応じて
  + summary
  + summary JSON
  + assets-dir
  + debug
確認
  warnings / notes / images / diagnostics
```

## 7. Node.js と Java

- Node.js CLI
- Node.js runtime bundle
- Java CLI
- v0.5.1 では option set が同じ
- runtime は違っても CLI 契約はそろえる

## 8. 向いている用途

- PowerPoint 資料を AI agent に読ませる
- 会議資料や研修資料を検索しやすくする
- speaker notes も含めて文脈を読む
- warnings や assets の有無を確認する

## 9. 向いていない用途

- PowerPoint の完全な見た目再現
- 図形や矢印の意味の完全推論
- SmartArt / chart の完全変換
- `.pptx -> md -> pptx` の完全 round-trip

## 10. まとめ

- 目的は「PowerPoint を Markdown に置き換える」ではない
- 目的は「PowerPoint を読む入口を作る」
- 地味だけれど、AI agent へ渡す前の整え役

