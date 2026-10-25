# 多数のファイルから配備用データを準備する

## 主題

- 多数のテキストファイルを少数の Knowledge 向け Markdown へバンドルする。
- Agent Builder 向けには Markdown を DOCX へ変換する。
- `upload/` と、名前・説明・Instructions などの設定用 Markdown を準備する。

## 図解キーワード

- miku-text-bundle
- 少数の Markdown
- miku-md2docx
- DOCX
- upload/
- 設定用 Markdown

## 関係・流れ・対比

多数のテキスト → `miku-text-bundle` → 少数の Knowledge Markdown

Agent Builder: Markdown → `miku-md2docx` → DOCX

Gem Classic: Markdown のまま／DOCX を選択

## グラレコ構図案

- 左: 相対パスと境界を持つ多数のテキストファイル。
- 中央: 上段にバンドル、下段に DOCX 変換の二つの工程。
- 右: `upload/` と設定用 Markdown、その先に Agent Builder と Gem Classic。
- みくくの表情・視線: 中央の変換フローを見て、丁寧に順路を説明する。
- 吹き出し: 「まとめて、渡せる形へ」

## 正確性メモ

- 多数のファイルを少数へまとめ、Markdown を DOCX へ橋渡しするのが主要機能。
- 自動アップロードや共有は行わない。
- みくくには物を持たせない。
