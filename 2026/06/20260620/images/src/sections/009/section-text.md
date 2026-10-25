# Section Graphic Recording Text

## 見出し

同じ問いで動作確認する

## 主題

同じ探索タスクで、step3 構成が `distilled` を意味の地図として使い、必要な raw へ戻るかを観察する。

## キーワード

- 同じ問い
- 動作確認
- step3 構成
- `SKILL.md`
- `index.json`
- `agent-skills-context-map.md`
- raw へ戻る判断
- 厳密なベンチマークではない
- トークン消費の揺れ

## 観測値

- 75K used
- 84.2K used
- 94.9K used
- 72.4K used
- 65K used
- 72.1K used
- 平均 約 77.3K used
- 中央値 約 73.7K used

## 図解

```text
同じ問い
  ↓
SKILL.md / index.json / distilled
  ↓
必要な raw
  ↓
資料群の内容構造として回答
```

## 注意点

- distilled だけの効果とは言い切らない
- `--exclude-glob` による索引ノイズ削減も効いた可能性がある
- 消費量だけでなく、読み方と回答構造を見る

## 吹き出し案

「大きい消費量も、次に整える場所を教える観測点なのです…」

