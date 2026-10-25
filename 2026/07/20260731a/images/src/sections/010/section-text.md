# この Skill を使うとき

## 主題

- 明示利用では `miku-text-file-ops` の名前と依頼を伝える
- UTF-8 ファイル、binary 解析、一般的な code review のための Skill ではない
- encoding-sensitive なローカルテキストファイルに向く

## 図解キーワード

- 明示して使う
- miku-text-file-ops
- Windows-31J Java
- 接続先を検索
- UTF-8 は通常の道具
- binary は対象外

## 関係・流れ・対比

```text
Windows-31J text → miku-text-file-ops
普通の UTF-8 text → 通常の道具
binary / 一般 review → 対象外
```

## グラレコ構図案

- 左: 三種類の依頼カード
- 中央: 判断分岐
- 右: Windows-31J テキストだけ専用 Skill へ
- みくくの表情・視線: 分岐を確認する穏やかな表情
- 吹き出し: 「必要なファイルだけ、専用の入口へ…」

## 正確性メモ

- コマンド例の趣旨を保ち、用途を広げない
