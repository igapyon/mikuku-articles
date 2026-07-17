# はじめての方へ：miku-text-bundleとは

## 主題

散らばったテキストを、ファイル境界を保ったまま、渡し先に合う分割Markdownへ整理するCLIツール。

## 図解キーワード

- README・設計資料・TODO・ソースコード
- 収集・除外・順序・文字コード・サイズ制限
- ファイル境界を保持
- handoff
- knowledge-source

## 関係・流れ・対比

左の散らばった複数ファイルが中央のmiku-text-bundleを通り、右で2本に分岐する。上は会話用のhandoff、下は中立的なKnowledge source。共通の土台は収集・除外・分割。

## グラレコ構図案

- 左: 種類の違うファイルが散らばる机
- 中央: 静かに整える箱「miku-text-bundle」
- 右上: handoff「順番・応答指示あり」
- 右下: knowledge-source「会話用指示なし」
- みくく: 中央下で荷物を包むような仕草。視線は2つの渡し先へ
- 吹き出し: 「渡す前に、整えます」

## 正確性メモ

- 指定ディレクトリ以下のテキストファイルを収集するCLI。
- 出力はファイル境界を保った分割Markdown。
- handoffとknowledge-sourceの2モードがある。
