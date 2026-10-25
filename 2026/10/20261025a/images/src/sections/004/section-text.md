# miku-ms-office同梱ツールの半分を再利用する

## 主題

- 図内題名: MarkdownからOfficeへの半分を再利用
- OfficeとMarkdownの行き帰りのうち、MarkdownからOfficeへの変換CLIを再利用。Node.js版とJava版のCLIを使い、HTML変換を加えた。

## 図解キーワード

- Office→Markdown
- Markdown→Office
- 半分＝変換方向
- miku-md2docx
- miku-md2xlsx
- miku-md2pptx
- miku-md2html
- 再利用

## 関係・流れ・対比

- 既存の双方向ツールからMarkdown→Office側を選ぶ ＋ HTML変換 → 四形式

## 図解構造

- layout-family: layers
- primary-relation: 既存の双方向ツールからMarkdown→Office側を選ぶ ＋ HTML変換 → 四形式

## グラレコ構図案

- 左: 既存miku-ms-office-skillsを上下二段。「Office→Markdown」は薄い補助欄、「Markdown→Office」は選択された強い色で囲む。両方向が再利用対象に見えないようにする。
- 中央: 主図は選んだMarkdown→Officeから独立した3カード「miku-md2docx → DOCX」「miku-md2xlsx → XLSX」「miku-md2pptx → PPTX」。
- 右: 別の「miku-md2html → HTML」を加えた四形式の枠。下に「Node.js版 / Java版」。カード同士を変換する矢印は禁止。
- 最も大きく見せる主図: 上記のprimary-relation。左右と中央の関係を明確にする。
- みくくの表情・視線: 画面の右下、または指定がある場合は中央下。画面の20%程度の大きさで1人。やわらかな少し照れた説明表情で主図を見る。キャラの外観は正本を維持。何も持たない。自然な空の手。
- 吹き出し: 「半分」は、変換する方向のことです。

## 正確性メモ

- 対象セクションの本文だけに基づく。再利用対象はMarkdown→Office方向のCLI。Office→Markdownを新Skillに同梱した図にしない。
- 設計文は印刷せず、題名・短いラベル・吹き出しだけを画像内に描く。出力形式カード同士を連続変換する矢印を描かない。足りない情報を別セクションから補わない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右の3領域、主図を最大化
- 均一に明るい白〜薄いアイボリー。濃色の読みやすい文字。淡い暖色、ティールの囲み、手描き線と矢印。暗い陰影やビネットなし。
- fully opaque background; no transparent or semi-transparent pixels
- みくくは説明役として読める大きさで1人、短い吹き出しを1つ、物を持たない

## 変更（deviation）

- none
