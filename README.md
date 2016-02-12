# Vim Things

## `selection`
* `SHIFT+v` visual line select

## `editing`
* `u` undo previous 
* `ctrl+r` redo the undo 
* `daw` delete a word
* `caw` change a word (deletes and then goes into insert mode)
* write a visual selection to a file `:w temp`
* search/repl in a visual selection `:s/patt/subs/g`
* `>>` indent line/selection
* `=` format indentation line/selection
* `gg=G` indent entire file
* `:qa` close all buffers

## `buffers`
* `:e.` browse directory to edit a file
* `:ls` or `:buffers` show the open file buffers
* `:bn` next buffer
* `:bp` previous buffer
* `:b 1` open (switch to) the file at buffer 1
* `:bd` or `:bw` remove current or numbered buffer
* `vsp | b<n>` open buffer <n> in vertical split pane
* `vsp <filename>` open a file in vertical split pane
* `sp` for horizontal splits
* `:q` to close the split
* `ctrl+w` then arrow keys to switch between split panes
* `ctrl+w+w` to move to next pane
   * shows hidden pane after a maximize
* `ctrl+w` then `=` to normalize size of all panes
* `ctrl+w` then `|` to maximize size of current pane
* `ctrl+w` then `r` to swap the left and right panes
* `ctrl+w` then `t` to move the pane to a tab view
* `ctrl+w` then `o` closes all but current pane
* `ctrl+w` then (n)`<` make current pane smaller by (n) 
* `ctrl+w` then (n)`>` make current pane larger by (n)


## `shell`
* `!<command>` to run a command in the shell
* `!ls` run `ls` in the shell
* `:shell` to open the shell. then return to vim with `exit`

## `plugins`
* [vim-plug](https://github.com/junegunn/vim-plug)
   * add list of plugins to `~/.vimrc`
   * to install, run `:PlugInstall` from vim
   * to update, run `:PlugUpdate`
* `matze/vim-move` - keyboard shortcuts to move line/selection up/down
* `powerline/powerline` - awesome in-editor info bar
* `Bling/vim-airline` - cool info bar 
* `easymotion/vim-easymotion` - fuzzy search, etc
* `wincent/Command-T` - easily open files and buffers with `,t`
   * after a `:PlugUpdate`
   * go to `~/.vim/plugged/Command-T`
   * run `rake make`
   * `git status`, then checkout the changed files
   * then run `:PlugUpdate` again to verify
* `w0ng/vim-hybrid` - BEST color theme
* `tomasr/molokai` - GOOD color theme
* `pangloss/vim-javascript` - javascript syntax, indentation support, etc

