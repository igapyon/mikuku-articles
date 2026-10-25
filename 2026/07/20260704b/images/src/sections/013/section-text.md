# Exit code

- CLI 結果を機械的に判断するための番号

| code | 意味 |
| --- | --- |
| 0 | success / metadata command |
| 1 | conversion / runtime / IO error |
| 2 | input または `--out` 不足 |

- CI や Agent 実行で扱いやすい
- 引数不足と変換失敗を分けられる

