# Exit code

- `--help` には exit code table は含まれない
- Java 版は source/docs で意味を確認
- Node.js と Java で少し違う

| runtime | exit code | 意味 |
| --- | --- | --- |
| Node.js | 0 | success / metadata |
| Node.js | 1 | usage / I/O / runtime error |
| Java | 0 | success / metadata |
| Java | 1 | I/O or conversion failure |
| Java | 2 | usage error |

図解:

```text
command
  ↓
success? -> 0
usage error? -> Node 1 / Java 2
I/O failure? -> 1
```

AI agent 向け注意:

- Java は usage error と conversion failure を分ける
