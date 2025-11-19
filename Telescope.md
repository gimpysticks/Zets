---
title: Telescope
created: 2025-10-21
modified: 2025-10-21
---

Telescope has been added to your Neovim configuration! Here's what I
  installed:

  Telescope Setup:
  - telescope.nvim - Main fuzzy finder plugin
  - plenary.nvim - Required dependency
  - telescope-fzf-native.nvim - FZF integration for better performance

  Key Mappings (with Space as leader):
  - <Space>ff - Find files
  - <Space>fg - Live grep (search in files)
  - <Space>fb - Find buffers
  - <Space>fh - Help tags
  - <Space>fr - Recent files
  - <Space>fc - Commands
  - <Space>fk - Keymaps
  - <Space>fs - Search in current buffer
  - <Space>ft - Treesitter symbols
  - <Space>fd - Diagnostics

  Features:
  - FZF integration for fast fuzzy finding
  - Hidden files included in searches
  - Smart case matching
  - Customized layout and ignore patterns
  - Navigation with Ctrl+j/k in both insert and normal modes

  Restart Neovim or run :Lazy sync to install the new plugins. The
  fzf-native extension will be built automatically.

