# 対応 runtime

- 確認対象 release tag を固定
- Node.js 版 v0.2.2
- Java 版 v0.2.3
- CLI 引数はほぼ同じ
- path 解決が大きな違い

```text
Node.js CLI
  miku-md2pptx-0.2.2.mjs
  relative path = runtime root 基準

Java CLI
  miku-md2pptx-java-0.2.3.jar
  relative path = current working directory 基準
```

注意:

- version を混ぜない
- parser/model の違いを説明する
- AI agent には実行場所と path を明示
