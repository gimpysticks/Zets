---
title: AI_plugin_commands
created: 2025-11-05
modified: 2025-11-05
---

# AI Plugin Commands in Neovim

This document lists the commands and keybindings for the AI-related Neovim plugins configured in your setup.

## 1. `ChatGPT.nvim` (jackMort/ChatGPT.nvim)

This plugin provides an interface to interact with OpenAI's ChatGPT.

### Commands for Code Editing and Actions:

*   `:ChatGPTEditWithInstructions`: Opens an interactive window to edit selected text or the entire buffer with instructions for ChatGPT.
*   `:ChatGPTRun [action]`: Executes specific predefined actions using ChatGPT on your code. Common actions include:
    *   `grammar_correction`
    *   `translate`
    *   `keywords`
    *   `docstring`
    *   `add_tests`
    *   `optimize_code`
    *   `summarize`
    *   `fix_bugs`
    *   `explain_code`
    *   `roxygen_edit`
    *   `code_readability_analysis`
*   `:ChatGPTActAs [persona]`: Instructs ChatGPT to adopt a specific persona.

### General Chat Window Keybindings (default, may be customized):

*   `<C-f>`: Cycles between chat window modes (centered or sticky to the right).
*   `<C-c>`: Closes the chat window.
*   `<C-p>`: Toggles the list of chat sessions.
*   `<C-u>`: Scrolls up the chat window.
*   `<C-d>`: Scrolls down the chat window.
*   `<C-k>`: Copies or yanks code from the last AI response.
*   `<C-n>`: Starts a new chat session.
*   `<C-r>`: Drafts a message without immediately submitting it to the server.
*   `<C-r>`: Switches between user and assistant roles to define a workflow.
*   `<C-s>`: Toggles the system message window.

## 2. `gemini.nvim` (kiddos/gemini.nvim)

This plugin integrates Google Gemini for various AI-assisted coding tasks. It primarily uses keybindings for core functionalities, but defines specific commands for instruction-based prompts.

### Commands for Instruction-based Prompts:

*   `:GeminiUnitTest`: Triggers the unit test generation prompt.
*   `:GeminiCodeReview`: Triggers the code review prompt.
*   `:GeminiCodeExplain`: Triggers the code explanation prompt.

### Keybindings (default, may be customized in `gemini.lua`):

*   `<S-Tab>` (for `insert_result_key`): Used to insert results for hints and completion.
*   `<Leader><Leader><Leader>g` (for `menu_key`): Likely opens a menu for instruction prompts.

## 3. `gmn.nvim` (meinside/gmn.nvim)

This plugin focuses on Google Gemini text generation and Git commit message generation.

### Text Generation Commands:

*   `:GeminiGenerate <<your prompt text here>>`: Generates text based on the provided prompt and inserts it at the current cursor position.
*   `:GeminiGenerateWithSearch <<your prompt which needs some searched results from google>>`: Generates text by incorporating Google web search results.
*   `:GeminiGenerateWithURLFetch <<your prompt which does something with <https://url1>, <https://url2> ...>>`: Generates text using content fetched from specified URLs.
*   `:'<,'>GeminiGenerate`: Uses visually selected text as a prompt to generate new text, replacing the selection.
*   `:'<,'>GeminiGenerate your prompt text here`: Combines visually selected text with an additional prompt to generate new text, replacing the selection.

### Git Commit Message Generation Commands:

*   `:GeminiGenerateGitCommitMessage`: Generates a Git commit message based on `git diff HEAD`, clears the buffer, and inserts the message.
*   `:'<,'>GeminiGenerateGitCommitMessage`: Generates a commit message from visually selected text and replaces the selection.
