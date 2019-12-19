---
title: "top page"
date: 2019-12-18T16:13:53+09:00
draft: false
---

# dadenCKEP-wiki

以前はMediaWikiで管理していたものですが、Raspberry Pi上で運用していたためそこそこの頻度で障害が発生する上にバックアップとリカバリーの手間が非常にかかるため、hugo + GitHug Pagesに移行しました。編集権限はGitHubで管理されます。

## 更新手順
1. src/master branchのcontent以下を更新
1. `hugo --gc --minify`
1. master branchにdocs以下をもってくる
    1. `git stash push -u`
    1. `checkout master`
    1. `rm docs -rf` (Windows: `rd /s docs`)
    1. `git stash pop stash@{0}`
    1. `git add docs`
    1. `git commit -m "generated contents"`
    1. `git push`

GitHub Actionsでできそうだけどうまく動かなかったので目処が立つまでは手動で行う。