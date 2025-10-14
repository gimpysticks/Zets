---
title: Remove_Spaces_In_filenames
date: 2022-02-16 12:17
---
for f in *\ *; do mv "$f" "${f// /_}"; done
