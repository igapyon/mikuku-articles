# 007 miku-indexgen で索引を作る

## 主題

- `references/raw/mikuku-articles` を毎回直接探す前に、軽い地図を作る
- `igapyon-miku-indexgen` スキル経由で `index.json` を生成する
- 索引は手書きせず、再生成できる生成物として扱う

## 流れ

```text
references/raw/mikuku-articles
  ↓ miku-indexgen
index.json
```

## 構成

```text
mikuku-articles-rag-skill/
├── SKILL.md
├── README.md
├── index.json
└── references/raw/mikuku-articles/
```

## 注意点

- `references/raw/` は Git 管理外
- `index.json` は Agent Skill 側の参照入口
- 手編集せず、必要なら再生成する

## キーワード

- miku-indexgen
- index.json
- 生成物
- 目録
- 再生成

## 吹き出し候補

「索引は手で直さず、必要なときに作り直すのです…」
