---
title: "Raspberry Pi"
date: 2019-12-19T14:45:53+09:00
draft: false
---

Raspberry Piのn回目のセットアップ用簡易ガイド  
毎回同じことやると漏れがありそうで怖い

## ハードウェア編
### 本体
* Raspberry Pi Zero W
  * ピンヘッダがないほう。取り扱いが非常に少ない。[Prusa i3 MK3S]({{< ref "/Digital_Fabricators/3D_Printer/Prusa_i3_MK3S.md" >}})とかに使う。
  * スイッチサイエンス: https://www.switch-science.com/catalog/3200/
* Raspberry Pi Zero WH
  * ピンヘッダがあるほう。特に理由がなければこちらのほうが入手性が良い。
  * 秋月電子通商: https://akizukidenshi.com/catalog/g/gM-12961/
  * スイッチサイエンス: https://www.switch-science.com/catalog/3646/
  * 千石電商: https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-57LT
* Raspberry Pi 4とか3とかはバリレーションが多いためそのうち追記

### 周辺
* 追加購入
    * ヒートシンク: http://www.aitendo.com/product-list/1141/0/photo?num=100&img=120&available=1&sort=featured  
        * Raspberry Pi 3のSoCが14mm,RAMが12mm,LANコントローラが9mm
    * ACアダプタ  
        * 安いほう: http://akizukidenshi.com/catalog/g/gM-10660/
        * 高いほう: http://akizukidenshi.com/catalog/g/gM-06238/
        * 分岐ケーブル: https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-0A6P
    * 拡張基板: http://akizukidenshi.com/catalog/g/gP-11073/
        * ピンソケット: http://akizukidenshi.com/catalog/g/gC-00085/  
        スタック用もあるらしい: http://akizukidenshi.com/catalog/g/gC-10702/
        * DCジャック: http://akizukidenshi.com/catalog/g/gC-09408/
    * スタック用のスペーサー: M2.6
        * ピンヘッダ+ピンソケットが11
        * 千石電商にあるのはこれだけ: https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-4UUR
        * それ以外は廣杉計器から直接買う (例: https://www.hirosugi-net.co.jp/shop/g/g514/)

適当にはんだ付けして利用。Raspberry Pi2-4まで同じようにできるはず。

## セットアップ編
Raspbian Stretch時点でのフロー。更新の際に一部変更になることがある。
過去にあった変更としては、hostnameの設定方法やIP固定の手順などが変更になっている。
1. [https://www.raspberrypi.org/downloads/](https://www.raspberrypi.org/downloads/)からimageをDL
1. 念のため[SD Memory Card Formatter](https://www.sdcard.org/jp/downloads/formatter/)で消去して[Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/)で書き込み
1. `/boot/ssh` というファイルを作成する。  
これがあるとデフォルトでSSHが有効になりディスプレイなしセットアップが可能。
1. LANケーブルを接続して電源を接続。
1. ルーターの管理画面からMACアドレスが`B8:27:EB`で始まる新規のデバイスを探す。
1. とりあえずルータ側から固定IPを振る。このwikiにメモするとよい。
1. `sudo raspi-config` から一通り設定
1. `sudo apt-get update` と `sudo apt-get upgrade`
1. `sudo apt-get install vim`
1. IPを固定してhostnameを設定(OSのバージョンによって操作が違う)
1. sudoなユーザを追加し`pi`を削除
1. `pi`はnopasswdなので必要に応じて`visudo`で後処理
1. 鍵交換

## オプション編
1. m2xに本体温度を送信するスクリプト(`m2x.sh`)を`/home/daden/bin`に置いてcronを設定
  * m2xは無料サービスの提供を取りやめた。移行先検討中。
1. ラックに格納する前に付箋でIP等を書いておかないと後で見分けがつかなくてどれの電源を切ればいいかわからなくなる
