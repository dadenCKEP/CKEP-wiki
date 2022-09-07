---
title: "top page"
date: 2019-12-18T16:13:53+09:00
draft: false
---

# dadenCKEP-wiki
各種設備や装備とそのセットアップやメンテナンスに関するチートシートやメモなど。  
以前はMediaWikiで管理していたものだが、Raspberry Pi上で運用していたためそこそこの頻度で障害が発生する上にバックアップとリカバリーの手間が非常にかかるため、hugo + GitHug Pagesに移行した。編集権限はGitHubで管理される。

## 管理の仕組み
GitHub repositoryの[dadenCKEP/CKEP-wiki](https://github.com/dadenCKEP/CKEP-wiki)を利用し、静的サイトジェネレータの[Hugo](https://gohugo.io/)を使ったサイトを[GitHub Pages](https://pages.github.com/)にて公開している。

### 各branchの役割
現在作成するrepositoryのGitHub Pagesは以前と多少仕様が違い、Sourceの選択肢は「masterの/」か「masterの/docs」のみになっているため、以下のような構成を取っている。
* `src/master` - 変換元コード。直接編集した際はここにpushする。デフォルトブランチ。
* `master` - 変換後コード。GitHub Actionsによってpushされるため直接操作はしない。GitHub PagesのSourceはこのブランチに設定されている。

### 更新作業の流れ
1. `src/master` branchに更新をpushする。
1. GitHub Actionsにより[変換用のスクリプト](https://github.com/dadenCKEP/CKEP-wiki/blob/src/master/.github/workflows/main.yml)が実行され、生成物が`master` branchへpushされる。
1. GitHub Pagesにより公開ページが更新される。

### その他
* Hugo用のテーマは[matcornic/hugo-theme-learn](https://github.com/matcornic/hugo-theme-learn/)を利用しており、サブモジュールとして読み込んでいる。
* GitHubはウェブサイト上でマークダウンエディタを利用してソースコードを編集できる。