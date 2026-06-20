# グラレコ制作用整理テキスト

対象記事: `20260620-agent-skills-rag-step-03-distilled-answer-skeleton.md`

# 1. この記事の中心

**蒸留 Markdown は「意味の地図」**

- raw 記事本文の代替ではない
- 要約でも、回答テンプレートでもない
- 人間と AI agent が同じ全体像を見るための context artifact
- raw に戻る前に、どの資料を何のために読むかを絞る

```text
index.json = ファイルの地図
distilled Markdown = 意味の地図
raw Markdown = 根拠を確認する一次資料
```

# 2. step2 から step3 へ

## step2

- `miku-indexgen` で `index.json` を作成
- 探索の入口ができた
- ただし、主張や考え方を答えるには raw 本文が必要

```text
index.json なし: 平均 約 110.6K used
index.json あり: 平均 約 82.4K used
```

## step3

- `references/distilled/` に蒸留 Markdown を追加
- 先に意味構造をつかむ
- 必要な raw へ戻る判断を明示する

```text
探す入口
  ↓
意味の地図
  ↓
必要な raw
  ↓
根拠つき回答
```

# 3. 誤解しやすい対比

| 誤解 | 記事の位置づけ |
| --- | --- |
| raw を読まなくてよくする | raw に戻る前の見通しを作る |
| トークン削減だけが目的 | 読み方と根拠確認を安定させる |
| 記事ごとの要約 | 資料群をまたぐ意味構造 |
| AI agent の回答手順書 | 人間と AI agent の共有コンテキスト |
| 便利なまとめ | 根拠へ戻る順番を作る層 |

# 4. 蒸留 Markdown に入れるもの

- 中心概念
- 主要な主張
- 観測されたこと
- まだ断定できないこと
- raw に戻るべき条件
- 元記事へ戻るための手がかり

```text
よく整理された事実
概念同士の関係
背景
制約
未確定点
参照すべき根拠
```

# 5. 作るファイル

最初は 1 本から始める。

```text
references/distilled/
  agent-skills-context-map.md
```

大きくなりすぎたら、あとから自然な境界で分ける。

- 思想
- 構造
- 実験
- 運用

# 6. index.json も整える

蒸留 Markdown を置くだけでは入口にならない。

- `SKILL.md` から `references/distilled/` をたどれるようにする
- `index.json` を再生成する
- 画像生成用補助 Markdown はノイズになりやすい
- `--exclude-glob` で `images-*` / `images` 配下を除外

```text
地図に載せるものを選ぶ
  ↓
読み始める入口が見やすくなる
```

# 7. 期待する読み方

```text
1. SKILL.md
   ↓
2. index.json と references/distilled/ の存在を知る
   ↓
3. distilled Markdown で意味の地図を見る
   ↓
4. 質問が根拠確認を求めるか判断
   ↓
5. 必要な raw 記事本文へ戻る
   ↓
6. 意味構造と raw の根拠を分けて回答
```

# 8. 動作確認で見るもの

- 最初にどのファイルを見たか
- `agent-skills-context-map.md` を意味の地図として使ったか
- raw 記事本文へ戻る判断を明示したか
- 記事ごとの羅列ではなく、資料群の内容構造になったか
- トークン消費がどのくらい揺れたか

```text
step3 構成:
75K / 84.2K / 94.9K / 72.4K / 65K / 72.1K used

平均 約 77.3K
中央値 約 73.7K
```

ただし、これは厳密なベンチマークではない。

# 9. 記事の結論

```text
index.json
  どのファイルがあるかを見つける

references/distilled/
  資料群の意味構造を先につかむ

references/raw/
  主張や根拠を確認するときに戻る
```

**step3 は、トークン削減の成功談ではない。**

**意味の地図を作り、AI agent と人間が同じ景色を見てから歩き出すための設計。**

