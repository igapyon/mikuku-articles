# 基本コマンド

- Node.js 版と Java 版の最小形
- `--out` が必須
- `--title` で presentation title を明示
- PPTX bytes を stdout に流す CLI として扱わない

```text
node miku-md2pptx-0.2.2.mjs input.md --out output.pptx

java -jar miku-md2pptx-java-0.2.3.jar input.md --out output.pptx
```

追加:

```text
--title "Project brief"
```

注意:

- relative path の基準が runtime によって違う
- AI agent には絶対 path が安全
