---
layout: category-post
title: "メモ: Twitterのタブタイトル改善"
excerpt: "Twitterのタブタイトルが分かりにくくて不便なので、Firefoxアドオンを使って改変したときのメモ"
description: "Twitterのタブタイトルが分かりにくくて不便なので、Firefoxアドオンを使って改変したときのメモ"
author: "秋山翠花"
image: https://sueakiyama.github.io/images/20240104_3.png
---

## はじめに

あけましておめでとうございます!　初音ミクこと、秋山翠花です。

突然ですが、みなさんは [Twitter](https://twitter.com) を使いますか?　え、使ってる?　やめた方がいいですよ、あんなSNS。

ところで、最近 (と言っても半年前とかだと思いますが) Twitter のタイトル表記の仕様が変わりましたね。

- 旧: 〇〇さんは Twitter を使っています「(ツイート内容)」
- 新: Xユーザーの〇〇さん:「(ツイート内容)」

![新表記のTwitterタイトル](https://sueakiyama.github.io/images/20240104_0.png)  
新表記のTwitterタイトル。

まあ、大した変更ではないし、タブにある程度の幅があれば、欲しい情報 (ユーザー名とか) はこれまで通り手に入るのですが。

ところが、タブをたくさん開いたりして、各タブの幅が狭くなると……

![タブの幅が狭い場合](https://sueakiyama.github.io/images/20240104_1.png)  

**「Xユー」しか見えないんだが!?**

X (Twitter) ユーザーなのはアイコンで分かるので、「Xユーザー」というのは一番要らない情報なんですが、なぜかこれだけ表示される状態になっています。最悪ですね。

というわけで、この記事では、Twitterのタブ・タイトルを改変することで、もう少しばかり利便性を高めていこうと思います。

## 解決策

みなさんがどのブラウザを使っているかは知りませんが、私は[Firefox](https://www.mozilla.org/ja/firefox/new/) (厳密にいえば、[Firefox Nightly](https://www.mozilla.org/ja/firefox/channel/desktop/)) を使っています。みなさんもFirefoxを使うべきです。

Firefox の優れた点として、~~Google傘下でないこと~~ 多くのアドオンが使えることが挙げられます。(数年前のアップデートで、かなり減ったとはいえ!)

今回も、こうしたアドオンを活用していきます。今回使ったのは Tab Retitle というアドオン。タブの名前を変更してくれます。正規表現も使えます。やったね。

- [Tab ReTitle (Firefox Browser Add-ons)](https://addons.mozilla.org/ja/firefox/addon/tab-retitle/)
- [Tab ReTitle (chromeウェブストア)](https://chromewebstore.google.com/detail/tab-retitle/hilgambgdpjgljhjdaccadahckpdiapo) ←Chrome版もありました……泣

これを使って、Twitterのタブ・タイトルを「(ユーザー名)『(ツイート内容)』」にしていこうと思います。

### 手順

1. まず、アドオンをインストールします。
2. アドオンの管理ページ (Firefox なら、```about:addons```) に移動し、"Tab ReTitle"→「オプション」→"ADVANCED"→"Beta Feature: Add Your Own URL Pattern"に進みます。
![設定画面](https://sueakiyama.github.io/images/20240104_2.png)  
3. 設定画面の"URL Pattern"に```*twitter\.com/.*/status/.*```と入力、"New Title"に```/Xユーザーの(.*)さん:(.*)/$1$2/```と入力し、確定。

### 解説?

今回使った機能 "Add Your Own URL Pattern" は、URLが特定のパターンに一致するページにおいてのみ、タイトルを変更する、というものです。

私も最初は、デフォルトで用意されている、ドメイン単位 (```twitter.com``` すべて) の制御を試みたのですが、ツイート (```twitter.com/*/status/*```) 以外のページ (例えば、通知や設定など) でエラーを吐いたり (検索文字列に一致する部分がないので、当然ではありますが)、表示が壊れたりしたので断念。試行錯誤の末、"Add Your Own URL Pattern" 機能にたどり着きました。(最初から調べておけって?　はい……)

では、設定欄に入力した文字列の解説を、簡単にしていきます。

まず、"URL Pattern" 欄に入力した```*twitter\.com/.*/status/.*```について。これは大したことをしていなくて、先頭と末尾の```*```は任意の文字 (これは正規表現ではなく、このアドオン独自の要請です)、```\.```は、本来検索したかった```.```が**メタ文字** (正規表現で特殊な意味を持つ文字) だったので、```\```で**エスケープ**しています。```.*```は、(ざっくり言うと) 任意の数の任意の文字を表します。詳しくは、後に示す参考文献を見ていただけると……

次に、"New Title"欄の```/Xユーザーの(.*)さん:(.*)/$1$2/```をご覧ください。ここでは、Tab ReTitleの構文に従い、```/(検索ルール)/(置換ルール)/(フラッグ)```の順に記述しています。

検索ルールで使っている記号は、"URL Pattern" 欄で使ったものと同じです。置換ルールにおける```$1```などは、検索ルールに従って抽出された変数です。最初に抽出されたものが```$1```、次に抽出されたものが```$2```です。つまり、例えば「Xユーザーの秋山翠花さん:『ショタ足立レイ』」というタイトルがあったとき、```$1```は「秋山翠花」、```$2```は「『ショタ足立レイ』」となり、結果として表示されるタイトルは「秋山翠花『ショタ足立レイ』」となります。

![使用後](https://sueakiyama.github.io/images/20240104_3.png)  

このようにすると、求める結果が得られるはず……たぶん。

## おわりに

こんなことしてる暇があったらコミケレポを書けって?　うるせえ! 泣

## 参考文献

- [サルにもわかる正規表現入門](https://userweb.mnet.ne.jp/nakama/)
- [正規表現あれこれ｜Qiita](https://qiita.com/ikedams/items/12d1127056cdf4f0eea5)

## 投げ銭にかえて

私に投げ銭したい、という稀有な方は、代わりにこちらへ募金しておいてください。

- [令和6年能登半島地震 緊急支援募金（Yahoo!基金）](https://donation.yahoo.co.jp/detail/1630064/)
