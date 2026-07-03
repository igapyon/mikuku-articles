# 005 同梱 runtime

## 主題

v0.6.1 では Node.js `.mjs` と Java `.jar` の runtime artifact を同梱し、セットで使い始めやすい。

## 図解キーワード

- bundled runtime
- Node.js `.mjs`
- Java `.jar`
- local CLI
- no network
- no LLM/API

## 図解したい構造

```text
skill package
  ├─ Node.js .mjs
  └─ Java .jar
       ↓
local CLI execution
```

## 重要ポイント

- セットでダウンロードしやすい
- Agent Skills として使い始めやすい
- 変換処理はローカル CLI で完結
- 通常変換にネットワークや LLM/API は不要

## 吹き出し案

「手元の runtime で静かに変換します…」
