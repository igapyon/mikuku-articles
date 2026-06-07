# 処理のやり取りを書いてみる グラレコ整理

- 主題: `sequenceDiagram` で注文処理のやり取りを書く
- 登場人物: User, App, Service, Database
- メッセージが順番に流れる
- 注文する
- createOrder()
- insert(order)
- OK
- 注文完了

```text
User → App → Service → Database
          ←        ←
注文完了
```

キーワード:
- sequenceDiagram
- 参加者
- メッセージ
- 時間の流れ

吹き出し:
「誰が誰に話しかけるかを、順番で見ます…」

