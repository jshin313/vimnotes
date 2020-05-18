# Vim Notes from the Primeagen
[The Primeagen](https://www.youtube.com/playlist?list=PLm323Lc7iSW9kRCuzB3J_h7vPjIDedplM)

## Vim Movements P1 - Your First Moves
Don't use your arrow keys!

j, k, h, l: down, up, left, right  

w, b: jump forward by word, jump backwards by word  

f, t: jump to a letter, jump one before a letter  

%: Go to respective parenthesis, brace, etc.  

Ctrl-d, Ctrl-u: jump down half page, jump up half page  

{, }: jump up a block, jump down by a block  

V: highlight line and enter visual mode  

P, p: paste up a line, paste down a line  

U: Capitalize stuff that's highlighted  

Ctrl-a, ctrl-x: Increment var, decrement var  

o, O: Insert newline below current, insert newline above current line (both enter insert mode)  

I, A: Enter insert mode at first character on a line, enter insert mode at last character in the current line  


## Your first VimRC: How to setup your vim's vimrc
Source or "execute" everything in a file with `source %`.  
This applies changes made to .vimrc.  

Make sure to create the undodir at `~/.vim/undodir`  

Run the following command to install the plug vim plugin manager
```console
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

Open up the .vimrc and add in your plugins.
Then source the .vim with `:source %s`.
Then install plugins with `:PlugInstall`.

Make YCM work:
```console
$ cd ~/.vim/plugged/YouCompleteMe
$ python3 install.py
```

Add some nice remap to make thing easier:
* \<leader\> h: Move to window on the left
* \<leader\> l: Move to window on the right
* \<leader\> j: Move to window on the bottom
* \<leader\> k: Move to window on the top

* \<leader\> u: Show undo tree

* \<leader\> pv: Open up file tree

* \<leader\> ps: Project Search searches using ripgrep

* \<leader\> ps: (Project Search) searches for stuff using ripgrep

* \<leader\> gd: Go to definition
* \<leader\> gr: Go to references  

## VIM Movements P2: 5 moves to make you better ked
5. Remap Ctrl-c or Ctrl-{ to Esc
4. 
