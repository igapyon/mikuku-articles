# 006. ライセンス、ソースコード、実行環境

## 主題

- OSS として source / license / runtime 条件を確認できる
- release artifact と source tag をそろえる

## 確認するもの

- Apache License 2.0
- Node.js 版 source
- Java 版 source
- Node.js CLI の実行環境
- Java CLI の実行環境
- Java build from source は Maven

## 図解

```text
release artifact
  + source tag
  + license
  + runtime requirement
  ↓
説明の根拠が固定される
```

## 重要ポイント

- 実装時点を固定して説明できる
- 採用検討時に source と license を確認できる

## 吹き出し案

「artifact だけでなく、source と license も一緒に見ると安心です…」