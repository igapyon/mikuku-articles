# Exit code

- `0`: success / metadata command
- `1`: usage error / file I/O / parse error / unexpected runtime error

```text
0 -> 正常
1 -> 入力・処理・実行の問題
```

- 自動化では終了コードで次の処理を判断する

