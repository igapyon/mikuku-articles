# Knowledge sourceモードを追加する

## 主題

会話用の指示を外し、Knowledge sourceへ登録しやすい中立的なMarkdownを生成する新しい出力モード。

## 図解キーワード

- --mode knowledge-source
- knowledge-001.md / knowledge-002.md
- knowledge-index.mdは管理用
- 会話用指示を含めない
- 行範囲・文字オフセットで追跡
- 登録や変換は呼び出し元の役割

## 関係・流れ・対比

中央の同じ入力テキストから、左のhandoff「会話の案内あり」と右のknowledge-source「資料を静かに置く」へ分岐。右側では登録候補と管理用indexを明確に分ける。

## グラレコ構図案

- 左: handoff、吹き出しや読み込み指示のある文書
- 中央: miku-text-bundleのモード切替スイッチ
- 右: 中立なknowledge-001/002と、別枠のknowledge-index
- みくく: 右下で静かに資料を棚へ置く姿。視線は登録候補へ
- 吹き出し: 「会話の言葉を、そっと外します」

## 正確性メモ

- mode省略時はhandoff。
- knowledge-index.mdは登録対象ではなく管理用。
- ツールの責任範囲は登録候補Markdownの生成まで。
