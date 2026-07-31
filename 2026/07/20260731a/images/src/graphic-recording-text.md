# Shift_JIS を壊さず AI agent に渡す「小さな橋」

## 主題

- UTF-8 前提の agent ハーネスが、Windows-31J の検索・読取・保存で文字化けを起こす
- `miku-text-file-ops-skills` を入口にし、文字コード処理は `miku-text-file-ops` CLI に任せる
- 検索から更新・検証・競合回復まで、文字コードを守る同じ経路を使い続ける
- ハーネスが苦手なあいだだけ、必要な path を守るベータ版の小さな橋

## 図解キーワード

- Shift_JIS / Windows-31J
- 文字化け
- UTF-8 前提
- Agent Skill = 入口
- CLI = 文字コード処理
- 同じ経路
- repository rule
- revision 照合
- BOM・改行を維持
- ベータ版

## 関係・流れ・対比

### Before：いつもの道具へ戻ると経路が切れる

```text
AI agent
  ↓
UTF-8 前提の検索・読取・patch・保存
  ↓
Windows-31J の Java / JSP
  ↓
文字化け・意図しない UTF-8 化
```

### After：必要な path だけ、小さな橋を渡す

```text
AI agent
  ↓
miku-text-file-ops-skills
「いつ・どの操作・どの範囲」
  ↓
miku-text-file-ops CLI
「文字コード・revision・atomic mutation」
  ↓
Windows-31J のまま安全に扱う
```

### 最後まで同じ入口

```text
search → read → update → verify
              revision を引き渡す
```

- 更新だけ通常の UTF-8 patch tool へ戻さない
- 分からない文字コードは勝手に推測しない
- 途中で変わっていたら上書きしない

## 役割分担・判断軸

| 要素 | 役割 |
| --- | --- |
| AI agent | 依頼内容を理解し、必要な操作を選ぶ |
| Agent Skill | 専用 CLI を選び、同じ経路を使い続ける入口 |
| CLI | 文字コード解決、rule、revision、atomic mutation、diagnostics |
| repository rule | Java / JSP など path ごとの文字コードを明示 |

### 守るもの

- 既存の文字コード
- BOM
- 改行
- 読取時の revision

### 限定条件

- すべての AI agent の問題ではなく、ある特定の agent ハーネスで起きた問題
- 普通の UTF-8 ファイルまで何でも専用 CLI に寄せない
- `v0.5.0`、記事作成時点ではベータ版
- ハーネス側が改善されれば、すぐに不要になるかもしれない

## 開発を完成へ運んだ要因

- GPT-5.6 Sol Ultra と対話し、仕様を一緒に整理
- 曖昧な境界を発見
- test で固定すべき契約を整理
- 重要で繊細な設計を、現実的な労力で完成へ

## グラレコ構図案

- 左: UTF-8 前提の道具から文字化けした Windows-31J ファイルへ向かう「困りごと」
- 中央: `Agent Skill` と `CLI` の二層でできた小さな橋。橋の上を `search → read → update → verify` が一方向に進む
- 右: 文字コード、BOM、改行、revision が守られた Java / JSP ファイルと、安心を示す盾
- 最も大きく見せる主図: AI agent と既存ファイルをつなぐ「小さな橋」
- みくくの表情・視線: 右側で少し心配そうだが安心した表情。中央の橋を見ている。物は持たない
- 吹き出し: 「あ、あの…最後まで同じ入口を使うのです…！」

## 正確性メモ

- 記事本文に明記された事実だけを使う
- 問題の主体を「すべての AI agent」に広げない
- Shift_JIS と Windows-31J を完全に同一の規格として説明しない
- GPT-5.6 Sol Ultra は開発工程の要因として小さく示し、主図より目立たせない
- test の数値を画像へ無理に詰め込まない
