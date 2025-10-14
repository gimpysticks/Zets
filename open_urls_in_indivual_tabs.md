---
title: Open_Urls_In_Indivual_tabs
date: 2023-03-23 21:56
---

#!/bin/bash

# Read the list of URLs from a file (one URL per line)
urls=$(cat urls.txt)

# Loop through the list of URLs and open each one in a new tab in Vivaldi
for url in $urls
do
  vivaldi --new-tab "$url"
done
