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
* \<leader\>h: Move to window on the left
* \<leader\>l: Move to window on the right
* \<leader\>j: Move to window on the bottom
* \<leader\>k: Move to window on the top

* \<leader\>u: Show undo tree

* \<leader\>pv: Open up file tree

* \<leader\>ps: Project Search searches using ripgrep (Make sure to install ripgrep on your system)

* \<leader\>ps: (Project Search) searches for stuff using ripgrep

* \<leader\>gd: Go to definition
* \<leader\>gr: Go to references  

## VIM Movements P2: 5 moves to make you better ked
* Remap Ctrl-c or Ctrl-open bracket to Esc 
  ```vimscript
  inoremap <C-c> <esc>
  ```
  Instead of using the CAPS LOCK key for Esc, you can use it for CTRL.

* When using f and t, you can use `,` to go backwards and `;` to go forwards to search for the same letter without repeating the same command
* Use `c` instead of `d` to enter insert mode
* You can use `i` and `a` in conjunction with c or d to remove whatever's inside {}, [], "", '', etc.
  E.g. ci" will delete everything within the following string: "Hello, world".
  ca" will delete everything inside the string as well as the "". 
* Marks allow jumping to points in a file: `mJ` will create a mark called J. `'J` will jump to the mark. Note: Capital letter are marks that are unique across multiple files while lowercase letters are for local file marks.
* Bonus remap allows you to move highlighted regions up or down:
  ```vimscript
  vnoremap J :m '>+1<CR>gv=gv
  vnoremap K :m '<-2<CR>gv=gv
  ```
