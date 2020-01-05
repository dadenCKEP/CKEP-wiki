---
title: "Google Fit"
date: 2020-01-04T13:06:46+09:00
draft: false
---

## 概要
* 公式アプリ: [Google Fit](https://play.google.com/store/apps/details?id=com.google.android.apps.fitness)
* 紹介ページ: [Google Fit](https://www.google.com/fit/)  
以前はウェブインターフェースがあったが廃止された
* 公式ドキュメント: [The Google Fit SDK](https://developers.google.com/fit)

## Google Fitの思想(勝手な予想)について
Google Fitは他のデバイスメーカー・アプリメーカーの自社プラットフォームとは明確に意図(思想)が違い、「自社のデバイスのデータを集積して利用するのが主な目的で、ついでに連携先のプラットフォームに送信・連携先のデータを利用する」のではなく、「Google Fitを利用するアプリは、全てのデータをGoogle Fitに保存し、必要に応じて全てのデータをGoogle Fitから取り出して利用する」という意図がある。
つまり、「可能な限りすべてのデータを保存し、可能な限りGoogle Fit上のデータを利用する」必要がある。

例えば身長・体重のデータはGoogle Fit上に保存できるため、「設定欄で身長・体重をプラットフォーム独自の設定として利用できる」というのは不適切である。(参考: [Fitness Data Types | Google Fit](https://developers.google.com/fit/android/data-types) )
意図に合わせるのであれば、「身長・体重を一定期間ごとにGoogle Fitから取得して利用し、必要であれば現在の身長・体重の値をGoogle Fitに手動送信して初期値とすることができる」とすべきである。

## 上記を踏まえて手持ちのデバイスのデータを整理して格納する
(検討中)