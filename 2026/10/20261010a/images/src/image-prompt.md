## Style Contract

- Use case: infographic-diagram. Asset: Japanese article graphic-recording explainer poster.
- style-profile: mikuku-graphic-recording-v1
- 横長 3:2 の高精細な技術グラレコ説明ポスターを1枚描く。
- 均一に明るい白〜ごく薄いアイボリー（#FFFDF5）。fully opaque background; no transparent or semi-transparent pixels.
- 暖色の紙らしさはごく淡く、やわらかい手描き線、ホワイトボード解説風。文字は読みやすい濃いブラウン。ミント・淡い青・桃色・淡い黄は囲みと矢印だけに使う。
- 暗い色かぶり、周辺減光、古紙の汚れ、文字の背後の陰影を避ける。四隅・下端の注記も明瞭な濃色で描く。
- 左・中央・右の3領域。主図を最も大きく、矢印・囲み・紙アイコン・チェックを十分に描く。企業スライドや風景画にしない。
- 説明役みくくを右下に1人、画面面積の約20%を目安に、上半身で認識できる大きさに描く。極端に小さくしない。物を持たない。Do not let Mikuku hold any objects.
- 読める短い日本語の吹き出しを1つ描く。本文は「あの…文書に、また出番ができるんです。」
- 図解ラベルは手書き風でも字形を崩さず、下記の文言を正確に描く。長い段落ではなく短いラベルを使う。日本語テキストと関係線の明瞭さを優先する。

## Article-specific Design

- タイトルは上端に大きく、正確に「Agent Skillsで『活きたドキュメント』へ」。補助タイトル「規約・ルール・チェックシートが、日々の仕事につながる」。
- layout-family: flow
- primary-relation: 規約・ルール・チェックシート → Markdown → Agent Skills → 文書を参照して点検・判断材料・条件付き修正
- secondary-relations: 人の記憶頼みから文書に沿う確認へ／仕事で使う → 文書を更新 → 次の仕事で使う循環
- 図解キーワードを保持する: 規約・ルール・チェックシート／Markdown／Agent Skills／点検／判断材料／条件付き修正／根拠と一緒に指摘／見逃しを減らす／判断の観点を共有／文書を更新。

### 左の領域：仕事につながる入口

左上に「規約・ルール・チェックシート」と3枚の紙アイコン。紙それぞれの短いラベルは「規約」「ルール」「チェックシート」。紙の下に、小さな控えめな囲みで「記憶頼み」「読むのが後回し」。これは記事の困り事。
紙から右へ、しっかり太い手描き矢印を引き、「Markdownに整える」の短い注記を付け、「Markdown」の紙アイコンへつなぐ。

### 中央の領域：最も大きい主図

最大の主図は、文書からAgent Skillsを経て日々の点検・判断・条件付き修正へつながる流れ。
中央上部に「Markdown」→「Agent Skills」→「対応エージェント」の明確な流れを描く。「Agent Skills」の箱には「いつ・どう使うか」の副ラベルを入れる。「対応エージェント」の箱には「文書を参照」の副ラベルと小さな歯車。エージェントに第二の人物やマスコットを描かない。
「対応エージェント」から中央中段の3つの出力枠へ矢印を分岐する。
出力枠A: 「点検」。チェックアイコンと「根拠と一緒に指摘」。
出力枠B: 「判断材料」。整理した紙のアイコンと「次の作業へ」。
出力枠C: 「条件付き修正」。小さな編集アイコン。
出力枠Cの直下に、十分読みやすい注意囲みを付ける。見出し「修正の条件」、内容は「編集できる環境」「変更の許可」「判断材料がそろう」。この条件を3つとも省略しない。条件を修正枠に線で接続する。
小さなメリット枠として「見逃しを減らす」「判断の観点を共有」を描き、点検・判断材料と短い線で関連づける。

### 下部の補助図：使うことが更新につながる

左〜中央の下部に、読みやすい3段階の小さな循環を描く。
「仕事で使う」→「文書を更新」→「次の仕事で使う」→最初へ戻る曲線の矢印。
更新ラベルの下に短く「古くなったところを直す」。円環は補助図とし、中央の主図より小さく、文字は薄くしない。

### 右の領域：みくくが説明

右下のみくくは、やさしく少し困り眉、軽い頬の赤み。顔と視線は左上の主図へ向ける。両手は画面の下に自然に収め、何も持たない。右上に、彼女へ尾がつながる吹き出しを1つ。「あの…文書に、また出番ができるんです。」を正確に描く。
Same character Mikuku / みくく. Do not redesign. Preserve character identity: facial outline, eyes, caramel-chestnut twin-tails, black ribbons with deep-red trim, gentle shy impression. The following is the canonical character prompt, integrated into this image. Its gaze may turn toward the diagram at upper left, and its minimal warm background must be interpreted as the uniformly bright paper of the poster.

Canonical character prompt (source: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md):

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

### 正確性・避けたい表現

記事にある内容だけを説明する。修正は編集環境・許可・判断材料がある場合に限定。確認漏れを減らす助けとして表現する。全自動・漏れゼロ・必ず守るなどの保証を足さない。新しい固有名詞、数値、評価、モデル名、価格、日付、作成環境を足さない。上記のセクション名、内部メタデータ、canonical prompt、ファイルパス、正確性メモは画像に描かない。
背景の主役に建物・植物・机・大きな風景を描かない。写実、強いSF、フラットすぎるUI、暗い紙面、淡い文字、余白ばかり、文字の極端な少なさを避ける。図解の枠や矢印をみくくの顔・髪・吹き出しに重ねない。

## Deviation Record

none
