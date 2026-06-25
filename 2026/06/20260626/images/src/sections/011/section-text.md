# 最初に試すなら

- 小さな Web アプリや検証ページに 1 本だけ E2E テストを書く
- いきなり大きな基盤にしない

最初のコマンド:

```text
npm init playwright@latest
npx playwright test
npx playwright show-report
```

小さい確認:

- トップページが開ける
- ログイン画面が表示される
- フォーム入力
- 保存後メッセージ
- 一覧にデータ表示

吹き出し: 「手で毎回見ている確認を、少しずつ渡していきます…」
