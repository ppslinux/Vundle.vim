" 使用该配置文件可以完善整个vim的配置，使用该配置文件需要联网并且需要安装git
" 并且运行将远端库安装到本地
" git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
" vundle {
set rtp+=~/.vim/bundle/vundle/
" 如果在windows下使用的话，设置为
" set rtp+=$HOME/.vim/bundle/vundle/
call vundle#rc()
" }
"
" let Vundle manage Vundle
" required!
Bundle 'gmarik/vundle'
  
" My Bundles here:
"
" original repos on github
" github上的用户写的插件，使用这种用户名+repo名称的方式
" Bundle 'tpope/vim-fugitive'
" Bundle 'Lokaltog/vim-easymotion'
" Bundle 'rstacruz/sparkup', {'rtp': 'vim/'}
" Bundle 'tpope/vim-rails.git'
" vim-scripts repos " vimscripts的repo使用下面的格式，直接是插件名称
"
Bundle 'taglist.vim'
Bundle 'SuperTab'
Bundle 'vimwiki'
Bundle 'winmanager'
Bundle 'bufexplorer.zip'
Bundle 'The-NERD-tree'
Bundle 'matrix.vim--Yang'
Bundle 'FencView.vim'
Bundle 'Conque-Shell'
Bundle 'Vimpress'
Bundle 'Markdown'
Bundle 'LaTeX-Suite-aka-Vim-LaTeX'
Bundle 'c.vim'
Bundle 'snipMate'
Bundle 'code_complete'  
Bundle 'word_complete.vim'
Bundle 'cppcomplete'
Bundle 'javacomplete'
Bundle 'SnippetComplete'
Bundle 'CompleteHelper'
Bundle 'Source-Explorer-srcexpl.vim'
Bundle 'trinity.vim'


filetype on
filetype plugin on
filetype indent on

" non github reposo
" 非github的插件，可以直接使用其git地址
" Bundle 'git://git.wincent.com/command-t.git'
" ...
  
"
" Brief help
" :BundleList          - list configured bundles
" :BundleInstall(!)    - install(update) bundles
" :BundleSearch(!) foo - search(or refresh cache first) for foo
" :BundleClean(!)      - confirm(or auto-approve) removal of unused bundles
" vundle主要就是上面这个四个命令，例如BundleInstall是全部重新安装，BundleInstall!则是更新
" 一般安装插件的流程为，先BundleSearch一个插件，然后在列表中选中，按i安装
" 安装完之后，在vimrc中，添加Bundle 'XXX'，使得bundle能够加载，这个插件，同时如果
" 需要配置这个插件，也是在vimrc中设置即可
" see :h vundle for more details or wiki for FAQ
" NOTE: comments after Bundle command are not allowed..
"


nmap e :q 
" When started as "evim", evim.vim will already have done these settings.
if v:progname =~? "evim"
  finish
endif

" Use Vim settings, rather then Vi settings (much better!).
" This must be first, because it changes other options as a side effect.
set nocompatible
set autoread          " 文件修改之后自动载入。

" allow backspacing over everything in insert mode
set backspace=indent,eol,start

if has("vms")
  set nobackup		" do not keep a backup file, use versions instead
else
  set backup		" keep a backup file
endif
set history=150		" keep 50 lines of command line history
set ruler		" show the cursor position all the time
set showcmd		" display incomplete commands
set incsearch		" do incremental searching

" For Win32 GUI: remove 't' flag from 'guioptions': no tearoff menu entries
" let &guioptions = substitute(&guioptions, "t", "", "g")

" Don't use Ex mode, use Q for formatting
map Q gq

" CTRL-U in insert mode deletes a lot.  Use CTRL-G u to first break undo,
" so that you can undo CTRL-U after inserting a line break.
inoremap <C-U> <C-G>u<C-U>

"- 则点击光标不会换,用于复制
"set mouse-=a           " 鼠标暂不启用, 键盘党....
set mouse-=a           " 鼠标启用

" Switch syntax highlighting on, when the terminal has colors
" Also switch on highlighting the last used search pattern.
if &t_Co > 2 || has("gui_running")
  syntax on
  set hlsearch
endif

" Only do this part when compiled with support for autocommands.
if has("autocmd")

  " Enable file type detection.
  " Use the default filetype settings, so that mail gets 'tw' set to 72,
  " 'cindent' is on in C files, etc.
  " Also load indent files, to automatically do language-dependent indenting.
  filetype plugin indent on

  " Put these in an autocmd group, so that we can delete them easily.
  augroup vimrcEx
  au!

  " For all text files set 'textwidth' to 78 characters.


  " When editing a file, always jump to the last known cursor position.
  " Don't do it when the position is invalid or when inside an event handler
  " (happens when dropping a file on gvim).
  " Also don't do it when the mark is in the first line, that is the default
  " position when opening a file.
  autocmd BufReadPost *
    \ if line("'\"") > 1 && line("'\"") <= line("$") |
    \   exe "normal! g`\"" |
    \ endif

  augroup END

else

  set autoindent		" always set autoindenting on

endif " has("autocmd")

" Convenient command to see the difference between the current buffer and the
" file it was loaded from, thus the changes you made.
" Only define it when not defined already.
if !exists(":DiffOrig")
  command DiffOrig vert new | set bt=nofile | r # | 0d_ | diffthis
		  \ | wincmd p | diffthis
endif


"vim支持中文显示   
set fileencodings=gbk,utf-8,gb232
set cst
" 语法高亮
set syntax=on

"显示行号
set number

" 侦测文件类型
filetype on

" 载入文件类型插件
filetype plugin on
  
"搜索忽略大小写
set ignorecase
" 有一个或以上大写字母时仍大小写敏感
set smartcase 
"搜索逐字符高亮
set hlsearch
set incsearch

" 总是显示状态行
set laststatus=2

" 在编辑过程中，在右下角显示光标位置的状态..
set ruler           

" 命令行（在状态行下）的高度，默认为1，这里是2
set cmdheight=1

" 启动的时候不显示那个援助索马里儿童的提示
set shortmess=atI

" 高亮显示匹配的括号
set showmatch

" 匹配括号高亮的时间（单位是十分之一秒）
set matchtime=5

" 我的状态行显示的内容（包括文件类型和解码）
set statusline=[%F]%m%r%h%w\ \ \ \ [FORMAT=%{&ff}]\ [TYPE=%Y]\ [ENCODE=%{&enc}]\ [POS=%l,%v][%p%%]\ [%t]
"set statusline=%F%m%r%h%w\ [[ENCODE=%{&enc}]\FORMAT=%{&ff}]\ [TYPE=%Y]\ [POS=%l,%v][%p%%]\ %{strftime(\"%d/%m/%y\ -\ %H:%M\")}
"set statusline=[%F]%y%r%m%*%=[Line:%l/%L,Column:%c][%p%%]
 
" 允许backspace和光标键跨越行边界
set whichwrap+=<,>,h,l

set nobackup

" 在处理未保存或只读文件的时候，弹出确认
set confirm

" 自动缩进
set autoindent
set cindent

" 缩进和制表符宽度设为4，并用空格代替制表符
set shiftwidth=4
set tabstop=4
"set expandtab

colorscheme desert

map  <F12> :!ctags -R --c++-kinds=+p --fields=+iaS --extra=+q .<CR>
""""""""""""""""""""""""""""""
" Tag list (ctags)
""""""""""""""""""""""""""""""
 let Tlist_Ctags_Cmd = '/usr/bin/ctags'
 let Tlist_Show_One_File = 1     
   let Tlist_Exit_OnlyWindow = 1 
   "let Tlist_Auto_Open=1       
   set tags=tags;
   "set autochdir

   
   """"""""""""""""""""""""""""""
   " winManager setting
   """"""""""""""""""""""""""""""
   "设置界面分割
   let g:winManagerWindowLayout = "BufExplorer,FileExplorer|TagList"
   "let g:winManagerWindowLayout = "TagList|FileExplorer,BufExplorer"
         
   "设置winmanager的宽度，默认为25
   let g:winManagerWidth = 30
   "如果winmanager窗口是最后一个窗口，则退出vim
   "let g:persistentBehaviour = 0          
   "定义打开关闭winmanager按键
   nmap <silent> <F8> :WMToggle<cr>
   
   
   
   """""""""""""""""""""""""""""
   "VimGDB
   """"""""""""""""""""""""""""""
   "let g:vimgdb_debug_file = ""
   "run macros/gdb_mappings.vim 
   "":syntax enable			" enable syntax highlighting
   "":set previewheight=12		" set gdb window initial height
   "":run macros/gdb_mappings.vim	        " source key mappings listed in this
   ""                                     " document
   "":set asm=0                           " don't show any  assembly stuff
   "":set gdbprg=gdb_invocation           " set GDB invocation  string (default'gdb')

   " 设置vim插件 c-support的时间格式
   let g:C_FormatDate            = '%F'



" Open and close the taglist.vim separately 
nmap wm  :TrinityToggleTagList<CR> 

" Open and close the srcexpl.vim separately 
nmap ex :TrinityToggleSourceExplorer<CR> 

" cscope support begin 
"
if has("cscope")
		set csprg=/usr/bin/cscope
		set csto=0
		set cst
		set nocsverb
		" add any database in current directory
		if filereadable("cscope.out")
		    cs add cscope.out
		" else add database pointed to by environment
		elseif $CSCOPE_DB != ""
		    cs add $CSCOPE_DB
		endif
		set csverb
endif

map j gj
map k gk

""为方便复制，用<F2>开启/关闭行号显示:
function! HideNumber()
  if(&relativenumber == &number)
    set relativenumber! number!
  elseif(&number)
    set number!
  else
    set relativenumber!
  endif
  set number?
endfunc
"nnoremap <F2> :call HideNumber()<CR>
nmap <C-N> :call  HideNumber()<CR>

"" Save and quit vimu 
" nmap <F2>  :w!<CR> 
"
"" Save only 
nmap <F3>  :q!<CR> 
"
"" Quit vim without save
nmap <F4>  :wq!<CR> 
"
"" Quit vim without save
nmap <F5>  :vsp  
"
"" Save and quit vim 

" Open and close all the three plugins on the same time 
nmap <C-F11>   :TrinityToggleAll<CR> 

"系统剪切板使用register *
map <C-c> "*y
map <C-v> "*p
nmap <C-s> :w!<CR>
