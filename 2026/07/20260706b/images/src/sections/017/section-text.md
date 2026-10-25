# セクション整理: 生成AI向け情報

## 主題

- 生成AIや AI agent が説明・実行時に混同しないための情報

## 明示すべき情報

- release tag and artifact
- conversion direction
- required `--out`
- sheet mode and heading depth
- string-cell policy
- Markdown-to-Excel mapping
- image handling rules
- merge marker semantics
- unsupported / limited scope
- raw `--help`
- Node.js / Java runtime differences
- Java parser caveat
- no summary option

## 図解

```text
曖昧な説明
  ↓
AI が option や仕様を発明しやすい
  ↓
version / direction / limits を固定
```

## 吹き出し案

AI に渡すときほど、方向と制約をはっきり書きます…！
