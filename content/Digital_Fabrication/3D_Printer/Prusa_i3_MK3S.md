---
title: "Prusa i3 MK3S"
date: 2020-08-16T18:22:59+09:00
draft: false
---

## 概要
* Prusa i3 MK3S
  * https://reprap.org/wiki/Prusa_i3_MK3
  * https://www.prusa3d.jp/
  * キットが高いがクローンが大量にある
    * 例: https://ja.aliexpress.com/item/33022178159.html
    * 例2: https://ja.aliexpress.com/item/33020493926.html
      * 安い(送料込み4万程度で公式の半額相当)
  * 資料も多い

## V6
* V6はPrusa i3 MK3Sに使用されている汎用性の高いホットエンド。
  * Prusa i3 MK3Sのものはここから購入できる: https://e3d-online.com/products/prusa-v6-hotend
    * 通常のV6と一部互換がないので注意
  * 資料: https://e3d-online.dozuki.com/c/V6
    * 公式以外から購入したor修理などの場合は自力組み立てが必要。その際は上の資料を見る。
    * 動画もある: https://www.youtube.com/watch?v=gwNAMveHLmw

## カスタムパーツ
* Prusa MK3/MK3S Tool Holder
  * https://www.thingiverse.com/thing:3268830
  * 普通に便利。自分が使う工具に合わせてカスタマイズするといいかも。
  * これを合わせて使えるらしい。 [1.75mm Filament Clip - Universal (styled after 3D Solutech filament clips)](https://www.thingiverse.com/thing:3268797)
* Prusa i3 Mk3: Display Cover
  * https://www.thingiverse.com/thing:2933252
  * 説明を見るまで実用性に気づけなかった。夜にプリントする際、ディスプレイの光を遮ることができる。
  * 生成物が薄いため冷却前に剥がすと曲がる。あとベッドへの定着が悪いと曲がる。
* Prusa MK3S Reverse Bowden filament Sensor Cover
  * https://www.thingiverse.com/thing:3425397
  * Prusa i3 MK3SをReverse Bowdenに対応させるためのパーツ。
  * フィラメントを送り出す方式はDirect DriveとBowdenの2種類があり、BowdenとはギアでPTFEチューブにフィラメントを送り出すことでエクストルーダーにギアを搭載しない方式のこと。
  * Prusa i3 MK3SはDirect Drive方式なのだが、PTFEチューブからフィラメントを引っ張るのでReverse Bowden方式ということになる。
  * メリットとしてはスプールホルダーの位置によらずスムーズにフィラメントを取り出すことができる。
* Prusa i3 Mk3 Z-Tops with Reverse Bowden Mount Option
  * https://www.thingiverse.com/thing:2825557
  * Reverse BowdenのPTFEチューブを固定するエクストルーダー側じゃない方のパーツ。
  * 左右やクイック継ぎ手の径のバリエーションが充実しているのでこれを使用した。

## 便利な道具
* Bed Scraper/Print Removal Tool
  * https://www.thingiverse.com/thing:1345877
  * 生成物をはがすのではなくベッド上のゴミを取り除くのに便利。  
  生成物をはがすのはスチールベッドをはがして曲げたほうが早いし安全。
* Universal Filament Filter and Lubricator
  * https://www.thingiverse.com/thing:492067
  * フィラメントをスポンジで拭うフィルタ。ノズル径が小さいとわずかなゴミで詰まることがあるらしい。
* PTFE Cutting Tool 45° 60° 90°
  * https://www.thingiverse.com/thing:3749528
  * ホットエンドのPTFEチューブの切断を補助するツール。両端を真っ直ぐ切ることと先端の面取りを補助する。
  * ホットエンドやエクストルーダーの交換・改造をする際に元のエクストルーダーを分解する前に印刷しておく必要がある。

## 振動・騒音対策
* Seriously the BEST $2 3D printer upgrade!
  * https://www.youtube.com/watch?v=y08v6PY_7ak
  * 紹介記事: https://hackaday.com/2020/05/20/bricking-your-3d-printer-in-a-good-way/
  * 舗装ブロックと独立気泡フォーム(文中のclosed-cell packing foamに対応する日本語)によって
    格安で振動と騒音を軽減し品質を向上させるという研究。
  * 実際にホームセンターで30cm*30cmの舗装ブロック(わずかにサイズが足りなかったがゴム足を少し内側に移動してごまかした)
    と保護スポンジという名称で販売されていたゴムスポンジを利用して作成したところ、台への振動の伝播が多少軽減されたと思われる。
  * 副次的な効果だが重量が大幅に増加したことでプリンタ台自体の揺れが軽減された。これは非常に良かった。
  * コスト自体は非常に安いが、雨の中徒歩で5.5kgの舗装ブロックを手で持って帰るのは大変だった。
* How to build a simple, cheap enclosure for your 3D printer
  * https://blog.prusaprinters.org/cheap-simple-3d-printer-enclosure_7785/
  * IKEAの家具であるLACKシリーズのサイドテーブルを使って作成するエンクロージャ
  * コメント欄によると全ての部品を印刷するのに142時間が必要で、うち6つの部品は単体で15時間以上を要するため1週間以上確保すべきとのこと。
  * 印刷エリアの温度を一定に保つことで一部の材料は安定して印刷が可能になる。ただしPLAは軟化してしまうためドアを開けて印刷するべきだとのこと。
    * もちろん3Dプリンタの一部にPLAの部品を使うのも避けるべきだ。
  * アクリル板のせいで結構なコストがかかる。

## 資料
* Prusa i3 mk3s + mmu2s ようやく動く
  * http://ocean.opal.ne.jp/blog/?p=1647
* Original Prusa i3 MK3/S のアップグレードまとめ
  * https://satt99.hatenablog.com/entry/2020/01/13/124955
* Clone PRUSA 備忘録
  * http://www002.upp.so-net.ne.jp/hard-and-soft/Clone_Prusa/Clone_Prusa.html
* Prusa MK3sの簡単・便利・安価なアップグレード
  * https://qiita.com/yosuke_y2/items/2b5ef2cdee3d56fdbcfc
* Amazon欲しいものリスト
  * https://www.amazon.jp/hz/wishlist/ls/AMEIPAKCKW0R?tag=daden-22
  * 購入したものの個別レビューがわり。上記のリンクはAmazon.co.jpアソシエイトを使用しています。
