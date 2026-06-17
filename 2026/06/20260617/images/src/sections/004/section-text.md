# 004 step01-01 タグを checkout する

## 主題

- きれいな作業用リポジトリから始める
- step1 終了時点の `step01-01` タグを使う
- どこから何が増えたかを分かりやすくする

## 操作

```bash
git clone ...
cd mikuku-articles-rag-skill
git checkout step01-01
```

## 状態

- `SKILL.md` と `.gitignore` はある
- `references/raw/` の記事データは Git 管理外
- checkout 直後には raw 記事データは入っていない

## 図解ポイント

```text
新しい checkout
  ↓
step01-01
  ↓
最小構成から再開
```

## キーワード

- clean checkout
- step01-01
- Git 管理外データ
- 再現性

## 吹き出し候補

「途中状態ではなく、きれいな出発点から見直します…」
