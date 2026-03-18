---
created: 2026-03-18T02:03:22-04:00
modified: 2026-03-18T02:04:01-04:00
---

# Power user tips number one

# Linux Terminal Power User Tips

### 1. Fast Directory Navigation
* **`cd -`** : Toggle back to the previous working directory (like a "back" button).
* **`pushd /path/`** : Moves to a new directory and adds the current one to a stack.
* **`popd`** : Returns you to the directory at the top of the stack.
* **`Alt + .`** : Automatically inserts the last argument from your previous command.

### 2. History & Correction
* **`Ctrl + R`** : Reverse-i-search. Type a keyword to find and cycle through your command history.
* **`!!`** : The "Bang-Bang" command. Represents the entire last command (e.g., `sudo !!`).

### 3. Process Management
* **`command &`** : Runs a process in the background, keeping the prompt open.
* **`Ctrl + Z`** : Suspends (pauses) a running foreground process.
* **`bg`** : Resumes a suspended process in the background.
* **`fg`** : Brings a background job back to the foreground.
* **`jobs`** : Lists all active background tasks in the current session.

### 4. Detaching Processes (`disown`)
* **`disown`** : Detaches the most recent background job from the shell so it survives after the terminal is closed.
* **`disown -a`** : Detaches all current background jobs.
* **`disown -h %1`** : Keeps the job in the list but tells the shell not to kill it on exit (SIGHUP).

> **Pro-Tip:** To ensure output isn't lost when detaching:
> `command > output.log 2>&1 & disown`
