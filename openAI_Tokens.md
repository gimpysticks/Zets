---
created: 2026-01-30
---
# OpenAI Tokens and NVim AI Plugins

## Date: 2026-01-30

## NVim AI Plugin Status

### Installed Plugins
All three AI plugins are properly installed and configured:

1. **Avante.nvim** (Gemini-powered) ✓
   - Provider: Google Gemini (gemini-2.5-flash)
   - Commands: `:AvanteAsk`, `:AvanteChat`, `:AvanteEdit`
   - Keybinds: `<leader>aa` (ask), `<leader>ae` (edit), `<leader>at` (toggle)

2. **ChatGPT.nvim** (OpenAI) ⚠️
   - Provider: OpenAI (gpt-4o-mini)
   - Commands: `:ChatGPT`, `:ChatGPTEditWithInstructions`
   - **Issue**: Quota exceeded - needs credits added

3. **Gemini.nvim** (Google Gemini) ✓
   - Provider: Google Gemini (gemini-2.5-flash)
   - Commands: `:GeminiChat`, `:GeminiCodeExplain`, `:GeminiCodeReview`, `:GeminiUnitTest`
   - Keybind: `<Leader><Leader><Leader>g` (instruction menu)
   - Status: Working perfectly

---

## OpenAI Quota Issue

### Problem
```
Error: "You exceeded your current quota, please check your plan and billing details."
Type: insufficient_quota
```

### Solution: Add Credits to OpenAI Account

#### Steps to Add Credits:

1. **Go to OpenAI Billing Page**
   ```bash
   xdg-open https://platform.openai.com/settings/organization/billing
   ```

2. **Add Payment Method**
   - Click "Add payment details" or "Payment methods"
   - Enter credit/debit card information

3. **Add Credits** (Two Options)
   
   **Option A: Auto-recharge (Recommended)**
   - Set up automatic recharge when balance gets low
   - Example: Add $10 when balance drops below $5
   
   **Option B: Manual top-up**
   - Click "Add to credit balance"
   - Choose amount ($5, $10, $50, etc.)
   - Confirm payment

4. **Check Current Usage**
   ```bash
   xdg-open https://platform.openai.com/usage
   ```

---

## OpenAI Pricing Reference

### gpt-4o-mini Model Costs:
- **Input**: $0.150 per 1M tokens (~$0.00015 per 1K tokens)
- **Output**: $0.600 per 1M tokens (~$0.0006 per 1K tokens)

### Typical Costs:
- **$5** = ~3,000-10,000 API calls (depending on message length)
- **$10** = ~6,000-20,000 API calls

### Recommendation:
Start with $5-10 to see how long it lasts with your usage patterns. You can always add more later.

---

## Using AI Plugins in NVim

### Quick Usage Guide

#### For Code Explanation (Gemini):
- Select code in visual mode
- Run `:GeminiCodeExplain`
- OR press `<Leader><Leader><Leader>g` and select "Code Explain"

#### For Code Review (Gemini):
- Select code in visual mode
- Run `:GeminiCodeReview`

#### For Interactive Chat:
- **Avante**: Press `<leader>aa` or run `:AvanteChat`
- **ChatGPT**: Run `:ChatGPT` (after adding credits)
- **Gemini**: Run `:GeminiChat`

#### For Code Editing (Avante):
- Press `<leader>ae` to edit with instructions
- OR run `:AvanteEdit`

#### For Code Completion (Gemini):
- Just start typing - automatic suggestions appear after 800ms
- Press `<S-Tab>` to accept the suggestion

---

## ChatGPT.nvim Specific Usage

### Commands:
- `:ChatGPT` - Open interactive chat window
- `:ChatGPTEditWithInstructions` - Edit selected code with AI instructions
- `:ChatGPTActAs` - AI acts as a specific role
- `:ChatGPTCompleteCode` - Complete code at cursor
- `:ChatGPTRun` - Run a custom prompt

### Chat Window Controls:
- `<C-Enter>` or `<Enter>` - Submit message
- `<C-c>` - Close window
- `<C-n>` - New session
- `<Tab>` - Cycle between windows
- `<C-y>` - Yank last response to clipboard

### Example Workflow:
1. Open a file and select code in visual mode
2. Run `:ChatGPTEditWithInstructions`
3. Type instruction: "add error handling and type hints"
4. Press `<C-y>` to accept changes or `<C-c>` to cancel

---

## Working Example: Midjourney Prompt Generation

Since OpenAI quota was exceeded, used Gemini instead:

### Command Used:
```bash
curl -s "https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent?key=$GEMINI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "contents": [{
      "parts": [{
        "text": "Create a detailed Midjourney prompt for: a South Sea Island with a beautiful beach and a tiki bar"
      }]
    }]
  }'
```

### In NVim (Alternative):
```vim
:GeminiChat
```
Then type: "Create a Midjourney prompt for [description]"

Or use Avante:
```vim
<leader>aa
```
Type your prompt request.

---

## API Keys Configuration

Both API keys are configured in environment variables:
- `GEMINI_API_KEY` - Working ✓
- `OPENAI_API_KEY` - Valid but quota exceeded ⚠️

After adding credits to OpenAI, ChatGPT.nvim will work immediately without any configuration changes.

---

## Test Files Created

For testing purposes:
- Test script: `/tmp/test_ai_plugins.sh`
- Test file: `/tmp/ai_plugin_test.py`
- Full report: `/tmp/nvim_ai_plugin_test_results.md`

---

## Summary

- **Gemini and Avante** are working perfectly (FREE)
- **ChatGPT.nvim** needs billing credits added
- All plugins are properly configured once credits are added
- Use Gemini/Avante in the meantime for all AI assistance

---

## Avante API Key Fix (2026-01-30)

### Issue
Avante was prompting for API key even though `GEMINI_API_KEY` was set in environment.

### Root Cause
Avante's UI prompts for API key on first use if `vim.g.avante_login` flag isn't set.

### Solution
Added `init` function to `~/.config/nvim/lua/plugins/avante.lua` that sets the login flag if the environment variable exists:

```lua
init = function()
  -- Mark as logged in since we have GEMINI_API_KEY in environment
  if vim.env.GEMINI_API_KEY ~= nil then
    vim.g.avante_login = true
  end
end,
```

### Resolution
Avante plugin was removed due to persistent API key prompt issues.
Using Gemini.nvim directly instead, which works perfectly.

### Removal Steps
1. Deleted `~/.config/nvim/lua/plugins/avante.lua`
2. Run `:Lazy clean` in NVim to remove plugin files
3. Use `:GeminiChat`, `:GeminiCodeExplain`, etc. instead
