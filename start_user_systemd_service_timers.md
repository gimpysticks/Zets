---
title: Start_User_systemd_service_timers
date: 2023-07-02 21:53
---
--Enable the service
systemctl --user enable service.service

--Start the service
systemctl --user start service.service

--Enable the timer
systemctl --user enable timer.timer

--Start the timer
systemctl --user start timer.timer

