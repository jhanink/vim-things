# Vim Things

## `install`
* install brew
  * `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
* install vim
  * `brew install vim --override-system-vim --HEAD`
  * `cd /usr/bin && sudo mv vim BAK_vim && sudo ln -s /usr/local/Cellar/vim/HEAD/bin/vim vim`
  * if __Operation not permitted__
    * reboot and press `cmd+r`
    * select __Utilities > Terminal__ from the menu
    * `csrutil disable && reboot`
## `selection`
* `v` start visual select
* `SHIFT+v` start visual line select
* easier vim install
  * `brew install vim`
  * `brew install --with-python3 vim`
    * https://stackoverflow.com/questions/41452121/how-to-enable-python-on-vim-version-8-for-mac
  * `brew link vim --overwrite`

## `moving`
* `gg` top of file
* `shift+G` bottom of file
* \`\` returns to the previous line number before a jump
* `ma` sets a `mark` position labeled `a`
  * jump to label `a` with \``a`

## `find (grep) in files`
* `:noautocmd vimgrep "pattern" **/*.*`
* `:Ggrep` with vim-fugitive
* `:e` to reload
* `:cw` to list occurrences in quickfix

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
* `:Vex` open directory tree in vertical split

## `buffers`
* `:e.` browse directory to edit a file
* `:ls` or `:buffers` show the open file buffers
* `:bn` next buffer
* `:bp` previous buffer
* `:b 1` open (switch to) the file at buffer 1
* `:bd` or `:bw` remove current or numbered buffer
* `:vsp | b<n>` open buffer <n> in vertical split pane
* `:vsp <filename>` open a file in vertical split pane
* `:sp` for horizontal splits
* `:q` to close the split
* `ctrl+w` then left/right arrow keys to move between panes
* `ctrl+w+w` to move to next pane
   * shows hidden pane after a maximize
* `ctrl+w` then `=` to normalize size of all panes
* `ctrl+w` then `|` to maximize size of current pane
* `ctrl+w` then `r` to rotate the panes to the right
* `ctrl+w` then `o` closes all but current pane
* `ctrl+w` then (n)`<` make current pane smaller by (n)
* `ctrl+w` then (n)`>` make current pane larger by (n)

## `quick-fix`
* `:copen` Open the quickfix window
* `:ccl` Close it
* `:cw` Open it if there are "errors", close it otherwise (some people prefer this)
* `:cn` Go to the next error in the window
* `:cnf` Go to the first error in the next file

## `Command-T`
* `,t` list files
* `,b` list buffers
* `<C-v>` open file in vertical split

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
  * download the font __Input Mono__
    * [Input Mono font download](http://input.fontbureau.com/download/)
    * install the font using the native __Font Book__ application
    * set the terminal font to use __Input Mono__
    * in `~/.vimrc`
  * [other powerline fonts](https://github.com/powerline/fonts)

```sh
# .vimrc
set guifont=Input\ Mono
let g:Powerline_symbols = 'fancy'
let g:airline_powerline_fonts = 1
let g:airline#extensions#branch#enabled = 1
let g:airline_section_z = '%p%%  %l:%v'
# copy/paste without formatting 
noremap <C-c> "+y
noremap <C-v> "+p
```

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

## `etc`

* https://github.com/mhinz/vim-galore
* https://blog.mozhu.info/vimmers-you-dont-need-nerdtree-18f627b561c3
