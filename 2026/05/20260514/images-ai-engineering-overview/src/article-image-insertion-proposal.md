# Article Image Insertion Proposal

対象記事:

```text
/Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-note-writer/references/general/20260514-general-ai-engineering-overview.md
```

生成画像:

```text
/Users/igapyon/Documents/git/igapyon-agent-skills/workplace/20260524205052-graphic-recording/graphic-recording.png
```

## 推奨位置

`## はじめに` の本文で “Engineering” 群を列挙した直後に置く案が自然です。

理由:

- 記事全体の地図として機能する
- Prompt Engineering から Context Engineering への主題が早い段階で伝わる
- 以降の各 Engineering 説明を読むための足場になる

## 差し込み候補

次の段落の後:

```markdown
たとえば、次のような言葉です。

- Prompt Engineering
- Context Engineering
- Retrieval Engineering
- Tool Engineering
- Agent Engineering
- Repository Engineering
```

差し込み案:

```markdown
![生成AI開発における Engineering の変化を整理したグラレコ画像。Prompt Engineering から Context Engineering への流れ、Retrieval、Tool、Agent、Repository Engineering の関係、README、docs、TODO、search tool、Agent Skills、memory などの context 供給装置を、みくくが説明している。](./workplace/20260524205052-graphic-recording/graphic-recording.png)

Prompt の時代から Context の時代へ。AI が迷わず作業できる構造を作るための Engineering 整理です。
```

## Note 投稿時の注意

Note ではローカルパスをそのまま参照できないため、実際の投稿時は `graphic-recording.png` を Note の画像アップロード機能でアップロードしてください。

アップロード後、キャプションとして次を使えます。

```text
Prompt の時代から Context の時代へ。AI が迷わず作業できる構造を作るための Engineering 整理。
```

alt text として次を使えます。

```text
生成AI開発における Engineering の変化を整理したグラレコ画像。Prompt Engineering から Context Engineering への流れ、Retrieval、Tool、Agent、Repository Engineering の関係、README、docs、TODO、search tool、Agent Skills、memory などの context 供給装置を、みくくが説明している。
```
