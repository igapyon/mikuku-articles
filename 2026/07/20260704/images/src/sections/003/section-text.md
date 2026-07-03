# 生成AI向け情報

- AI agent へ説明するときは、概要だけでは不足
- version、runtime、変換方向、入出力契約を明示
- 対応範囲と非対応範囲を分ける
- raw `--help` は機械可読な契約として役立つ

## 図解

```text
version
runtime
contract
mapping
unsupported
help output
  -> AI の誤解を減らす
```

## 短いラベル

- release tag
- docx -> md
- mapping table
- unsupported scope
- raw help

