# Section Graphic Recording Text

## 見出し

生成後に index.json を更新する

## 主題

蒸留 Markdown を置いただけでは入口にならないため、`SKILL.md` と `index.json` から見つけられるように整える。

## キーワード

- `references/distilled/`
- `SKILL.md`
- `index.json`
- ファイルの地図
- ノイズ削減
- 画像生成用補助 Markdown
- `--exclude-glob`
- `**/images-*/**`
- `**/images/**`

## 図解

```text
distilled Markdown を置く
  ↓
SKILL.md から場所をたどれる
  ↓
index.json を再生成
  ↓
不要な images 系 Markdown を除外
```

## 対比

| ノイズが多い地図 | 見やすい地図 |
| --- | --- |
| 補助 Markdown まで大量に載る | 読むべき入口を探しやすい |
| 目的地が見えにくい | `distilled` と `raw` へ進みやすい |

## 吹き出し案

「地図に載せるものも、少し選ぶ必要があるのです…」

