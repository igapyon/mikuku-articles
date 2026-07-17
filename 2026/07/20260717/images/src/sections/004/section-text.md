# handoff出力を、少なく、分かりやすくする

## 主題

生成AIへ渡す順番を明確にし、管理するファイル数と会話中の迷いを減らすhandoff出力の改善。

## 図解キーワード

- 読み込み順を固定
- filename prefix
- YAML front matter
- promptとindexをPartへ同梱
- 中間Partは「OK」のみ
- Markdown自身が読み方を伝える

## 関係・流れ・対比

左で旧構成のprompt＋複数Part＋indexを示し、中央で整理、右でPartだけのcompact出力へ変化させる。Part 1にprompt、最終Partにindex、中間Partにacknowledgement footerを示す。

## グラレコ構図案

- 左: ファイルが多く順番に迷う旧handoff
- 中央: 順序・prefix・metadataの整理
- 右: Part 1→Part 2→最終Partの簡潔な列
- みくく: 右下でファイルを順番どおり差し出す姿。視線は矢印へ
- 吹き出し: 「この順番で、どうぞ」

## 正確性メモ

- v1.1.0以降は独立したprompt/indexを廃止しPartへ同梱。
- 中間Partの案内は最終Part前の分析を抑え、OKのみを促す。
- 標準出力ではなく生成Markdownが受け渡しの正本。
