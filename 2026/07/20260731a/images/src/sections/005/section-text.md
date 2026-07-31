# 読むときだけでなく、最後まで同じ入口を使う

## 主題

- 操作は search / read / create / update / delete の五つ
- 読取だけ専用 CLI にして、更新を通常の UTF-8 patch tool へ戻してはいけない
- encoding-sensitive と分かった path は検証・競合回復まで同じ CLI を使う

## 図解キーワード

- search
- read
- create
- update
- delete
- 最後まで同じ入口
- 必要な path だけ

## 関係・流れ・対比

```text
安全: search → read → update → verify（同じ CLI）
危険: read（専用 CLI）→ update（UTF-8 patch tool）
```

## グラレコ構図案

- 左: search と read
- 中央: 分岐せず続く専用 CLI の一本道
- 右: update・verify・競合回復
- みくくの表情・視線: 一本道を指ささず、視線で追う
- 吹き出し: 「途中で、いつもの道具へ戻らないでください…！」

## 正確性メモ

- 普通の UTF-8 ファイルまで専用 CLI へ寄せない
