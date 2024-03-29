---
title: "Software"
date: 2021-01-05T15:44:41+09:00
draft: false
---
常用しているソフトウェアとそのDL先の一覧。セットアップ時に参考にしつつ更新する。

## エディタ
* Visual Studio Code
  * https://code.visualstudio.com/
  * private reposに拡張機能のバックアップ・復元ツールあり
* Stirling
  * https://www.vector.co.jp/soft/win95/util/se079072.html
  * バイナリエディタ。
* ImHex
  * https://github.com/WerWolv/ImHex
  * 高機能バイナリエディタ。

## Git関連
* Git for Windows
  * https://gitforwindows.org/
  * インストール時のオプションはよく読んで設定すること。
* GitHub Desktop
  * https://desktop.github.com/
  * 連携等があるためVisual Studio Codeより後に入れること。

## 診断ツール
* CPU-Z
  * https://www.cpuid.com/softwares/cpu-z.html
* HWMonitor
  * https://www.cpuid.com/softwares/hwmonitor.html
  * PCの状態、特に温度や消費電力を確認する際に有用。
* GPU-Z
  * https://www.techpowerup.com/gpuz/
* OCCT
  * https://www.ocbase.com/
* CrystalDiskInfo
  * https://crystalmark.info/ja/software/crystaldiskinfo/
  * ストレージ監視ツール。スタートアップ&常駐必須。  
  異常の通知が出たらすぐにバックアップを取り始めれば間に合うかもしれない。

## 通信関連
* Putty
  * https://www.putty.org/
  * 更新されてない日本語版を使うのはやめよう
* WinSCP
  * https://winscp.net/eng/download.php
  * Puttyのプロファイルをインポートする機能がある。

## 通話関連
* Discord
  * https://discord.com/download
* Open Broadcaster Software
  * https://obsproject.com/ja/download
* VDRAW
  * https://sites.google.com/view/vdraw/vdraw
  * private reposに最新のVRMあり

## VRC関連
* Unity Hub
  * https://unity3d.com/jp/get-unity/download
* Substance Painter
  * Steamから導入
  * NASに各種素材があるので再インポートが必要
* Marvelous Designer
  * Steamから導入
* Blender
  * Steamから導入
  * [プラグインリスト](/3d/blender/plugin/)

## ゲーム
* Steam
  * https://store.steampowered.com/
    * 上部
  * Steamライブラリの場所に注意(バックアップから復元できるが手動で認識させる)
* Epic Game Launcher
  * https://www.epicgames.com/store/ja/
    * 右上
* Battle.net Desktop App
  * https://www.blizzard.com/ja-jp/download/

## その他
* WinMerge
  * https://winmerge.org/downloads/?lang=ja
  * 差分ツール。プラグインを使用することでExcelファイル等の比較も可能。
* PowerToys
  * https://github.com/microsoft/PowerToys/releases
  * 複合ツール。FancyZonesやPowerRename、PowerToys Runが便利。
* DevToys
  * https://github.com/veler/DevToys
  * 複合ツール。デベロッパーのためのスイスアーミーナイフ、というキャッチフレーズの通り、PowerToysより開発者向けのツールが多い。
* FastCopy
  * https://fastcopy.jp/
  * ファイルコピー・バックアップ・削除ツール。デバイスごとのチューニングがある他、ベリファイや時間予測も可能。
* SD Card Formatter
  * https://www.sdcard.org/jp/downloads/formatter/
  * パーティション割ってあったりWindowsで認識できないシステムが書いてあったりする場合はこれを使って初期化する。
* Win32 Disk Imager
  * https://sourceforge.net/projects/win32diskimager/
  * SDカードのディスクイメージを読み書きするツール。
* Audacity
  * https://www.audacityteam.org/download/windows/
  * 波形を見たり解析をしたりするやつ。特殊な条件下での再生もこれを使う。
* Hugo
  * https://github.com/gohugoio/hugo/releases
  * 静的サイトジェネレータ
  * wiki編集の際のプレビューができるのでローカルにも置く。
* ImageMagick
  * https://imagemagick.org/script/download.php
  * コマンドラインから使用できる万能の画像加工ツール
  * 旧コマンドは面倒なことになるので辞めよう。
  * ffmpegを内蔵しているのでffmpegを同時に使用する場合はパスを通す順番に注意
* Media Player Classic Black Edition
  * https://sourceforge.net/projects/mpcbe/
  * Media Player Classicの後継。多機能。
  * コマンドラインから操作できるが手動でパスを通しておく必要がある。
* QuickViewer
  * https://kanryu.github.io/quickviewer/index-ja
  * zip等のアーカイブを直接読み込みできる高速画像ビュワー
* Rapture
  * http://www.knystudio.net/rapture.html
  * 使いやすいキャプチャツール
* ScreenToGif
  * https://www.screentogif.com/downloads
  * 使いやすい動画キャプチャツール(短時間用)
    * 長時間キャプチャはOBSとかを使う
* 7-Zip
  * https://sevenzip.osdn.jp/
  * 一番使いやすくて無難なアーカイバ。
  * シェル拡張に圧縮・展開だけでなくハッシュの計算もできる。
* DiskInfo
  * https://www.vector.co.jp/soft/winnt/util/se475617.html
  * フォルダごとの専有容量を再帰的に解析できるツール。
  * ドライブの容量が不自然に少なくなったらこれで調べる。
* Audio Router
  * https://github.com/audiorouterdev/audio-router
  * アプリケーションごとにオーディオ出力先デバイスを指定できるツール。
* Touch Portal
  * https://www.touch-portal.com/
  * スマホをStream Deckみたいにするツール。
* リンク作成シェル拡張 Ver.1.55 for Windows
  * https://github.com/kobake/lnhdr
  * エクスプローラ上にてシンボリックリンク関連の機能を拡張するツール。
* yt-dlp
  * https://github.com/yt-dlp/yt-dlp
  * youtube-dlのフォーク。youtube-dlの最新版を取り込みながら多数のパッチを当てている。
  * ffmpegを使用するので導入しておくとよい。
* ffmpeg
  * https://www.ffmpeg.org/
  * 動画と音声を扱う汎用ソフト。
* drawio-desktop
  * https://github.com/jgraph/drawio-desktop
  * https://www.diagrams.net/
  * 図を作成するツールであるdraw.ioのデスクトップ版。
  * オリジナルであるブラウザ版やChrome拡張版、VSCode拡張まである。
  * ファイルがテキストベースなので扱いやすい。
