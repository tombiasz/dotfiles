scriptencoding utf-8
set encoding=utf-8

" VIM PLUG
if empty(glob('~/.vim/autoload/plug.vim'))
  silent !curl -fLo ~/.vim/autoload/plug.vim --create-dirs
    \ https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
  autocmd VimEnter * PlugInstall --sync | source $MYVIMRC
endif

call plug#begin('~/.vim/plugged')
  " Plug 'lifepillar/vim-solarized8'
  Plug 'altercation/vim-colors-solarized'
  Plug 'pangloss/vim-javascript'
  Plug 'othree/yajs.vim'
  Plug 'Raimondi/delimitMate'
  Plug 'itchyny/lightline.vim'
  Plug 'itchyny/vim-gitbranch'
  Plug 'ap/vim-buftabline'
  Plug 'junegunn/fzf', { 'dir': '~/.fzf', 'do': './install --all' }
  Plug 'junegunn/fzf.vim'
  Plug 'Shougo/deoplete.nvim'
  Plug 'roxma/nvim-yarp'
  Plug 'roxma/vim-hug-neovim-rpc'
  Plug 'carlitux/deoplete-ternjs'
  Plug 'ternjs/tern_for_vim', { 'do': 'npm install && npm install -g tern' }
  Plug 'scrooloose/nerdtree'
  Plug 'HerringtonDarkholme/yats.vim'
  " Plug 'mhartington/nvim-typescript', {'do': './install.sh'}
  Plug 'gertjanreynaert/cobalt2-vim-theme'
call plug#end()


" EDIT
set nocompatible
syntax on
set nowrap
set title
set showcmd
set backspace=indent,eol,start
set pastetoggle=<F1>
set mouse=a
set clipboard=unnamed

set history=1000
set undolevels=100


" INDENTATION
set expandtab
set shiftround
set autoindent
set copyindent

set shiftwidth=2
set softtabstop=2
set tabstop=2

autocmd Filetype html setlocal ts=4 sw=4 expandtab
autocmd Filetype python setlocal ts=4 sw=4 expandtab
autocmd Filetype javascript setlocal ts=2 sw=2 sts=0 expandtab


" VIEW
set scrolloff=5
set sidescrolloff=5
set sidescroll=1
set showmatch
set cursorline

set background=dark
" colorscheme solarized
colorscheme cobalt2


highlight CursorLine ctermbg=238
highlight Visual     ctermbg=238

set colorcolumn=81

set laststatus=2
set hidden
set showmode

set relativenumber

" set listchars=eol:~,tab:>.,trail:~,extends:>,precedes:<,space:.
set listchars=eol:~,tab:>.,trail:~,extends:>,precedes:<,
set list


" SEARCH
set hlsearch
set incsearch " incremental search
set gdefault
set ignorecase
set smartcase


" AUTOCOMPLETE
set wildmenu
set wildmode=list:full
set wildignore=*.swp,*.pyc,*.class


" MISC
set nobackup
set noswapfile
set visualbell
set noerrorbells

" KEYMAPPINGS
let mapleader="\<space>"
nnoremap <leader>w :bw<CR>
nnoremap <leader>h :bp<CR>
nnoremap <leader>l :bn<CR>
nnoremap <leader>/ :noh<CR>

" PLUGINS

" lightline
set laststatus=2
set noshowmode
let g:lightline = {
  \ 'colorscheme': 'wombat',
  \ 'active': {
  \   'left': [ [ 'mode', 'paste' ],
  \             [ 'gitbranch', 'readonly', 'filename', 'modified' ] ]
  \ },
  \ 'component_function': {
  \   'gitbranch': 'gitbranch#name'
  \ },
  \ }

" buftabline
let g:buftabline_indicators=1
let g:buftabline_numbers=1

" fzf
nnoremap <leader>p :Files<Cr>
nnoremap <leader>t :Ag<Cr>

" deoplete
let g:deoplete#enable_at_startup = 1
inoremap <expr><TAB>  pumvisible() ? "\<C-n>" : "\<TAB>"
let g:deoplete#sources#ternjs#types = 1
let g:deoplete#sources#ternjs#docs = 0

let g:deoplete#enable_ignore_case = 1
let g:deoplete#enable_smart_case = 1
let g:deoplete#enable_camel_case = 1
let g:deoplete#enable_refresh_always = 1
let g:deoplete#max_abbr_width = 0
let g:deoplete#max_menu_width = 0
let g:deoplete#omni#input_patterns = get(g:,'deoplete#omni#input_patterns',{})

let g:tern_request_timeout = 1
let g:tern_request_timeout = 6000
let g:tern#command = ["tern"]
let g:tern#arguments = ["--persistent"]
let g:deoplete#sources#tss#javascript_support = 1
let g:tsuquyomi_javascript_support = 1
let g:tsuquyomi_auto_open = 1
let g:tsuquyomi_disable_quickfix = 1

" nerdtree
map <leader>b :NERDTreeToggle<CR>
