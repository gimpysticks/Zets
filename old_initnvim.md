---
title: old_init.nvim
date: 2023-09-03 11:23
---
sset nocompatible
set ruler
filetype plugin on
set shortmess+=I
set nowrap
set undodir=~/.config/nvim/vimswap
set undofile
set noswapfile
set showcmd       " display incomplete commands
set incsearch     " do incremental searching
set laststatus=2  " Always display the status line
set hlsearch      " Turn highlight seach on
set nrformats=alpha
set number	  " Turn on line numbers
set rnu           " Turn on relative numbers
set scrolloff=8
set signcolumn=yes
set cursorline
set textwidth=80
set colorcolumn=+1
set path+=**
set shiftwidth=4
set shiftround
set softtabstop=4
set expandtab
set wildmenu
set wildmode=longest:full,full
set list
set listchars=eol:¬,tab:>-,trail:~,extends:>,precedes:<
set clipboard=unnamedplus
set hidden
set history=200
set cmdheight=2
set timeoutlen=1000
set directory^=$HOME/.config/nvim/vimswap//
set signcolumn=yes
set ignorecase
setglobal complete-=i
syntax enable
set rtp+=/home/sticks/.fzf/bin/fzf
let mapleader = "\<Space>"
"
function ClearRegs()
  let regs=split('abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789/-"', '\zs')
  for r in regs
    call setreg(r, @_)
  endfor
:endfunction


" press \\ to convert every forwardslash to a backslash
" press \/ to convert every backslash to a forwardslash
nnoremap <silent> <Bslash>/ :let tmp=@/<BAR>s:\\:/:ge<BAR>let @/=tmp<BAR>noh<CR>
nnoremap <silent> <Bslash><Bslash> :let tmp=@/<BAR>s:/:\\:ge<BAR>let @/=tmp<BAR>noh<CR>
nnoremap <C-J> <C-W><C-J>
nnoremap <C-K> <C-W><C-K>
nnoremap <C-L> <C-W><C-L>
nnoremap <C-H> <C-W><C-H>
nnoremap <Right> :bn<enter>
nnoremap <Left> :bp<enter>
nnoremap <C-p> :CocCommand explorer<enter>
nnoremap <silent> <F3> :FZF -m<CR>
nnoremap <A-j> :m+<CR>==
nnoremap <A-k> :m-2<CR>==
inoremap <A-j> <Esc>:m+<CR>==gi
inoremap <A-k> <Esc>:m-2<CR>==gi
vnoremap <A-j> :m'>+<CR>gv=gv
vnoremap <A-k> :m-2<CR>gv=gv
nnoremap <buffer> K :<C-u>execute "!pydoc " . expand("<cword>")<CR>
nnoremap <silent> <leader> :WhichKey '<Space>'<CR>
nnoremap <leader>md :MarkdownPreview<CR>
nnoremap <leader>ms :MarkdownPreviewStop<CR>
nnoremap <leader>nz :ZettelNew
nnoremap <leader>ni gg0dG:VimwikiGenerateLinks
4dd
nnoremap <leader>x :!xdg-open %<cr><cr>
let g:tmux_navigator_no_mappings = 1
cnoremap w!! execute 'silent! write !sudo tee % >/dev/null' <bar> edit!
cnoremap <expr> %% getcmdtype() == ':' ? expand('%:h').'/' : '%%'
let g:tmux_navigator_no_mappings = 1
""" SYSTEM CLIPBOARD COPY & PASTE SUPPORT
set pastetoggle=<F2> "F2 before pasting to preserve indentation
"Copy paste to/from clipboard
map <silent><Leader>p :set paste<CR>o<esc>"*]p:set nopaste<cr>"
map <silent><Leader><S-p> :set paste<CR>O<esc>"*]p:set nopaste<cr>"
nnoremap <silent> {Left-Mapping} :TmuxNavigateLeft<cr>
nnoremap <silent> {Down-Mapping} :TmuxNavigateDown<cr>
nnoremap <silent> {Up-Mapping} :TmuxNavigateUp<cr>
nnoremap <silent> {Right-Mapping} :TmuxNavigateRight<cr>
nnoremap <silent> {Previous-Mapping} :TmuxNavigatePrevious<cr>
nnoremap <silent> <leader>R :call ClearRegs()<CR>
nmap <F9> :!python %<cr>
vnoremap <C-c> "+y
set spelllang=en
let g:spellfile_URL='http://ftp.vim.org/vim/runtime/spell'
set spellfile=/home/sticks/.config/nvim/spell/us.utf-8.add
set splitbelow splitright
nnoremap <silent> <F6> :set spell!<cr>
inoremap <silent> <F6> <C-O>:set spell!<cr>
" Run commands that require an interactive shell
nnoremap <Leader>r :RunInInteractiveShell<space>
nnoremap <Leader>t :AirlineTheme random<cr>
nmap <leader>l :set list!<CR>
set laststatus=2
set t_Co=256
let g:pymode_python = 'python3'
let g:sudo_askpass='/usr/lib/openssh/gnome-ssh-askpass'
inorea _SH #!/bin/bash
inorea _PY #!/usr/bin/env python
call plug#begin()
Plug 'neoclide/coc.nvim', {'branch': 'release'}
Plug 'ternjs/tern_for_vim', { 'do': 'npm install' }
Plug 'vimwiki/vimwiki'
Plug 'junegunn/fzf', { 'do': './install --bin' }
Plug 'junegunn/fzf.vim'
Plug 'michal-h21/vim-zettel'
Plug 'michal-h21/vimwiki-sync'
Plug 'tmsvg/pear-tree'
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'
Plug 'liuchengxu/vim-which-key'
Plug 'tpope/vim-surround'
Plug 'junegunn/vim-peekaboo'
Plug 'tpope/vim-commentary'
Plug 'tpope/vim-repeat'
Plug 'tpope/vim-fugitive'
Plug 'plasticboy/vim-markdown'
Plug 'tommcdo/vim-fubitive'
Plug 'dracula/vim', { 'as': 'dracula' }
Plug 'tomtom/tlib_vim'
Plug 'MarcWeber/vim-addon-mw-utils'
Plug 'honza/vim-snippets'
Plug 'godlygeek/tabular'
Plug 'christoomey/vim-tmux-navigator'
Plug 'junegunn/goyo.vim'
Plug 'flazz/vim-colorschemes'
Plug 'Yggdroot/indentLine'
Plug 'iamcco/mathjax-support-for-mkdp'
Plug 'iamcco/markdown-preview.vim', { 'do': 'cd app & yarn install' }
Plug 'glacambre/firenvim', { 'do': { _ -> firenvim#install(1) } }
call plug#end()

if !exists('g:started_by_firenvim')
    Plug 'vim-airline/vim-airline'
    Plug 'vim-airline/vim-airline-themes'
endif

filetype plugin indent on
let g:airline_powerline_fonts = 1
let g:airline_left_sep='>'
let g:airline_right_sep='<'
" ==============================================================
"     "Uncomment to override defaults:
let g:vimwiki_global_ext = 0
let g:vimwiki_list = [{'path': '~/zets/',
                      \ 'syntax': 'markdown', 'ext': '.md'}]
let g:mkdp_path_to_chrome = ""
    " Path to the chrome or the command to open chrome (or other modern browsers).
    " If set, g:mkdp_browserfunc would be ignored.

    let g:mkdp_browserfunc = 'MKDP_browserfunc_default'
    " Callback Vim function to open browser, the only parameter is the url to open.

    let g:mkdp_auto_start = 0
    " Set to 1, Vim will open the preview window on entering the Markdown
    " buffer.

    let g:mkdp_auto_open = 0
    " Set to 1, Vim will automatically open the preview window when you edit a
    " Markdown file.

    let g:mkdp_auto_close = 1
    " Set to 1, Vim will automatically close the current preview window when
    " switching from one Markdown buffer to another.

    let g:mkdp_refresh_slow = 0
    " Set to 1, Vim will just refresh Markdown when saving the buffer or
    " leaving from insert mode. With default 0, it will automatically refresh
    " Markdown as you edit or move the cursor.

    let g:mkdp_command_for_global = 0
    " Set to 1, the MarkdownPreview command can be used for all files,
    " by default it can only be used in Markdown files.

    let g:mkdp_open_to_the_world = 0
    " Set to 1, the preview server will be available to others in your network.
    " By default, the server only listens on localhost (127.0.0.1).
    let g:vimwiki_url_maxsave = 0
" ===============================================================
"let fc = g:firenvim.config['localSettings']
"let fc['https?://twitter.com'] = { 'takeover': 'never', 'priority': 1 }
"let fc['https?://twitch.tv'] = { 'takeover': 'never', 'priority': 1 }
"=================================================================
let $FZF_DEFAULT_OPTS='--reverse --preview-window=down'
" Let <Tab> also do completion
inoremap <silent><expr> <Tab>
\ pumvisible() ? "\<C-n>" :
" Close the documentation window when completion is done
autocmd InsertLeave,CompleteDone * if pumvisible() == 0 | pclose | endif
autocmd BufWritePre * :%s/\s\+$//e
let g:numbers_exclude = ['tagbar', 'gundo', 'minibufexpl', 'nerdtree']
" nmap <silent> <F3> :NERDTreeToggle<CR>
nnoremap <F4> :set nonumber!<CR>
nnoremap <F5> :set relativenumber!<CR>
map <F6> :setlocal spell! spelllang=us_en<CR>
nmap <leader>g :Goyo<CR>
" colorscheme 256-grayvim
" colorscheme spacecamp
colorscheme gruvbox
let g:airline_theme='fairyfloss'
let g:nv_search_paths = ['/home/sticks/zets']
let g:zettel_format = "%Y%m%d%H%M-%title"
map <leader>ew :e %%
map <leader>es :sp %%
map <leader>ev :vsp %%
map <leader>et :tabe %%
map <leader>gj :diffget //3<CR>
map <leader>gf :diffget //2<CR>
map <leader>gs :G<CR>
map <leader>fs  :Files<CR>
map <leader>pyfile :-1r /home/sticks/snipets/shebangpy<CR>G
map <leader>bash :-1r /home/sticks/snipets/shebangsh<CR>G
" Plugin key-mappings.
" Note: It must be "imap" and "smap".  It uses <Plug> mappings.
imap <C-k>     <Plug>(neosnippet_expand_or_jump)
smap <C-k>     <Plug>(neosnippet_expand_or_jump)
xmap <C-k>     <Plug>(neosnippet_expand_target)
