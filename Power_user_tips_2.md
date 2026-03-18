---
created: 2026-03-18T23:22:32-04:00
modified: 2026-03-18T23:22:32-04:00
---

# Power user tips number two

# Linux Terminal Power User Tips

### 1. I/O Redirection & Pipes
* **`command > file`** : Redirects stdout to a file, overwriting it.
* **`command >> file`** : Appends stdout to a file instead of overwriting.
* **`command 2>&1`** : Merges stderr into stdout so both can be piped or redirected together.
* **`command | tee file`** : Pipes output to both a file *and* the terminal simultaneously.
* **`command1 | command2`** : Chains commands so the output of one feeds the input of the next.

### 2. Text Processing
* **`grep -r "pattern" .`** : Recursively searches for a pattern in all files under the current directory.
* **`grep -v "pattern"`** : Inverts the match — prints lines that do *not* contain the pattern.
* **`sed 's/old/new/g' file`** : Substitutes all occurrences of `old` with `new` in a file (non-destructive by default).
* **`sed -i 's/old/new/g' file`** : Same as above but edits the file in-place.
* **`awk '{print $2}' file`** : Prints the second whitespace-delimited field of every line.
* **`cut -d',' -f1 file`** : Cuts the first column from a comma-delimited file.
* **`sort | uniq -c | sort -rn`** : Classic pipeline: count unique lines and rank them by frequency.

### 3. Finding Files
* **`find . -name "*.log" -mtime -7`** : Finds `.log` files modified within the last 7 days.
* **`find . -type f -empty`** : Lists all empty files recursively from the current directory.
* **`find . -exec command {} \;`** : Runs a command on every file found.
* **`locate filename`** : Near-instant file lookup using a pre-built index (run `updatedb` to refresh).

### 4. Brace & Parameter Expansion
* **`{a,b,c}`** : Expands to multiple arguments (e.g., `cp file.txt{,.bak}` creates `file.txt.bak`).
* **`{1..10}`** : Generates a numeric sequence (e.g., `touch log_{1..5}.txt` creates 5 files).
* **`${var:-default}`** : Uses `default` if `$var` is unset or empty.
* **`${var%suffix}`** : Strips a trailing suffix from the value of `$var`.
* **`${#var}`** : Returns the length of the string stored in `$var`.

### 5. Keyboard Shortcuts (Readline)
* **`Ctrl + A`** : Jump to the beginning of the current line.
* **`Ctrl + E`** : Jump to the end of the current line.
* **`Ctrl + W`** : Delete the word immediately before the cursor.
* **`Ctrl + U`** : Delete everything from the cursor back to the beginning of the line.
* **`Ctrl + K`** : Delete everything from the cursor to the end of the line.
* **`Ctrl + L`** : Clear the screen (equivalent to `clear`).
* **`Ctrl + X Ctrl + E`** : Open the current command line in your `$EDITOR` for multi-line editing.

### 6. System Inspection
* **`lsof -i :PORT`** : Shows which process is listening on a given port.
* **`ss -tulnp`** : Lists all open TCP/UDP sockets with their associated processes (modern `netstat` replacement).
* **`ps aux --sort=-%mem`** : Lists all processes sorted by memory usage, highest first.
* **`du -sh * | sort -rh`** : Summarizes disk usage of items in the current directory, sorted largest first.
* **`df -h`** : Shows disk space usage for all mounted filesystems in human-readable form.

> **Pro-Tip:** Chain inspection commands with `watch` to monitor them live:
> `watch -n 2 'ss -tulnp'`
