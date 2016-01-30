# vim things

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
* `:buffers` show the open file buffers
* `:b 1` open (switch to) the file at buffer 1
* `:bw 2` removes buffer 2 from buffers
