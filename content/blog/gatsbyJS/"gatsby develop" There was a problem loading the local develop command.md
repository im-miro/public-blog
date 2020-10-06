---
title: 'There was a problem loading the local develop command.'
date: 2020-10-6 21:46:13
category: 'gatsbyJS'
draft: false
---

# There was a problem loading the local develop command

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
$ gatsby develop

 ERROR

There was a problem loading the local develop command. Gatsby may not be installed in your site's "node_modules" directory. Perhaps you need to run "npm install"? You might need to delete your "package-lock.json" as well.
```

## RESOLUTION

```
npm install
```

## comment

再発性あり、gatsby develop 後に時々起こる。

ERROR 通り npm install すればよい
