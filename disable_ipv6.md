---
title: Disable IPV6
date: 2022-02-05 15:22
---
sysctl -w net.ipv6.conf.all.disable_ipv6=1
sysctl -w net.ipv6.conf.default.disable_ipv6=1

