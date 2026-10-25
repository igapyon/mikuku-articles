# 共通オプション

- Node.js 版と Java 版の主な共通 option
- 通常変換は最小形から始める

| option | 役割 |
| --- | --- |
| `--out <path>` | PPTX 出力先、必須 |
| `--title <text>` | generated presentation title を上書き |
| `--version` | package version |
| `--help` | help |

確認していないもの:

- summary
- summary JSON
- assets directory
- debug comment

メッセージ:

- 余計な option を invent しない
- 生の `--help` を契約として扱う
