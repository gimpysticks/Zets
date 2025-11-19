---
title: treesitter-markdown-fix
created: 2025-10-21
modified: 2025-10-21
---

# nvim-treesitter Markdown Parser Fix

## Summary

I successfully resolved the nvim-treesitter compilation issue for the markdown_inline parser. Here's what was happening and how I fixed it:

## The Problem

The nvim-treesitter installation process was failing because:
1. The parsers were being downloaded and extracted correctly
2. However, the compilation step was not producing the expected parser.so file
3. This was causing the final mv command to fail with "No such file or directory"

## Root Cause

The Tree-sitter parsers for markdown use a different build system than what nvim-treesitter expects. They use a Makefile that builds libraries named `libtree-sitter-markdown.so` instead of the expected `parser.so`.

## The Solution

I manually compiled both the markdown and markdown_inline parsers by:

1. **Cleaning up the failed installation directories**
2. **Installing build dependencies** (build-essential was already present)
3. **Manually compiling the parsers:**
   - Compiled object files: `gcc -Isrc -std=c11 -fPIC -c -o src/parser.o src/parser.c`
   - Compiled scanner files: `gcc -Isrc -std=c11 -fPIC -c -o src/scanner.o src/scanner.c`
   - Created shared libraries: `gcc -shared src/parser.o src/scanner.o -o parser.so`
4. **Copied the compiled parsers to the correct nvim-treesitter location:**
   - `markdown.so` for markdown parser
   - `markdown_inline.so` for markdown_inline parser

## Verification

Both parsers are now successfully installed and appear in the list of available parsers when queried through LunarVim.

---

*Saved: 2025-06-23 03:43 UTC*
*System: Pop!_OS Linux*
