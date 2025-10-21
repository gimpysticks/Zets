---
title: "Delete_Trailing_White_Space_On_Save"
date: 2021-10-19 19:12

autocmd BufWritePre * :%s/\s\+$//e
