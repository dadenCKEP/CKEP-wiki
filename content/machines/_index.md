---
title: "Machines"
date: 2019-12-18T22:46:13+09:00
draft: falsel
---
自宅設備のメモなど。これを保管するためにwikiがあるみたいなところがある。各セットアップの情報などは個別にまとめる(予定)。

## 外部
* cloudflare
    * ドメイン  
    ckep.info以下全部一括管理

## 自宅
* ルーター・モデム等
  * RT-AC68U(192.168.0.2)(192.168.12.1)
    * ルーター
* ワンボードコンピュータ
  * Raspberry Pi 2 B(192.168.11.10)
    * hostname: allocator
    * eth0: B8:27:EB:XX:XX:44
    * 2021-05-07-raspios-buster-armhf-lite.img
    * リバースプロキシ
    * 常時稼働
  * Raspberry Pi 3 B(192.168.11.12)
    * hostname: web-server
    * eth0: B8:27:EB:XX:XX:D1
    * wlan0: B8:27:EB:XX:XX:84
    * Node-RED
    * Home Assistant
      * エラーが出てて怪しい
    * 常時稼働
  * Raspberry Pi 3 B(192.168.11.14)
    * hostname: ubuntu
    * eth0: B8:27:EB:XX:XX:49
    * wlan0: B8:27:EB:XX:XX:1C
    * 停止中
  * Raspberry Pi 4B 8GB(192.168.11.19)
    * hostname: power
    * eth0: DC:A6:32:XX:XX:20
    * ubuntu-20.04.1-preinstalled-server-arm64+raspi.img
    * 常時稼働
    * InfluxDB
    * Grafana
  * Raspberry Pi Zero WH
    * 停止中
  * Pine A64+2GB(192.168.11.15)
    * hostname: streamer
    * eth0: 
    * ストリーミング用
    * メモ
      * OS: https://wiki.pine64.org/wiki/Pine_A64_Software_Release#Armbian
        * Armbian: https://www.armbian.com/pine64/
      * youtube-dl: https://github.com/ytdl-org/youtube-dl
      * NGINX-based Media Streaming Server: https://github.com/arut/nginx-rtmp-module
  * Raspberry Pi 3 B(192.168.11.13)
    * hostname: ranchan
    * 用途未定 ディスプレイを付けてある
    * 停止中
  * サブPC(192.168.11.20)
    * hostname: ubuntu-game
    * ゲームサーバー用。元メインPCだったもの。
    * [Minecraft advanced_vanilla](/games/minecraft/advanced_vanilla)
* NAS
  * [ReadyNAS 212](/machines/readynas212)(192.168.11.51)  
    * 各種バックアップ用
* その他
  * Philips Hue ブリッジ (192.168.11.50)
    * 00:17:88:XX:XX:13
    * ランプ1(メインルーム/室内中央)
    * ランプ2(メインルーム/電気スタンド)
  * メインPC(192.168.11.30)
  * Google Nest Hub
  * Nature Remo mini
  * OctoPrint(192.168.11.210)
    * Prusa i3 MK3S
  * HS105
    * 4台くらいある
    * N極対応のプラグしか使用できないため、この延長ケーブルと併用すると使いやすい。  
      https://www.amazon.co.jp/gp/product/B01N9BX7PI/

## 実家
* ルーター・モデム等
  * F660A(192.168.0.1)(グローバルIP不定)  
    モデム 貸与だと思う  
    ポートフォワーディングのみ設定(HTTP,VPN等) 他はほぼスルー
  * Archer C3150(192.168.0.3)(192.168.11.1)  
* サーバー
  * HP Compaq Business Desktop dc5800 SF/CT(有線: 192.168.11.17)(86-server)  
    http://jp.ext.hp.com/products/desktops/old/dc5800sf_ct/core_duo_model.html (リンク切れ)  
    ジャンクショップで購入。E7300が載ってる版。メモリだけ差し替わってた。HDDは差し替えた。  
    x86の鯖でしかできない実験用。当分はdockerとelastic stack関係が載ると思う。現在停止中。
  * 自作機(無線: 192.168.11.31)  
    以前のメイン機。CentOSが入れてある。主にゲームサーバー用。最近全く使っていない。
