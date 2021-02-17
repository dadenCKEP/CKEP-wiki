---
title: "Setup"
date: 2021-02-11T23:53:01+09:00
draft: false
---

## ユーザー側
### MultiMCの導入
[Fabric Wikiの該当項目を参照](https://fabricmc.net/wiki/player:tutorials:install_multimc:windows)

### ModPackの適用
MultiMCにxmlファイルを投げ込むと読み込まれる

## サーバー側
### 初期設定
* Ubuntu 20.04 Serverをインストール
* IP固定・通信確立
* `minecraft`ユーザーを作成
  ```bash
  sudo adduser minecraft
  ```

### 必要なパッケージの導入
* 更新
  ```bash
  sudo apt update | apt upgrade -y
  ```
* OpenJDK11をインストール
  ```bash
  sudo apt install default-jdk
  ```
* もしもscreenかwgetが入っていないならインストール。
  ```bash
  sudo apt install wget screen
  ```

### 本体の設置
[Fabric Wikiの該当項目を参照](https://fabricmc.net/wiki/player:tutorials:install_server)

### ModPackの作成・更新
[Fabric Wikiの該当項目を参照](https://fabricmc.net/wiki/tutorial:mcupdater_modpacks)
