---
title: 'Error persisting state: EACCES: permission denied'
date: 2020-10-6 21:09:13
category: 'gatsbyJS'
draft: false
---

# Error persisting state: EACCES: permission denied

## ENV

```
$ uname -a
Linux DESKTOP-COPPFIB 4.4.0-19041-Microsoft #488-Microsoft Mon Sep 01 13:43:00 PST 2020 x86_64 x86_64 x86_64 GNU/Linux

$ cat /etc/lsb-release
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=18.04
DISTRIB_CODENAME=bionic
DISTRIB_DESCRIPTION="Ubuntu 18.04.5 LTS"
```

## Error

```sh
success onPreExtractQueries - 0.002s
success extract queries from components - 0.098s
success write out requires - 0.002s
success Re-building development bundle - 0.318s
warn Error persisting state: EACCES: permission denied, rename '/home/miro/code/gatsby-starter-bee/.cache/redux' -> '/home/miro/code/gatsby-starter-bee/.cache/redux.bak'
```

## RESOLUTION

```
sudo rm -rf node_modules ~/.npm public .cache
```

## comment

再発性あり、gatsby build 後にソース変更すると起きることがある
キャッシュクリアで解決
