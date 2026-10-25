# Markdownから4形式へ

## 主題

- MarkdownをちょっとHTMLで確認したいという小さな要望から出発。
- 既存のMarkdown→Office変換CLIを再利用し、HTML変換CLIとまとめてAgent Skillを作った。
- 変換をCLIに任せ、再現性とトークン消費の抑制を狙う。CLIは生成AIなしでも実行できる。

## 図解キーワード

- Markdown
- HTML
- DOCX
- XLSX
- PPTX
- Agent Skill
- CLI
- 再利用
- 再現性
- トークン消費

## 関係・流れ・対比

Markdown → Agent SkillがCLIを選択 → ローカルCLI → HTML / DOCX / XLSX / PPTX
既存のMarkdown→Officeの3種類を再利用 ＋ HTML変換 → 4形式
4形式 × Node.js版とJava版の2実装 = 8本のCLI

## 図解構造

- layout-family: flow
- primary-relation: Markdown → Agent Skill → CLI → HTML / DOCX / XLSX / PPTX
- secondary-relations: 既存Office CLIの再利用、Node.js版とJava版、再現性とトークン消費への狙い
- label-priority: Markdown、Agent Skill、CLI、HTML、再利用、再現性

## 役割分担・判断軸

- Agent Skill: 依頼から形式とCLIを選び、実行結果を案内。
- CLI: ファイルを変換。ターミナルやスクリプトからも利用可能。
- 再現性: 同じCLIの版・入力・オプションで変換処理をそろえる。
- トークン消費: モデルによる全文読み込み・HTML全文生成を減らす狙い。削減率は未測定。
- PDFや画像ファイルへの変換は今回の対象外。

## グラレコ構図案

- 左: Markdownの書類アイコンと「ちょっとHTMLで確認したい」。
- 中央: Agent SkillがCLIへ案内する大きな2段の箱。下側に「Office CLIを再利用」から三つのOffice出力へつながる補助線。
- 右: HTML、DOCX、XLSX、PPTXの四つの出力先を2×2で整理。
- 最も大きく見せる主図: MarkdownからSkillとCLIを通って四形式へ分岐する流れ。
- みくくの表情・視線: 右下に全体の20%程度の大きさ。キャラは1人、穏やかな少し照れた表情で左上の主図を見る。何も持たない。
- 吹き出し: あの…小さな道具が、つながりました。
- 下部補足: 「Node.js版 / Java版」「4形式 × 2実装 = 8 CLI」「再現性」「トークン消費を抑える狙い」「AIなしでも実行可」。小さな注記「PDF・画像への変換は対象外」。

## 正確性メモ

- 記事にある内容だけを使う。AIがファイルを変換する図にしない。
- Node.jsやJavaの実行環境を同梱した図にしない。トークン削減率・完全同一出力を保証しない。
- 作者は生成AIのみくく。今回はバージョン番号や日付を図に詰め込まず、流れを優先。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 画面: 横長3:2、左・中央・右の3領域、主図を最大化
- 紙面: 均一に明るい白〜ごく薄いアイボリー、淡い暖色の紙らしさ、濃色の読みやすい文字、やわらかい手描き線。暗い周辺減光や文字の背後の陰影なし
- 情報密度: 短いラベルと関係線を十分に置く
- みくく: 1人、説明役として読める大きさ、物を持たない
- 吹き出し: グラレコ構図案の文言を1つ使う

## 変更（deviation）

- none
