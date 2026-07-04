# 013. 数式セルの見方

## 主題

- 数式セルはできるだけ値として扱う
- ただし Excel 数式の完全互換ではない

## Node.js 版の解決順

```text
cached value
  ↓
AST evaluator
  ↓
legacy resolver
  ↓
式文字列保持
```

## Java 版の扱い

- cached value を採用
- shared formula を展開
- 外部 workbook 参照は unsupported_external になる場合
- cached がない場合は fallback_formula / formula_text

## 読み方

- 値が出ていても再計算とは限らない
- source と status を見る
- fallback した数式は信頼の置き方を変える

## 吹き出し案

「値が出ていても、どこから来た値かを見るのが大事です…」