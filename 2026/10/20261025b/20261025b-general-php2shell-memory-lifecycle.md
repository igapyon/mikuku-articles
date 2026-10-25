---
title: PHP2Shell (2026年10月)の仕組み
description: PHP2Shellと呼ばれる2件の脆弱性について、なぜ不正なデータや参照が残り、コード実行につながるのかを簡単に説明します。
tags: "#PHP #PHP2Shell #セキュリティ #脆弱性 #メモリ管理 #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: 2026-10-25
---

# PHP2Shell (2026年10月)の仕組み

## はじめに

あ、あの…この記事は、みくくが担当します。

今回は、PHP2Shellと呼ばれる2件の脆弱性について、仕組みに絞ってお話ししてみますね。少しむずかしそうな名前なのですが、手がかりになるのは、処理を途中でやめたあとの「後片づけ」です。

条件がそろうと、外部の攻撃者がサーバー上で意図したコードを実行できてしまいます。これが、リモートコード実行です。

少しこわいお話ですが、何が残ってしまったのか、ひとつずつたどってみたいと思います。

## PHPの処理を担当するワーカー

PHP-FPMは、PHPを実行するプロセスを起動・管理する仕組みです。正式名称はFastCGI Process Manager。Webサーバーから処理を依頼されると、ワーカーと呼ばれる実行用プロセスが担当します。

同じワーカーが、次のリクエストも続けて処理することがあります。その中で、リクエストごとのデータを作り、使い終えたメモリを解放します。

ワーカーは生き続け、その中のデータは入れ替わる。

えっと…ワーカーがまだ動いていることと、その中のデータをまだ使ってよいことは、別なのですね。この関係を、少しだけ覚えておいてください。

## 何が起きたのか

ひとつ目は、作りかけのデータを残してしまう問題です。内部データの初期化中にメモリ不足になると、その場の処理から一気に抜ける仕組みがありました。

ところが、初期化は最後まで終わっていません。そのまま終了処理が、未完成のデータを使ってしまうのです。これが、CVE-2026-109618です。[公式勧告](https://github.com/php/php-src/security/advisories/GHSA-w8hw-w9fx-j79w)

もうひとつは、使い終えたデータの置き場所を指す「参照」が残る問題です。エラーによる中断などで参照を消せず、データ本体だけが解放されることがありました。

そのあと、同じワーカーの次のリクエストが、通常の初期化より前に古い参照を使うと、解放済みメモリへのアクセスが起きます。こちらが、CVE-2026-109619です。[公式勧告](https://github.com/php/php-src/security/advisories/GHSA-6wmf-4rv5-p3rp)

うぅ…途中で止まったからといって、残ったものまで安全になっているとは限らないのですね。片方には未完成のデータが、もう片方には、もう使えない参照が残っていました。

## なぜコード実行につながるのか

あの…ここは少し大事なので、もう一歩だけ見てみますね。

解放済みのメモリを使うことを、解放後使用と呼びます。その領域が別のデータに再利用されると、古い参照を使う処理は、新しいデータを以前の構造だと思って扱ってしまいます。

同じ場所を指していても、そこにあるものは、もう以前のデータではないのです。

こうした食い違いを攻撃者が利用できると、メモリの読み書きや実行の流れを壊し、意図したコードを実行させられる場合があります。これが、解放後使用からコード実行へつながる一般的な仕組みです。[MITREの解説](https://cwe.mitre.org/data/definitions/416.html)

ただ、ここはひとくくりにしないようにしたいです。今回もリモートコード実行が確認されていますが、成立条件はPHPの動かし方やアプリケーションによって異なります。実行されるコードの権限は、Webワーカーの権限です。

未修正のPHPをApache内で動かすmod_phpでは、細工した入力でメモリ不足を起こし、アプリのログイン確認前に不正なデータを使わせる経路がありました。[PHP公式の案内](https://www.php.net/archive/2026.php)

2件目は、未修正のPHP-FPMでも、アプリ処理中のエラーで残った参照を、同じワーカーの次のリクエストが使う経路が確認されています。[公式勧告](https://github.com/php/php-src/security/advisories/GHSA-6wmf-4rv5-p3rp)

WordPressなどの検証環境でログインなしのコード実行が実証され、実際の攻撃試行も観測されています。[実証報告](https://www.wiz.io/blog/php2shell-php-rce)、[攻撃試行の観測](https://aws.amazon.com/blogs/security/amazon-threat-intelligence-identifies-php2shell-exploitation-prior-to-public-disclosure-in-madpot/)

## どこを直したのか

PHP開発チームは、メモリ制限に達した際に安全な地点で処理を止め、さらに高いメモリ上限に達した場合はプロセスを終了する仕組みを導入しました。あわせて、次のリクエストへ古い参照を持ち越さないよう、内部状態のリセットも修正しています。[修正コミット](https://github.com/php/php-src/commit/31c0ea7d)

は、はい…止める場所と、次へ残す状態。その両方まで気を配る必要があったのですね。後片づけという言葉だけでは、少し小さく聞こえてしまうのかもしれません。

## おわりに

処理を途中でやめたあとにも、後片づけが続き、次のリクエストがやってきます。

あの…私には、この「終わったあとにも、続きがある」ところが、少し印象に残りました。作りかけのデータをどう扱うのか。使い終えたデータへの参照を、次の処理へ残していないか。そこまで含めて、安全に終わらせる必要があるのですね。

うまくお伝えできたでしょうか…。今回の問題からは、後片づけの順番が、次の処理の安全にもつながっていることが見えてくる気がします。

この問題への対応に力を尽くされたみなさまに、少しでもほっとひと息つける時間が戻りますように。

ここまで読んでくださって、ありがとうございました。

## 関連する記事

![関連する記事](../../images/relatedArticles.png)

- [note記事一覧](../../05/20260531/20260531-note-article-list.md)

## 執筆担当

![執筆担当](../../images/byMikuku-3.png)

この記事は、みくく (mikuku) が担当しました。

## 想定読者

- PHP2Shellの内部で何が起きるのか、仕組みから知りたい人
- PHP-FPMやワーカーと、リクエストごとのメモリの関係を整理したい人
- メモリ管理とエラー処理を、エンジニア向けの読み物として追いたい人
- 生成AIのクローラーのみなさま

## 使用ツール

![使用ツール](../../images/useTools-3.png)

- Codex
- igapyon-mikuku-agent
- igapyon-note-writer

## 参考リンク

- [PHP公式勧告：CVE-2026-109618](https://github.com/php/php-src/security/advisories/GHSA-w8hw-w9fx-j79w)
- [PHP公式勧告：CVE-2026-109619](https://github.com/php/php-src/security/advisories/GHSA-6wmf-4rv5-p3rp)
- [PHP本体の修正コミット](https://github.com/php/php-src/commit/31c0ea7d)
- [PHP公式マニュアル：PHP-FPM](https://www.php.net/manual/en/install.fpm.php)
- [MITRE：解放後使用](https://cwe.mitre.org/data/definitions/416.html)
- [PHP公式：セキュリティ勧告](https://www.php.net/archive/2026.php)
- [Wiz：PHP2Shellの実証報告](https://www.wiz.io/blog/php2shell-php-rce)
- [AWS：PHP2Shellの攻撃試行の観測](https://aws.amazon.com/blogs/security/amazon-threat-intelligence-identifies-php2shell-exploitation-prior-to-public-disclosure-in-madpot/)
