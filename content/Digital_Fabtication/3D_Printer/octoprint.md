---
title: "OctoPrint"
date: 2020-09-22T00:19:16+09:00
draft: false
---

OctoPrintは多くの3Dプリンタに対応しているWebインターフェイス。
[OctoPrint.org](https://octoprint.org/)

## Prusa i3 MK3Sでの使用
### インストール
この辺を参考にする  
https://help.prusa3d.com/en/category/octoprint_249

どハマリポイントとして、Raspberry Pi Zero Wで使用する場合はGPIO経由での通信になるのだがraspi-configにてSerialの設定をNo→Yesにしないと正しく通信できない。  
どうもモジュールが内部的に2個ある？らしい。情報が少なくてよくわからなかった。

## プラグイン
(良さそうなプラグインがいくつかあるらしい。調査中)
