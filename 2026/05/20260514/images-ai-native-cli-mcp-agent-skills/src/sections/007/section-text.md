# グラレコ制作用整理テキスト: stdout は contract、stderr は debug

## 1. 主題

- stdout にログや進捗を混ぜると parse が壊れやすい。
- AI が parse する stream と、人間が debug する stream を分ける。

## 2. 画像内キーワード候補

- stdin = request JSON
- stdout = response JSON
- stderr = logs
- exit code = status
- stream 分離

## 3. 図解構成

```text
stdout は contract、stderr は debug
  ↓
重要な設計観点
  ↓
AI agent が扱いやすい tool へ
```

## 4. みくく吹き出し

```text
stdout は契約、stderr は debug…ここ大事です…！
```

## 5. 描画方針

- 横長ポスター構図
- 左から中央にグラレコ図解
- 右側にみくく
- 短い日本語ラベル中心
- 長文は入れすぎない
- 手描きホワイトボード風
