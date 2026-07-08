# セクション006 グラレコ制作用整理テキスト

## 主題

- `miku-md2docx` のテンプレート適用
- Word の構造や見た目を借りる
- 本文は Markdown 生成内容に置き換える

## 図解

```text
template.docx
  ├─ styles
  ├─ theme assets
  └─ section settings

sample.md
  ↓
生成本文
  ↓
output.docx
```

## 注意

- 既存本文へ差し込む機能ではない
- template の body content はコピーしない
- structural / best-effort

## 画像内ラベル

- 「土台を借りる」
- 「本文は生成内容へ」
