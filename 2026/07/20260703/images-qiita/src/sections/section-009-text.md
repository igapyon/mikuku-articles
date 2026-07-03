# 009 向いている使い方

## 主題

仕様メモ、一覧表、スライド内テキストなどを、まず Markdown にして AI agent と扱いやすくする。

## 図解キーワード

- Word memo
- Excel table
- PowerPoint text
- Markdown compare
- lightweight `.md`
- Node.js / Java backend

## ユースケース

| 元ファイル | 使い方 |
| --- | --- |
| Word | 仕様メモを読ませる |
| Excel | 一覧表を要約する |
| PowerPoint | スライド内テキストを取り出す |
| repository | Markdown と比較する |

## 図解したい感触

```text
コピー貼り直しの手間
  ↓
converter で入口を作る
  ↓
AI agent と作業開始
```

## 吹き出し案

「まず中身を読める形にします…」
