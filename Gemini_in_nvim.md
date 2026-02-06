---
created: 2026-01-06
---
That's a great workflow to master\! Using the Gemini CLI directly inside Neovim allows you to harness its power without leaving your editor, especially when you need to send code for analysis or insert generated code.

There are two primary ways to interact with the shell from within Neovim. The first is non-interactive (command-line mode), and the second is using the terminal buffer.

Here is an example for both, focusing on how you would send the contents of your current file to Gemini for review and then insert the suggestion.

-----

## 1\. 📝 Non-Interactive: Code Review and Insertion

This method is best for when you want to send a chunk of text or the entire buffer, get a response, and quickly insert the result into your file. It uses Neovim's built-in `:read` command with the external shell command (`!`).

### The Scenario: Review the current file for improvements.

| Command | Action | Description |
| :--- | :--- | :--- |
| **Piping Current Buffer** | `:%!cat` | `:%` selects the entire buffer, and `!cat` pipes it to `cat` (standard Unix utility). This command is *often* not strictly necessary but is a common pattern to ensure the buffer content is on standard input. |
| **Executing Gemini** | `| gemini -p "Review this code for efficiency and bugs. Suggest a refactoring if needed."` | The pipe (`|`) sends the output of `cat` (which is the file content) to Gemini. The `-p` flag passes your prompt. |
| **Inserting the Result** | `:read !cat % \| gemini -p "..."` | **The final, one-line command** runs the chain, and the `:read !` part ensures the output from the shell command (`gemini ...`) is read and inserted below your current line. |

### The Neovim Command:

With the file you want to review open, and your cursor on the line *where you want the AI's response to appear*, run:

```vim
:read !cat % \| gemini -p "Review the following code for efficiency and suggest a refactored version of the primary function."
```

**Note:**

  * `%` is the path of the current buffer.
  * `|` is the pipe character (you may need to escape it with `\` in Vim/Neovim's command line, or use `<bar>`). The search results confirm `\|` is the safer approach for the command line.
  * The output from Gemini will be inserted into your current buffer below the cursor.

-----

## 2\. 🖥️ Interactive: Dedicated Terminal Buffer

This method is better for longer, multi-turn conversations where you want a dedicated window to chat with Gemini without polluting your main code buffer.

### The Scenario: Debugging a tricky error over multiple prompts.

1.  **Open the Terminal Buffer:**
    Start the Gemini CLI in a split window.

    ```vim
    :split | terminal gemini
    ```

    *(If you use a plugin like `toggleterm.nvim`, you might simply use a keybinding like `<leader>gt` to open the terminal.)*

2.  **Enter Terminal Mode:**
    Press `i` to enter Terminal Mode so your keystrokes are sent to the shell/Gemini.

3.  **Start Interacting with Gemini:**
    You are now in the interactive Gemini shell. You can reference files directly using the `@` symbol:

    ```bash
    Ask: Fix the error in the `main` function in @my_file.py
    ```

4.  **Send a File to Gemini for Context:**
    If you want to send the entire content of your current code buffer to the open Gemini session for context, you can leave Terminal Mode (`<C-\><C-N>` or `ESC`), and use a modified command to pipe the file's content directly to the terminal buffer.

      * **Get the Terminal Buffer Number:** Find the buffer number of your new terminal (e.g., using `:ls`). Let's assume it's **4**.
      * **Send Code to the Terminal:**

    <!-- end list -->

    ```vim
    :call chansend(4, "My code is:\n" . join(getline(1, '$'), "\n") . "\n")
    ```

      * *This is more complex, but it sends the content of your current buffer (buffer 4) to the running Gemini session.*

The simplest and most immediate way to get code *from* Gemini *into* your buffer is **Method 1** using `:read !`. The next time you need to generate code, give that a try\!

Would you like a simplified Lua function to wrap the `:read !` command into a custom keybinding?
