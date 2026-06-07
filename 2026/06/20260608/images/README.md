# Export Images

Note などへアップロードしやすいように、代表画像とセクション別画像を連番ファイル名でコピーしたフォルダです。
元画像は親ディレクトリと `sections/` 配下に残しています。

## Files

- `000-whole-article.png`: 記事全体の代表画像
- `001-introduction.png`: はじめに
- `002-seven-copilots.png`: まずは大きく7つに分ける
- `003-model-names.png`: モデル名は、見えるものと見えないものがある
- `004-microsoft-copilot-chat.png`: Microsoft Copilot は、普通のAIチャットに近い
- `005-copilot-in-m365-apps.png`: Microsoft 365 アプリ内の Copilot は、Officeアプリの中に入る
- `006-m365-copilot-business-ai.png`: Microsoft 365 Copilot は、会社向けの業務AIとして見る
- `007-copilot-chat-rag.png`: Copilot Chat は、利用者視点では RAG のように見える
- `008-edge-microsoft-search.png`: Edge から利用する Microsoft Search 体験では、社内検索に近づきやすい
- `009-copilot-studio-builder.png`: Copilot Studio は、Copilotを作る側の道具
- `010-copilot-studio-data.png`: Copilot Studio は、データ作りが重要になる
- `011-github-copilot.png`: GitHub Copilot は、開発者向けなので別枠で見る
- `012-copilot-cowork.png`: Copilot Cowork は、Frontier の先行公開系として見る
- `013-how-to-understand.png`: どう理解すればよいか
- `014-closing.png`: おわりに

## Verification

```bash
shasum -a 256 -c checksums.sha256
```
