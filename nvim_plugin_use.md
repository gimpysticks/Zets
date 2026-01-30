# Neovim AI Plugin Usage

## Installed AI Plugins

1. **Avante.nvim** (`yetone/avante.nvim`) - AI-powered coding assistant configured to use Gemini 2.5 Flash. Includes keybindings like `<leader>aa` for ask, `<leader>ae` for edit, and various diff management features.

2. **ChatGPT.nvim** (`jackMort/ChatGPT.nvim`) - OpenAI ChatGPT integration using the `gpt-4o-mini` model for both chat and code editing.

3. **Gemini.nvim** (`kiddos/gemini.nvim`) - Full-featured Gemini integration with code completion, hints, chat, instruction prompts (unit tests, code review, code explain), and task capabilities using `gemini-2.5-flash`.

4. **GMN.nvim** (`meinside/gmn.nvim`) - Another Gemini plugin configured to use `gemini-2.5-flash` with a 30-second timeout.

5. **nvim-wingman** (`haydenkz/nvim-wingman`) - Configured for Grok AI using the `grok-beta` model.

Additionally, **Copilot.lua** (`zbirenbaum/copilot.lua`) is listed as a dependency for Avante, though it's not configured as a standalone plugin.

## How to Use Avante

### Core Commands
- **`<leader>aa`** - Open Avante and ask a question about your code
- **`<leader>ae`** - Edit code with AI assistance
- **`<leader>ar`** - Refresh the AI response
- **`<C-s>`** - Submit your prompt

### Toggle Commands
- **`<leader>at`** - Toggle Avante sidebar on/off
- **`<leader>ad`** - Toggle debug mode
- **`<leader>ah`** - Toggle hints
- **`<leader>as`** - Toggle suggestions

### Diff Navigation (when reviewing AI changes)
- **`]x`** / **`[x`** - Next/previous conflict
- **`]]`** / **`[[`** - Jump to next/previous section
- **`co`** - Choose "ours" (keep your version)
- **`ct`** - Choose "theirs" (accept AI version)
- **`ca`** - Accept all AI changes
- **`cb`** - Keep both versions
- **`cc`** - Choose at cursor

### Suggestions (if enabled)
- **`<M-l>`** (Alt+L) - Accept suggestion
- **`<M-]>`** / **`<M-[>`** - Next/previous suggestion
- **`<C-]>`** - Dismiss suggestion

### How It Works
Avante opens a sidebar on the right (30% width) where you can chat with Gemini 2.5 Flash about your code. It won't auto-apply changes - you'll review and accept them manually using the diff commands above.

## Best Plugin for Midjourney Prompts

**ChatGPT.nvim** is best suited for creating Midjourney prompts because:

1. It uses `gpt-4o-mini`, which excels at creative writing tasks like prompt engineering
2. It has a dedicated chat interface that's ideal for iterative prompt refinement
3. You can have back-and-forth conversations to refine your prompts

**How to use it:**
- Use commands like `:ChatGPT` or `:ChatGPTEditWithInstructions`
- Ask it to generate, refine, or improve Midjourney prompts in the chat interface
- Use `<C-y>` to yank responses, `<C-n>` for new sessions

The other plugins (Avante, Gemini, GMN) are more focused on code-related tasks like completion, code review, and inline editing, making them less ideal for creative prompt generation.
