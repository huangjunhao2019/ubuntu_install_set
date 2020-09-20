# vim安装注意事项
可以使用的vimrc直接就位于当前文件夹下的vimrc中，这个vimrc是位于/etc/vim下的vimrc中，直接用这个vimrc代替/etc/vim下的vimrc即可。
## 1.主要功能
```` c
set nu
set tabstop=4
set nobackup
set cursorline
set ruler
set autoindent
set shiftwidth=4
set softtabstop=4
set ai
set showmatch
set foldmethod=syntax
set foldlevel=100
set cindent
set autoindent
inoremap ( ()<ESC>i
inoremap [ []<ESC>i
inoremap { {}<ESC>i
inoremap {<CR> {<CR><CR>}<ESC>k<ESC>i
inoremap < <><ESC>i
inoremap ' ''<ESC>i
inoremap " ""<ESC>i

````
其中需要注意的是inoremap {<CR> {<CR><CR>}<ESC>k<ESC>i，这实现了光标位于两个大括号之间，即第二行的位置，这里inoremap主要是起到代替的作用，即前面的部分被替代为后面的命令，这里主要是，光标会位于第二个大括号的紧前面，解决的方法，是让光标向上来一下，即esc下的k命令
## 2.注意的坑
千万不要去修改那个~/.vimrc，在更新之后好像就不可以使用了，郁闷啊，原来调试好的都没有了
