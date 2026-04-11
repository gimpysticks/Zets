---
title: while_loop
created: 2026-03-01
---


To loop through a text file and run a command on every line in Bash, the most robust method is using a `while` loop combined with `read`.

### The Recommended Script

This approach handles spaces in URLs and ensures the file is read line-by-line correctly.

```bash
while IFS= read -r line; do
    yt-dlp "$line"
done < list.txt

```

---

### Why this works:

* **`IFS=`**: Prevents leading/trailing whitespace from being trimmed from the URL.
* **`read -r`**: Prevents backslashes from being interpreted as escape characters.
* **`"$line"`**: Quoting the variable is crucial; it ensures that if a URL contains special characters (like `&` or `?`), the shell doesn't misinterpret them.
* **`< list.txt`**: This redirects the content of your file into the loop.

### The "Quick & Dirty" One-Liner

If you are working directly in the terminal and your URLs don't have spaces, you can use this shorter version:

```bash
xargs -a list.txt -n 1 yt-dlp

```

> **Pro Tip:** If your `list.txt` contains a mix of URLs and comments (lines starting with `#`), you can skip them by adding a simple `grep` check:
> `grep -v '^#' list.txt | xargs -n 1 yt-dlp`

---

Would you like me to help you add specific `yt-dlp` flags to that loop, such as for choosing a file format or saving to a specific folder?
