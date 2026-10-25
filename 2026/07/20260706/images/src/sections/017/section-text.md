# 017. 生成AI向け情報

## 主題

- 生成AIへ説明するときは、契約情報を明示する
- 散文だけでは過剰一般化しやすい

## 明示する情報

- release tag と artifact 名
- conversion direction
- Excel-to-Markdown mapping table
- output mode table
- table detection mode table
- formula resolution notes
- unsupported / limited scope
- raw `--help`
- Node.js と Java の違い
- recommended basic commands

## 効果

```text
曖昧な説明
  ↓
AI が勝手に一般化

契約情報つき説明
  ↓
version / scope / runtime を固定
```

## 吹き出し案

「生成AIには、version と scope をはっきり渡すのが大事です…」