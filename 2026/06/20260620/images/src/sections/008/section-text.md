# Section Graphic Recording Text

## 見出し

期待する読み方

## 主題

AI agent が `SKILL.md`、`index.json`、`distilled`、必要な `raw` の順に読み、意味構造と根拠を分けて回答する。

## キーワード

- 読む順番
- `SKILL.md`
- `index.json`
- `references/distilled/`
- 意味の地図
- `references/raw/`
- 根拠確認
- 答えの代用品ではない

## 図解

```text
1. SKILL.md
2. index.json
3. distilled Markdown
4. raw 候補を絞る
5. 必要な raw 本文へ戻る
6. 意味構造 + 根拠で回答
```

## 注意点

- 蒸留 Markdown だけで答え切らない場合がある
- 既存記事の主張や根拠を聞かれたら raw へ戻る
- 根拠を隠す層ではなく、根拠へ戻る順番を作る層

## 吹き出し案

「意味の地図を見てから、必要な raw へ戻るのです…」

