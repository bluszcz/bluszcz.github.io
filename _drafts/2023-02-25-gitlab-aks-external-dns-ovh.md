---
layout: single
title:  "Git daemon with WSL2"
date:   2023-02-21 06:00:00 +0100
categories: development git
---


`git daemon --verbose --base-path=. --export-all --reuseaddr --informative-errors --verbose --listen=0.0.0.0`

`netsh interface portproxy add v4tov4 listenport=9418 listenaddress=0.0.0.0 connectport=9418 connectaddress=172.28.209.191 `


`git clone git://192.168.1.12/mysql-backup/`

