# 対応 runtime

- 確認対象は 2 runtime

| runtime | version | 実行形 |
| --- | --- | --- |
| Node.js CLI | v0.9.2 | `node ...` |
| Java CLI | v0.9.1 | `java -jar ...` |

- CLI 引数はほぼ同じ
- parser は違う
- Node.js は remark 系
- Java は line-oriented parser helpers
- version と artifact を混同しない

