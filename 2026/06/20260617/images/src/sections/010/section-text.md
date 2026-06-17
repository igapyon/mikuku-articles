# 010 同じプロンプトをもう一度実行する

## 主題

- `index.json` と `SKILL.md` の追記後、同じプロンプトを再実行する
- ユーザー依頼は変えない
- Agent Skill 側の入口だけが変わる

## 観察された流れ

```text
SKILL.md
  ↓
README.md
  ↓
index.json
  ↓
候補 Markdown
  ↓
本文を読む
  ↓
Agent Skills の主張を整理
```

## 主な整理

- Agent Skills は単なるプロンプト集ではない
- AI agent に渡す再利用可能な作業仕様
- `SKILL.md` は入口、判断基準、参照先、出力形式を決める
- 詳細知識は `references/`、出力構造は `templates/`、温度感は `examples/`

## キーワード

- 同じプロンプト
- 入口の変化
- index.json を先に読む
- 本文 Markdown へ進む

## 吹き出し候補

「同じお願いでも、最初に見る場所が変わりました…」
