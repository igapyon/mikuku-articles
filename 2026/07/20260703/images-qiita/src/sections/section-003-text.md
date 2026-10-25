# 003 使い方

## 主題

AI agent に `igapyon-miku-ms-office` を使うよう依頼し、入力形式と出力形式から converter を選ばせる。

## 図解キーワード

- user request
- skill activation
- converter selection
- input extension
- explicit output target

## 図解したい流れ

```text
ユーザー依頼
  ↓
igapyon-miku-ms-office
  ↓
format check
  ↓
converter selection
```

## 注意点

- `.docx` / `.xlsx` / `.pptx` は Markdown 方向を選びやすい
- `.md` だけでは出力 Office 形式を決められない
- `.docx` / `.xlsx` / `.pptx` の明示が必要

## 吹き出し案

「.md だけでは、行き先を決められません…」
