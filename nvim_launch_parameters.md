Neovim (and Vim) has many command line options. Here are some of the most common and useful ones:

### Opening Files and Executing Commands

* `nvim filename` - Opens `filename` for editing. You can list multiple files.
* `nvim -c "command"` or `nvim +"command"` - Executes an Ex command (`:command`) after the first file has been read.
    * Example: `nvim +5 file.txt` (Starts editing at line 5).
    * Example: `nvim -c "set number" file.txt` (Opens file and enables line numbers).
    * Example: `nvim +/pattern file.txt` (Opens file and searches for "pattern").
* `nvim --cmd "command"` - Executes a command **before** processing your user configuration files (like `init.lua` or `init.vim`).

### Startup Configuration

* `nvim -u NONE` - Starts Neovim without loading any configuration files (useful for debugging your config).
* `nvim -u filename` - Uses `filename` as the config file instead of the default.
* `nvim --clean` - Mimics a fresh install of Neovim (disables configuration and plugins).

### Modes and Behavior

* `nvim -R` - Read-only mode.
* `nvim -m` - Modifying files is disabled (like read-only, but you can still change options).
* `nvim -e` or `nvim -E` - Starts in Ex mode.
* `nvim -s scriptin` - Reads normal mode commands from `scriptin` after opening the file.
* `nvim -S sessionfile` - Restores a saved session from `sessionfile`.
* `nvim --headless` - Runs Neovim in the background without a user interface (useful for scripting).

### Information

* `nvim --help` or `nvim -h` - Prints a usage (help) message and exits.
* `nvim --version` or `nvim -v` - Prints version information and exits.

You can mix and match most options and file names. For the most complete and official list, you should check the Neovim documentation.