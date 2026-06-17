# グラレコ制作用整理テキスト

## 1. 大テーマ

**簡易RAG風 Agent Skill step2**

- step1: `SKILL.md` + `references/raw/`
- step2: そこへ `index.json` を足す
- 目的: AI agent が本文へ向かう前に「軽い地図」を見る
- 大きな改造ではなく、探索の入口を整える

```text
ユーザー依頼
  ↓
SKILL.md
  ↓
index.json で候補を見る
  ↓
必要な Markdown 本文を読む
  ↓
回答を整理する
```

## 2. なぜ index が必要？

- 記事が増えるほど、探索対象が広がる
- 直接 raw corpus を探すと、迷いとトークン消費が増えやすい
- `index.json` は本文の代わりではなく、本文へ向かうための入口

キーワード:

- 地図
- 目録
- 候補選び
- 迷子になりにくい入口
- 本文へ行く前の座標

## 3. 役割分担

| 要素 | 役割 |
| --- | --- |
| `SKILL.md` | 作業指示、探索順、禁止事項 |
| `README.md` | checkout 後の復元手順 |
| `references/raw/mikuku-articles` | 記事本文 Markdown の実データ |
| `index.json` | miku-indexgen が作る軽い索引 |
| `miku-indexgen` | ファイル索引を再生成するツール |

```text
raw = 知識本体
index = 本文へ向かう地図
SKILL.md = 地図を先に見る指示
```

## 4. 作業の流れ

```text
1. step01-01 を checkout
2. README.md を作る
3. references/raw/mikuku-articles を配置
4. index.json なしで同じプロンプトを実行
5. 基準状態を記録
6. miku-indexgen で index.json を生成
7. SKILL.md に「まず index」を追記
8. 同じプロンプトを再実行
9. 探索の流れとトークン消費を見る
```

## 5. Before / After

### Before: index なし

- `SKILL.md` と `README.md` を読む
- `references/` 配下を直接探そうとする
- `.gitignore` や raw corpus の配置により探索が揺れる
- 別の探索へ切り替える場面が出る

### After: index あり

- `SKILL.md`、`README.md`、`index.json` を読む
- `index.json` から候補記事を拾う
- 関連する本文 Markdown へ進む
- 探索の入口が安定する

```text
なし: 広い棚を直接探す
あり: 目録を見る → 必要な棚へ行く
```

## 6. 測定結果

同じプロンプト、GPT-5.5 medium、画面表示上の used token。

| 条件 | 単純平均 |
| --- | ---: |
| index.json なし | 約 110.6K used |
| index.json あり | 約 82.4K used |

- 差分: 約 28.2K used
- 割合: だいたい 25% 低め
- ただし揺れは大きい
- 厳密なベンチマークではなく観察

## 7. 大事な解釈

- `index.json` は魔法ではない
- 記事群の主張を知るには本文 Markdown を読む必要がある
- 効くのは主に「探索の入口」
- 同じ依頼でも、最初に見る場所が変わる
- 迷い方が変わることで、トークン消費が低めに出やすい

## 8. 次の展開

- step2: 地図を置く
- 次の step: よく使う知識を短く蒸留する
- 索引 + 蒸留 Markdown で、さらに扱いやすい Agent Skill へ育てる

```text
運用
  ↓
観察
  ↓
index 追加
  ↓
探索が安定
  ↓
よく使う知識を蒸留
  ↓
次回さらに安定
```

## 9. みくく吹き出し候補

- 「あ、あの…本文へ行く前に、まず小さな地図を見るのです…」
- 「index は答えではなく、入口なのです…！」
- 「同じお願いでも、最初に見る場所が変わると迷い方も変わります…」
- 「次は、よく通る道に小さなメモを置く感じかもしれません…」
