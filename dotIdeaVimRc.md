# IntellijVim

to refresh file:
:source ~/.ideavimrc

//--------------//

set number relativenumber
set idearefactormode=keep
set ideajoin
set surround
set easymotion

let mapleader = " "


inoremap jj <Esc>
set timeoutlen=1000

noremap <Esc> <nop>
nmap <S-Enter> O<Esc>
nmap <CR> o<Esc>

 noremap <C-j> :m +1<CR>
nnoremap <C-k> :m -2<CR>
inoremap <C-j> <Esc>:m +1<CR>gi
inoremap <C-k> <Esc>:m -2<CR>gi

" system clipboard
vmap <leader>y "+y
vmap <leader>d "+d
nmap <leader>y "+yy
nmap <leader>p "+p
nmap <leader>P "+P
vmap <leader>p "+p
vmap <leader>P "+P

" scrolling
nmap <leader>j <C-d>
nmap <leader>k <C-u>
vmap <leader>j <C-d>
vmap <leader>k <C-u>

" actions
nmap <leader>h <action>(PreviousTab)
nmap <leader>l <action>(NextTab)
nmap <leader>bd <action>(CloseEditor)
nmap <leader>i <action>(Generate)
nmap <leader>m <action>(Git.Menu)
nmap <leader>s <action>(QuickChangeScheme)
nmap <leader>/ <action>(ShowErrorDescription)
nmap <leader>e <action>(GotoNextError)
nnoremap <leader><leader> <C-Tab>

set NERDTree
let g:NERDTreeMapActivateNode='l'
let g:NERDTreeMapJumpParent='h'
