---
title: Start_Docker_Container_at_boot
date: 2023-03-10 10:11
---

sudo nano /etc/systemd/system/mycontainer.service

[Unit]
Description=My Docker container
Requires=docker.service
After=docker.service

[Service]
Restart=always
ExecStart=/usr/bin/docker start -a mycontainer
ExecStop=/usr/bin/docker stop -t 2 mycontainer

[Install]
WantedBy=default.target


sudo systemctl daemon-reload
