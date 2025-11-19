---
title: Vim_Keybindings
created: 2025-10-21
modified: 2025-10-21
---

**n  K**           *@:<C-U>execute "!pydoc " . expand("<cword>")<CR>
	Last set from ~/.config/nvim/init.vim line 44

v  <C-C>       * "+y
	Last set from ~/.config/nvim/init.vim line 61

n  <C-H>       * <C-W><C-H>
	Last set from ~/.config/nvim/init.vim line 34

n  <NL>        * <C-W><NL>
	Last set from ~/.config/nvim/init.vim line 31

x  <C-K>         <Plug>(neosnippet_expand_target)
	Last set from ~/.config/nvim/init.vim line 131

s  <C-K>         <Plug>(neosnippet_expand_or_jump)
	Last set from ~/.config/nvim/init.vim line 130

n  <C-K>       * <C-W><C-K>
	Last set from ~/.config/nvim/init.vim line 32

n  <C-L>       * <C-W><C-L>
	Last set from ~/.config/nvim/init.vim line 33

n  <C-P>       * :Explore!<CR>
	Last set from ~/.config/nvim/init.vim line 37

x  <C-S>         <Plug>(coc-range-select)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 121

n  <C-S>         <Plug>(coc-range-select)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 120

n  <Space>M    * :call magit#show_magit('v')<CR>
	Last set from ~/.config/nvim/plugged/vimagit/plugin/magit.vim line 46

n  <Space>p    * :<C-U>CocListResume<CR><Space>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 153

n  <Space>k    * :<C-U>CocPrev<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 151

n  <Space>j    * :<C-U>CocNext<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 149

n  <Space>s    * :<C-U>CocList -I symbols<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 147

n  <Space>o    * :<C-U>CocList outline<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 145

n  <Space>c    * :<C-U>CocList commands<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 143

n  <Space>e    * :<C-U>CocList extensions<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 141

n  <Space>qf     <Plug>(coc-fix-current)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 105

n  <Space>ac     <Plug>(coc-codeaction)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 103

n  <Space>a    * :<C-U>CocList diagnostics<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 139

x  <Space>a      <Plug>(coc-codeaction-selected)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 99

n  <Space>f      <Plug>(coc-format-selected)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 87

x  <Space>f      <Plug>(coc-format-selected)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 86

n  <Space>rn     <Plug>(coc-rename)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 83

   <Space>et     :tabe %%

	Last set from ~/.config/nvim/init.vim line 126

   <Space>ev     :vsp %%

	Last set from ~/.config/nvim/init.vim line 125

   <Space>es     :sp %%

	Last set from ~/.config/nvim/init.vim line 124

   <Space>ew     :e %%

	Last set from ~/.config/nvim/init.vim line 123

n  <Space>g      :Goyo<CR>
	Last set from ~/.config/nvim/init.vim line 117

n  <Space>r    * :RunInInteractiveShell<Space>
	Last set from ~/.config/nvim/init.vim line 69

n  <Space>l      :set list!<CR>
	Last set from ~/.config/nvim/init.vim line 70

   <Space>P      :set paste<CR>O<Esc>"*]p:set nopaste<CR>"

	Last set from ~/.config/nvim/init.vim line 53

ov <Space>p      :set paste<CR>o<Esc>"*]p:set nopaste<CR>"
	Last set from ~/.config/nvim/init.vim line 52

o  %             <Plug>(MatchitOperationForward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 60

x  %             <Plug>(MatchitVisualForward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 58

n  %             <Plug>(MatchitNormalForward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 56

n  K           * :call <SNR>20_show_documentation()<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 69

x  S             <Plug>VSurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 608

o  [%            <Plug>(MatchitOperationMultiBackward)
	Last set from /sr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 75

x  [%            <Plug>(MatchitVisualMultiBackward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 73

n  [%            <Plug>(MatchitNormalMultiBackward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 71

n  [g            <Plug>(coc-diagnostic-prev)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 59

n  \\          * :let tmp=@/|s:/:\\:ge|let @/=tmp|noh<CR>
	Last set from ~/.config/nvim/init.vim line 30

n  \/          * :let tmp=@/|s:\\:/:ge|let @/=tmp|noh<CR>
	Last set from ~/.config/nvim/init.vim line 29

o  ]%            <Plug>(MatchitOperationMultiForward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 76

x  ]%            <Plug>(MatchitVisualMultiForward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 74

n  ]%            <Plug>(MatchitNormalMultiForward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 72

n  ]g            <Plug>(coc-diagnostic-next)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 60

x  a%            <Plug>(MatchitVisualTextObject)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 80

o  ac            <Plug>(coc-classobj-a)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 116

x  ac            <Plug>(coc-classobj-a)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 115

o  af            <Plug>(coc-funcobj-a)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 112

x  af            <Plug>(coc-funcobj-a)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 111

n  cS            <Plug>CSurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 602

n  cs            <Plug>Csurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 601

n  ds            <Plug>Dsurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 600

v  gx            <Plug>NetrwBrowseXVis
	Last set from /usr/share/nvim/runtime/plugin/netrwPlugin.vim line 88

n  gx            <Plug>NetrwBrowseX
	Last set from /usr/share/nvim/runtime/plugin/netrwPlugin.vim line 82

o  g%            <Plug>(MatchitOperationBackward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 61

x  g%            <Plug>(MatchitVisualBackward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 59

n  g%            <Plug>(MatchitNormalBackward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 57

n  gcu           <Plug>Commentary<Plug>Commentary
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 114

n  gcc           <Plug>CommentaryLine
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 110

o  gc            <Plug>Commentary
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 109

n  gc            <Plug>Commentary
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 108

x  gc            <Plug>Commentary
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 107

x  gS            <Plug>VgSurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 609

n  gr            <Plug>(coc-references)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 66

n  gi            <Plug>(coc-implementation)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 65

n  gy            <Plug>(coc-type-definition)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 64

n  gd            <Plug>(coc-definition)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 63

o  ic            <Plug>(coc-classobj-i)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 114

x  ic            <Plug>(coc-classobj-i)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 113

o  if            <Plug>(coc-funcobj-i)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 110

x  if            <Plug>(coc-funcobj-i)
	Last set from ~/.config/nvim/plugged/coc.nvim/coc.vim line 109

n  y<C-G>      & :<C-U>call setreg(v:register, fugitive#Object(@%))<CR>
	Last set from ~/.config/nvim/plugged/vim-fugitive/plugin/fugitive.vim line 519

n  ySS           <Plug>YSsurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 607

n  ySs           <Plug>YSsurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 606

n  yss           <Plug>Yssurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 605

n  yS            <Plug>YSurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 604

n  ys            <Plug>Ysurround
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 603

n  {Previous-Mapping} * :TmuxNavigatePrevious<CR>
	Last set from ~/.config/nvim/init.vim line 58

n  {Right-Mapping} * :TmuxNavigateRight<CR>
	Last set from ~/.config/nvim/init.vim line 57

n  {Up-Mapping} * :TmuxNavigateUp<CR>
	Last set from ~/.config/nvim/init.vim line 56

n  {Down-Mapping} * :TmuxNavigateDown<CR>
	Last set from ~/.config/nvim/init.vim line 55

n  {Left-Mapping} * :TmuxNavigateLeft<CR>
	Last set from ~/.config/nvim/init.vim line 54

v  <Plug>(coc-snippets-select) * :<C-U>call coc#rpc#notify('doKeymap', [Tasks.md'snippets-select'])<CR>
x  <Plug>(coc-git-chunk-outer) * :<C-U>call coc#rpc#request('doKeymap', [Tasks.md'git-chunk-outer'])<CR>
o  <Plug>(coc-git-chunk-outer) * :<C-U>call coc#rpc#request('doKeymap', [Tasks.md'git-chunk-outer'])<CR>
x  <Plug>(coc-git-chunk-inner) * :<C-U>call coc#rpc#request('doKeymap', [Tasks.md'git-chunk-inner'])<CR>
o  <Plug>(coc-git-chunk-inner) * :<C-U>call coc#rpc#request('doKeymap', [Tasks.md'git-chunk-inner'])<CR>
n  <Plug>(coc-git-commit) * :<C-U>call coc#rpc#notify('doKeymap', [Tasks.md'git-commit'])<CR>
n  <Plug>(coc-git-chunkinfo) * :<C-U>call coc#rpc#notify('doKeymap', [Tasks.md'git-chunkinfo'])<CR>
n  <Plug>(coc-git-prevchunk) * :<C-U>call coc#rpc#notify('doKeymap', [Tasks.md'git-prevchunk'])<CR>
n  <Plug>(coc-git-nextchunk) * :<C-U>call coc#rpc#notify('doKeymap', [Tasks.md'git-nextchunk'])<CR>
   <Plug>AirlineSelectNextTab * :<C-U>call <SNR>126_jump_to_tab(v:count1)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 212

   <Plug>AirlineSelectPrevTab * :<C-U>call <SNR>126_jump_to_tab(-v:count1)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 211

   <Plug>AirlineSelectTab9 * :call <SNR>126_select_tab(8)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

   <Plug>AirlineSelectTab8 * :call <SNR>126_select_tab(7)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

   <Plug>AirlineSelectTab7 * :call <SNR>126_select_tab(6)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

   <Plug>AirlineSelectTab6 * :call <SNR>126_select_tab(5)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

   <Plug>AirlineSelectTab5 * :call <SNR>126_select_tab(4)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

   <Plug>AirlineSelectTab4 * :call <SNR>126_select_tab(3)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

   <Plug>AirlineSelectTab3 * :call <SNR>126_select_tab(2)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

   <Plug>AirlineSelectTab2 * :call <SNR>126_select_tab(1)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

   <Plug>AirlineSelectTab1 * :call <SNR>126_select_tab(0)<CR>

	Last set from ~/.config/nvim/plugged/vim-airline/autoload/airline/extensions/tabline/buffers.vim line 203

v  <Plug>NetrwBrowseXVis * :<C-U>call netrw#BrowseXVis()<CR>
	Last set from /usr/share/nvim/runtime/plugin/netrwPlugin.vim line 90

n  <Plug>NetrwBrowseX * :call netrw#BrowseX(expand((exists("g:netrw_gx")? g:netrw_gx : '<cfile>')),netrw#CheckIfRemote())<CR>
	Last set from /usr/share/nvim/runtime/plugin/netrwPlugin.vim line 84

v  <Plug>(MatchitVisualTextObject)   <Plug>(MatchitVisualMultiBackward)o<Plug>(MatchitVisualMultiForward)
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 79

o  <Plug>(MatchitOperationMultiForward) * :<C-U>call matchit#MultiMatch("W",  "o")<CR>
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 69

o  <Plug>(MatchitOperationMultiBackward) * :<C-U>call matchit#MultiMatch("bW", "o")<CR>
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 68

v  <Plug>(MatchitVisualMultiForward) * :<C-U>call matchit#MultiMatch("W",  "n")<CR>m'gv``
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 67

v  <Plug>(MatchitVisualMultiBackward) * :<C-U>call matchit#MultiMatch("bW", "n")<CR>m'gv``
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 66

n  <Plug>(MatchitNormalMultiForward) * :<C-U>call matchit#MultiMatch("W",  "n")<CR>
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 65

n  <Plug>(MatchitNormalMultiBackward) * :<C-U>call matchit#MultiMatch("bW", "n")<CR>
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 64

o  <Plug>(MatchitOperationBackward) * :<C-U>call matchit#Match_wrapper('',0,'o')<CR>
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 54

o  <Plug>(MatchitOperationForward) * :<C-U>call matchit#Match_wrapper('',1,'o')<CR>
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 53

v  <Plug>(MatchitVisualBackward) * :<C-U>call matchit#Match_wrapper('',0,'v')<CR>m'gv``
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 52

v  <Plug>(MatchitVisualForward) * :<C-U>call matchit#Match_wrapper('',1,'v')<CR>m'gv``
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 51

n  <Plug>(MatchitNormalBackward) * :<C-U>call matchit#Match_wrapper('',0,'n')<CR>
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 50

n  <Plug>(MatchitNormalForward) * :<C-U>call matchit#Match_wrapper('',1,'n')<CR>
	Last set from /usr/share/nvim/runtime/pack/dist/opt/matchit/plugin/matchit.vim line 49

n  <Plug>CommentaryUndo   :echoerr "Change your <Plug>CommentaryUndo map to <Plug>Commentary<Plug>Commentary"<CR>
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 104

n  <Plug>ChangeCommentary * c:<C-U>call <SNR>47_textobject(1)<CR>
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 103

o  <Plug>Commentary * :<C-U>call <SNR>47_textobject(get(v:, 'operator', '') ==# 'c')<CR>
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 102

n  <Plug>CommentaryLine * <SNR>47_go() . '_'
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 101

n  <Plug>Commentary * <SNR>47_go()
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 100

x  <Plug>Commentary * <SNR>47_go()
	Last set from ~/.config/nvim/plugged/vim-commentary/plugin/commentary.vim line 99

v  <Plug>VgSurround * :<C-U>call <SNR>46_opfunc(visualmode(),visualmode() ==# 'V' ? 0 : 1)<CR>
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 595

v  <Plug>VSurround * :<C-U>call <SNR>46_opfunc(visualmode(),visualmode() ==# 'V' ? 1 : 0)<CR>
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 594

n  <Plug>YSurround * <SNR>46_opfunc2('setup')
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 593

n  <Plug>Ysurround * <SNR>46_opfunc('setup')
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 592

n  <Plug>YSsurround * <SNR>46_opfunc2('setup').'_'
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 591

n  <Plug>Yssurround * '^'.v:count1.<SNR>46_opfunc('setup').'g_'
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 590

n  <Plug>CSurround * :<C-U>call <SNR>46_changesurround(1)<CR>
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 589

n  <Plug>Csurround * :<C-U>call <SNR>46_changesurround()<CR>
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 588

n  <Plug>Dsurround * :<C-U>call <SNR>46_dosurround(<SNR>46_inputtarget())<CR>
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 587

n  <Plug>SurroundRepeat * .
	Last set from ~/.config/nvim/plugged/vim-surround/plugin/surround.vim line 586

o  <Plug>(fzf-maps-o) * <C-C>:<C-U>call fzf#vim#maps('o', 0)<CR>
	Last set from ~/.config/nvim/plugged/fzf.vim/plugin/fzf.vim line 153

x  <Plug>(fzf-maps-x) * :<C-U>call fzf#vim#maps('x', 0)<CR>
	Last set from ~/.config/nvim/plugged/fzf.vim/plugin/fzf.vim line 152

n  <Plug>(fzf-maps-n) * :<C-U>call fzf#vim#maps('n', 0)<CR>
	Last set from ~/.config/nvim/plugged/fzf.vim/plugin/fzf.vim line 150

o  <Plug>(coc-classobj-a) * :<C-U>call coc#rpc#request('selectSymbolRange', [Tasks.mdv:false, '', [Tasks.md'Interface', 'Struct', 'Class']])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 468

o  <Plug>(coc-classobj-i) * :<C-U>call coc#rpc#request('selectSymbolRange', [Tasks.mdv:true, '', [Tasks.md'Interface', 'Struct', 'Class']])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 467

v  <Plug>(coc-classobj-a) * :<C-U>call coc#rpc#request('selectSymbolRange', [Tasks.mdv:false, visualmode(), [Tasks.md'Interface', 'Struct', 'Class']])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 466

v  <Plug>(coc-classobj-i) * :<C-U>call coc#rpc#request('selectSymbolRange', [Tasks.mdv:true, visualmode(), [Tasks.md'Interface', 'Struct', 'Class']])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 465

o  <Plug>(coc-funcobj-a) * :<C-U>call coc#rpc#request('selectSymbolRange', [Tasks.mdv:false, '', [Tasks.md'Method', 'Function']])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 463

o  <Plug>(coc-funcobj-i) * :<C-U>call coc#rpc#request('selectSymbolRange', [Tasks.mdv:true, '', [Tasks.md'Method', 'Function']])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 462

v  <Plug>(coc-funcobj-a) * :<C-U>call coc#rpc#request('selectSymbolRange', [Tasks.mdv:false, visualmode(), [Tasks.md'Method', 'Function']])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 461

v  <Plug>(coc-funcobj-i) * :<C-U>call coc#rpc#request('selectSymbolRange', [Tasks.mdv:true, visualmode(), [Tasks.md'Method', 'Function']])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 460

n  <Plug>(coc-cursors-position) * :<C-U>call coc#rpc#request('cursorsSelect', [bufnr('%'), 'position', 'n'])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 458

n  <Plug>(coc-cursors-word) * :<C-U>call coc#rpc#request('cursorsSelect', [bufnr('%'), 'word', 'n'])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 457

v  <Plug>(coc-cursors-range) * :<C-U>call coc#rpc#request('cursorsSelect', [bufnr('%'), 'range', visualmode()])<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 456

n  <Plug>(coc-cursors-operator) * :<C-U>set operatorfunc=<SNR>21_CursorRangeFromSelected<CR>g@
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 455

n  <Plug>(coc-refactor) * :<C-U>call       CocActionAsync('refactor')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 452

n  <Plug>(coc-command-repeat) * :<C-U>call       CocAction('repeatCommand')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 451

n  <Plug>(coc-float-jump) * :<C-U>call       coc#util#float_jump()<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 450

n  <Plug>(coc-float-hide) * :<C-U>call       coc#util#float_hide()<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 449

n  <Plug>(coc-fix-current) * :<C-U>call       CocActionAsync('doQuickfix')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 448

n  <Plug>(coc-openlink) * :<C-U>call       CocActionAsync('openLink')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 447

n  <Plug>(coc-references) * :<C-U>call       CocActionAsync('jumpReferences')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 446

n  <Plug>(coc-type-definition) * :<C-U>call       CocActionAsync('jumpTypeDefinition')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 445

n  <Plug>(coc-implementation) * :<C-U>call       CocActionAsync('jumpImplementation')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 444

n  <Plug>(coc-declaration) * :<C-U>call       CocActionAsync('jumpDeclaration')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 443

n  <Plug>(coc-definition) * :<C-U>call       CocActionAsync('jumpDefinition')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 442

n  <Plug>(coc-diagnostic-prev-error) * :<C-U>call       CocActionAsync('diagnosticPrevious', 'error')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 441

n  <Plug>(coc-diagnostic-next-error) * :<C-U>call       CocActionAsync('diagnosticNext',     'error')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 440

n  <Plug>(coc-diagnostic-prev) * :<C-U>call       CocActionAsync('diagnosticPrevious')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 439

n  <Plug>(coc-diagnostic-next) * :<C-U>call       CocActionAsync('diagnosticNext')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 438

n  <Plug>(coc-diagnostic-info) * :<C-U>call       CocActionAsync('diagnosticInfo')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 437

n  <Plug>(coc-format) * :<C-U>call       CocActionAsync('format')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 436

n  <Plug>(coc-format-selected) * :<C-U>set        operatorfunc=<SNR>21_FormatFromSelected<CR>g@
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 435

n  <Plug>(coc-rename) * :<C-U>call       CocActionAsync('rename')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 434

n  <Plug>(coc-codeaction-line) * :<C-U>call       CocActionAsync('codeAction',         'n')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 433

n  <Plug>(coc-codeaction) * :<C-U>call       CocActionAsync('codeAction',         '')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 432

n  <Plug>(coc-codeaction-selected) * :<C-U>set        operatorfunc=<SNR>21_CodeActionFromSelected<CR>g@
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 431

v  <Plug>(coc-codeaction-selected) * :<C-U>call       CocActionAsync('codeAction',         visualmode())<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 430

v  <Plug>(coc-format-selected) * :<C-U>call       CocActionAsync('formatSelected',     visualmode())<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 429

n  <Plug>(coc-codelens-action) * :<C-U>call       CocActionAsync('codeLensAction')<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 428

n  <Plug>(coc-range-select) * :<C-U>call       CocAction('rangeSelect',     '', v:true)<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 427

v  <Plug>(coc-range-select-backward) * :<C-U>call       CocAction('rangeSelect',     visualmode(), v:false)<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 426

v  <Plug>(coc-range-select) * :<C-U>call       CocAction('rangeSelect',     visualmode(), v:true)<CR>
	Last set from ~/.config/nvim/plugged/coc.nvim/plugin/coc.vim line 425

n  <F5>        * :set relativenumber!<CR>
	Last set from ~/.config/nvim/init.vim line 115

n  <F4>        * :set nonumber!<CR>
	Last set from ~/.config/nvim/init.vim line 114

   <F6>          :setlocal spell! spelllang=us_en<CR>

	Last set from ~/.config/nvim/init.vim line 116

n  <F9>          :!python %<CR>
	Last set from ~/.config/nvim/init.vim line 60

v  <M-k>       * :m-2<CR>gv=gv
	Last set from ~/.config/nvim/init.vim line 43

v  <M-j>       * :m'>+<CR>gv=gv
	Last set from ~/.config/nvim/init.vim line 42

n  <M-k>       * :m-2<CR>==
	Last set from ~/.config/nvim/init.vim line 39

n  <M-j>       * :m+<CR>==
	Last set from ~/.config/nvim/init.vim line 38

n  <Left>      * :bp<CR>
	Last set from ~/.config/nvim/init.vim line 36

n  <Right>     * :bn<CR>
	Last set from ~/.config/nvim/init.vim line 35

u
