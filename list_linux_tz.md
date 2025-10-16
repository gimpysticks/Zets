---
title: List_Linux_TZ
date: 2022-05-09 00:44
---
list all time zones
cd /usr/share/zoneinfo/posix && find * -type f -or -type l | sort

Diaplay crrent Time in TZ
TZ='Europe/Warsaw' date
