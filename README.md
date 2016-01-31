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
* `gg=G` indent entire file

## `buffers`
* `:e.` browse directory to edit a file
* `:ls` or `:buffers` show the open file buffers
* `:bn` next buffer
* `:bp` previous buffer
* `:b 1` open (switch to) the file at buffer 1
* `:bd` or `:bw` removes buffer 2 from buffers

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
* `tomasr/molokai` - color theme
* `pangloss/vim-javascript` - javascript syntax, indentation support, etc

