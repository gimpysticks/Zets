---
title: fd_sorted_file_list
date: 2023-01-31 20:05
---

fd . -t f -H --sort time --order newest-first

Explanation:

fd .: search for files in the current directory.
-t f: search for only files (not directories).
-H: follow symbolic links.
--sort time: sort by modification time.
--order newest-first: sort the results in descending order (newest first).
