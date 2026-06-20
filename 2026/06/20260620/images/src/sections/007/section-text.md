# Section Graphic Recording Text

## 見出し

SKILL.md に distilled の入口を書く

## 主題

`SKILL.md` は個別ファイル名の一覧ではなく、読む順番と置き場所の入口だけを持つ。

## キーワード

- `SKILL.md`
- `index.json`
- `references/distilled/`
- `references/raw/`
- 入口
- 個別ファイル名を並べすぎない
- 役割分担
- 入口を軽く保つ

## 図解

```text
SKILL.md
  = 入口と読む順番

index.json
  = ファイルの地図

references/distilled/
  = 意味の地図置き場
```

## 設計

- `SKILL.md` に個別の蒸留 Markdown 名を直接並べない
- 追加や改名のたびに `SKILL.md` を直す負担を避ける
- 必要な蒸留 Markdown は `references/distilled/` を見て選ぶ

## 吹き出し案

「SKILL.md は入口、細かい地図は別に置くのです…」

