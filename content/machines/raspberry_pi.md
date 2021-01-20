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
  * ピンヘッダがないほう。取り扱いが非常に少ない。[Prusa i3 MK3S]({{< ref "/Digital_Fabrication/3D_Printer/Prusa_i3_MK3S.md" >}})とかに使う。
  * スイッチサイエンス: https://www.switch-science.com/catalog/3200/
* Raspberry Pi Zero WH
  * ピンヘッダがあるほう。特に理由がなければこちらのほうが入手性が良い。
  * 秋月電子通商: https://akizukidenshi.com/catalog/g/gM-12961/
  * スイッチサイエンス: https://www.switch-science.com/catalog/3646/
  * 千石電商: https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-57LT
* Raspberry Pi 4とか3とかはバリエーションが多いためそのうち追記

### 周辺
* 追加購入
    * ヒートシンク: http://www.aitendo.com/product-list/1141/0/photo?num=100&img=120&available=1&sort=featured  
        * Raspberry Pi 3のSoCが14mm,RAMが12mm,LANコントローラが9mm
        * Raspberry Pi 4については要調査
    * ACアダプタ  
    ※注意: いっぱい余剰あるよ！！！買う前に確認して！！！
        * 安いほう: http://akizukidenshi.com/catalog/g/gM-10660/
        * 高いほう: http://akizukidenshi.com/catalog/g/gM-06238/
        * 分岐ケーブル(安いほう): https://akizukidenshi.com/catalog/g/gC-06723/
        * 分岐ケーブル(高いほう): https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=EEHD-0A6P
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
* [https://www.raspberrypi.org/downloads/](https://www.raspberrypi.org/downloads/)からimageをDL
* 念のため[SD Memory Card Formatter](https://www.sdcard.org/jp/downloads/formatter/)で消去して[Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/)で書き込み
* `/boot/ssh` というファイルを作成する。  
これがあるとデフォルトでSSHが有効になりディスプレイなしセットアップが可能。
* LANケーブルを接続して電源を接続。
* ルーターの管理画面からMACアドレスが`B8:27:EB`から始まるDHCPで割り当てられてるっぽい新規のデバイスを探す。
  * `Raspberry Pi Foundation` の割り当て。`DC:A6:32`, `E4:5F:01`もあるらしいが未確認。
* とりあえずルータ側から固定IPを振る。このwikiにメモするとよい。
* `sudo raspi-config` から一通り設定
  * hostname周辺を変更してる場合は再起動
* `sudo apt-get update` と `sudo apt-get upgrade`
* `sudo apt-get install vim`
* IPを固定してhostnameを設定(Jessie以降とそれより前で違う)
  * 参考(Jessie以降): https://www.raspberrypi.org/forums/viewtopic.php?t=140252
* `daden`ユーザを追加
  * `$sudo adduser daden`
* `daden`を`sudo`に追加
  * `$sudo gpasswd -a daden sudo`
* `pi`はnopasswdなので必要に応じて削除か`visudo`で後処理(最近のバージョンはnopasswdじゃない？)
  * `$sudo userdel -r pi`
  * `$sudo visudo`
* microSDの寿命を気にするなら `/var/log` とかをtmpfs上に構成
  * 参考1: https://curecode.jp/tech/raspberrypi-ramdisk/
  * 参考2: [https://www.angelcurio.com/raspberrypi/Raspberry Pi/各種設定/log,tmpのオンメモリ(tmpfs)化](https://www.angelcurio.com/raspberrypi/?Raspberry%20Pi/%E5%90%84%E7%A8%AE%E8%A8%AD%E5%AE%9A/log%2Ctmp%E3%81%AE%E3%82%AA%E3%83%B3%E3%83%A1%E3%83%A2%E3%83%AA%28tmpfs%29%E5%8C%96)
* 鍵交換

## オプション編
* m2xに本体温度を送信するスクリプト(`m2x.sh`)を`/home/daden/bin`に置いてcronを設定
  * m2xは無料サービスの提供を取りやめた。移行先検討中。
* 同一・あるいは近い型番だと外見上の識別が難しく、ラック等へ格納する前に付箋でIP等を書いておかないと、後で見分けがつかなくてどれの電源を切ればいいかわからなくなる。
