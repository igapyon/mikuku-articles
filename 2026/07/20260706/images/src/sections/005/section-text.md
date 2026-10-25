# 005. 対応 runtime

## 主題

- Node.js 版と Java 版の v1.3.0 release を確認
- artifact と source をそろえて見る

## runtime 一覧

- Node.js CLI: `miku-xlsx2md-1.3.0.mjs`
- Node.js runtime bundle: `miku-xlsx2md-runtime-1.3.0.mjs`
- Node.js source archive
- Java CLI: `miku-xlsx2md-1.3.0.jar`
- Java source archive

## 関係

```text
Node.js 版
  単一 workbook 変換

Java 版
  単一 workbook 変換
  + directory batch conversion
```

## 重要ポイント

- 単一ファイル変換では基本引数がほぼ同じ
- Java 版には batch / directory 変換向け追加引数がある

## 吹き出し案

「同じ v1.3.0 でも、runtime ごとの役割を見分けます…」