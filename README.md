# IntellijVim

To reload file:
:source ~/.ideavimrc 

--------------------

--------------------

set number relativenumber
set idearefactormode=keep
set ideajoin
set surround
set easymotion

let mapleader = " "

nnoremap Y y$

"keep it centered
nnoremap n nzzzv
nnoremap N Nzzzv
nnoremap J mzJ`z

"undo break points
inoremap , ,<C-g>u
inoremap . .<C-g>u
inoremap ! !<C-g>u
inoremap ? ?<C-g>u

"Jumplist mutations
nnoremap <exp> k (v:count > 5 ? "m'" .  v.count : "") . 'k'
nnoremap <exp> j (v:count > 5 ? "m'" .  v.count : "") . 'j'

"Moving text (first 2 lines doesn't work in ideaVim)
"vnoremap J :m '>+1<CR>gv=gv
"vnoremap K :m '<-2<CR>gv=gv
noremap <C-j> :m +1<CR>
nnoremap <C-k> :m -2<CR>
inoremap <C-j> <Esc>:m +1<CR>gi
inoremap <C-k> <Esc>:m -2<CR>gi

"exit remap
"inoremap jk <Esc>
"set timeoutlen=1000

" system clipboard
nnoremap <leader>y "+y
vnoremap <leader>y "+y
nmap <leader>Y "+Y

nmap <leader>p "+p
vmap <leader>p "+p

nnoremap <leader>d "_d
vnoremap <leader>d "_d

" actions
nmap <C-h> <action>(PreviousTab)
nmap <C-l> <action>(NextTab)
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
