# Version

`20260728a`

## Versioning

このリポジトリでは、`VERSION.md` に記載した値を正式なバージョンとします。

バージョンは、Asia/Tokyo の日付を使った `YYYYMMDD<sequence>` 形式です。

- `YYYYMMDD` はバージョンを更新した日付です。
- `<sequence>` は同じ日付内の更新順です。最初を `a` とし、`b`、`c` の順に進めます。
- `z` の次は `aa`、`ab` の順に進めます。
- 日付が変わった最初のバージョンでは、`<sequence>` を `a` に戻します。
- GitHub のタグ名には、`VERSION.md` の値へ `v` 接頭辞を付けた `v<version>` 形式を使用します。

例:

```text
20260724a
20260724b
20260725a
```

対応する GitHub タグの例:

```text
v20260724a
v20260724b
v20260725a
```

過去の `tagYYYYMMDD...` 形式や `v` 接頭辞のないタグは旧形式として扱い、新しいバージョンには使用しません。
