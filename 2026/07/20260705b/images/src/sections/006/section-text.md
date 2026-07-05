# ライセンス、ソースコード、実行環境

- OSS として公開
- Apache License 2.0
- release artifact と source を確認できる
- Node.js CLI には Node.js が必要
- Java CLI には Java が必要
- Java build from source には Maven が必要

local-first:

```text
Markdown file
  ↓ 手元の machine で処理
server upload しない
```

path の注意:

- Node.js: CLI artifact の calculated runtime root
- Java: current process working directory
- 絶対 path または明示的な配置関係が安全
