# 009 SKILL.md に索引入口を足す

## 主題

- `index.json` を作っただけでは、AI agent が必ず見るとは限らない
- `SKILL.md` に「まず index.json を見る」と明示する
- 探索順序を変える小さな追記

## 追記イメージ

```markdown
If index.json exists, inspect it before searching the raw corpus.
Use the generated index to choose candidate article Markdown files.
Do not answer from the index alone.
```

## Before / After

```text
step1:
SKILL.md → raw corpus

step2:
SKILL.md → index.json → raw corpus
```

## 図解ポイント

- 地図を置く
- 「まずこれを見て」と伝える
- index だけで答えず、本文へ進む

## キーワード

- Index Guidance
- 探索順序
- 入口の向き
- raw corpus

## 吹き出し候補

「地図を置いたら、まず地図を見るようにお願いします…」
