# もの同士の関係を書いてみる グラレコ整理

- 主題: `classDiagram` で User と Order の関係を書く
- Markdown の `mermaid` コードブロック
- テキストが図として表示される
- User は Order を持つ
- 1 対 0..* の関係

```text
User
  └─ places
       ↓
     Order
```

キーワード:
- classDiagram
- クラス
- 属性
- 操作
- 関連

吹き出し:
「まずは、もの同士のつながりを小さく描いてみます…」

