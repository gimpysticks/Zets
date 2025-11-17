# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This appears to be a personal development environment and scripts collection with the following key characteristics:

- **Primary Purpose**: Collection of personal scripts, utilities, and development tools
- **License**: Apache (as mentioned in README.md)
- **Main Directory**: `/home/sticks` serves as the primary working directory
- **Script Location**: Scripts are expected to be in `~/.local/bin/scripts` with `$SCRIPTS` environment variable pointing there

## Development Environment

### Text Editor: Neovim
- **Configuration**: Modern Neovim setup using lazy.nvim plugin manager
- **Key Plugins**: 
  - Gruvbox theme
  - vim-airline for status line
  - vimwiki for note-taking (integrated with `~/zets/` directory)
  - nvim-surround for text manipulation
- **Leader Key**: Space (` `)
- **Important Features**:
  - Automatic git sync for vimwiki notes in `~/zets/`
  - Line movement with Alt+j/Alt+k
  - Swap files disabled
  - 4-space indentation, smart case search

### Key Directories and Projects

#### Scripts and Utilities (`/home/sticks/` root)
- Personal scripts collection designed for reuse
- Mix of POSIX shell, Perl, and Python3 scripts
- Includes shortcut commands (alternatives to aliases)

#### Programming Projects
- **Rust Projects**: `~/Projects/hello_cargo/`, `~/Projects/guessing_game/`
- **Python Projects**: Various Python utilities in `~/src/pythonfiles/`
- **Node.js**: Root package.json with dependencies including OpenAI and tree-sitter-cli

#### Development Tools
- **Languages**: Python, Rust, JavaScript/Node.js, Perl, POSIX shell
- **Package Managers**: npm (Node.js), Cargo (Rust), pip (Python)

## Common Commands

### Node.js Development
```bash
npm install    # Install dependencies
```

### Rust Development
```bash
cargo build    # Build Rust projects
cargo run      # Run Rust projects
cargo test     # Run tests (if any)
```

### Python Development
```bash
python3 -m pip install -r requirements.txt    # Install dependencies (various projects have requirements.txt)
```

### Neovim
```bash
nvim           # Launch Neovim
# Key mappings:
# <Space>ww    - Open vimwiki index
# <Space>wg    - Git sync vimwiki files
# Alt+j/Alt+k  - Move lines up/down
```

## Important Notes

### Script Philosophy
- Preference for POSIX shell, Perl, and Python3 over bash
- Scripts designed to work across different environments (Docker, etc.)
- Perl used as replacement for sed/awk with better regex support

### Vimwiki Integration
- Personal knowledge base in `~/zets/` directory
- Automatic git commits and pushes on file save
- Markdown format with `.md` extension

### Development Environment
- Mixed personal and development files in home directory
- Scripts expected to reference `$SCRIPTS` environment variable
- Various configuration files for different tools (git, ssh, containers, etc.)

## Project Structure Insights

This is primarily a personal development environment rather than a single focused project. Key areas include:

1. **Personal Scripts**: Utility scripts for various tasks
2. **Learning Projects**: Rust and other language learning exercises  
3. **Configuration Management**: Dotfiles and configuration for various tools
4. **Media and Personal Files**: Mixed with development files
5. **Knowledge Management**: Vimwiki-based note system with git integration