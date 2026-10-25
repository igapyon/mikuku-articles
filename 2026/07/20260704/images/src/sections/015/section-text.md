# Exit code

- `0`: success / metadata command
- `1`: usage error、I/O error、parse error、runtime error
- batch や agent 実行では exit code が判断材料

## 図解

```text
0 -> success
1 -> error
```

## 短いラベル

- success
- metadata command
- usage error
- runtime error

