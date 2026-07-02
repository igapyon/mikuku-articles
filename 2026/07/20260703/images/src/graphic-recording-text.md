# グラレコ制作用整理テキスト

## 1. 何の紹介？

- miku-ms-office-skills
- OSS の Agent Skills package
- Office ファイルを Markdown 化
- AI agent が読みやすい作業資料へ寄せる

```text
Word / Excel / PowerPoint
        ↓
miku-ms-office-skills
        ↓
GitHub風 Markdown
        ↓
AI agent が読む
```

## 2. 変換の中心

| 入力 | 出力 | 主な対象 |
| --- | --- | --- |
| .docx | .md | 本文、表、コメント系テキスト |
| .xlsx | .md | 表、簡単な Excel 方眼 |
| .pptx | .md | スライド内テキスト |

- Markdown から Office へ戻す方向は experimental
- まずは Office から Markdown への入口として考える

## 3. 大事な割り切り

| 目指すこと | 目指さないこと |
| --- | --- |
| AI agent が読みやすい | 見た目の完全再現 |
| テキスト中心 | 複雑な装飾の再現 |
| ローカル実行 | ネットワーク変換サービス |
| 軽い前処理 | 万能変換アプリ |

## 4. うれしい流れ

```text
Office 完成物
  ↓ 中身を取り出す
Markdown 作業資料
  ↓ 確認・要約・比較
AI agent との次の作業
```

- 本文確認
- 要約
- 関連メモとの比較
- リポジトリ差分
- 不要部分の削除
- 消費トークンの抑制につながる場合がある

## 5. 使いどころ

- Word の仕様メモを読ませる
- Excel の一覧表を要約する
- PowerPoint のスライド内テキストを取り出す
- Office と Markdown 資料を比較する
- 手元の資料を軽い .md にしておく

## 6. 向いていないこと

- レイアウト忠実再現
- 図形やチャートの完全変換
- 画像内文字の OCR
- 複雑な帳票レイアウト
- Office ファイルの美しい再編集

## 7. ベータ版として育てる

```text
実ファイルで試す
  ↓
癖を見つける
  ↓
変換範囲を調整
  ↓
Agent Skills を育てる
```

- Office ファイルには作り手ごとの癖がある
- 最初から万能とは言わない
- 現状の機能でできる範囲を大事にする
- 育てている OSS の Agent Skills

## 8. まとめ

- 小さな入口
- 地味な前処理
- ローカルで軽く動く
- Office を AI agent 用の Markdown 作業資料へ変える
- 次の作業を始めやすくする
