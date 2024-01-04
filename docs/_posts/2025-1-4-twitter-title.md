---
layout: category-post
title: "メモ: Twitterのタブタイトル改善"
excerpt: "Twitterのタブタイトルが分かりにくくて不便なので、Firefoxアドオンを使って改変したときのメモ"
description: "Twitterのタブタイトルが分かりにくくて不便なので、Firefoxアドオンを使って改変したときのメモ"
author: "秋山翠花"
image: https://sueakiyama.github.io/images/20230830_2.JPG
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

**「Xユーザー」しか見えないんだが!?**

X (Twitter) ユーザーなのはアイコンで分かるので、「Xユーザー」というのは一番要らない情報なんですが、なぜかこれだけ表示される状態になっています。最悪ですね。

というわけで、この記事では、Twitterのタブ・タイトルを改変することで、もう少しばかり利便性を高めていこうと思います。

## 解決策

みなさんがどのブラウザを使っているかは知りませんが、私は[Firefox](https://www.mozilla.org/ja/firefox/new/) (厳密にいえば、[Firefox Nightly](https://www.mozilla.org/ja/firefox/channel/desktop/)) を使っています。みなさんもFirefoxを使うべきです。

Firefox の優れた点として、~~Google傘下でないこと~~ 多くのアドオンが使えることが挙げられます。(数年前のアップデートで、かなり減ったとはいえ!)

今回も、こうしたアドオンを活用していきます。今回使ったのは Tab Retitle というアドオン。タブの名前を変更してくれます。正規表現も使えます。やったね。

- [Tab Retitle (Firefox Browser Add-ons)](https://addons.mozilla.org/ja/firefox/addon/tab-retitle/)
- [Tab Retitle (chromeウェブストア)](https://chromewebstore.google.com/detail/tab-retitle/hilgambgdpjgljhjdaccadahckpdiapo) ←Chrome版もありました……

これを使って、Twitterのタブ・タイトルを「(ユーザー名)『(ツイート内容)』」にしていこうと思います。





