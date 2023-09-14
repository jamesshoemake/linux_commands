# VIM

_Modes of operation: Command, Insert, and Last Line Modes._  
`VIM Config File: ~/.vimrc`

### Entering the Insert Mode from the Command Mode

_insert before the cursor_  
`i`  
_insert at the beginning of the line_  
`I`  
_insert after the cursor_  
`a`  
_insert at the end of the line_  
`A`  
_insert on the next line_  
`o`

### Entering the Last Line Mode from the Command Mode

`:`

### Returning to Command Mode from Insert or Last Line Mode

`ESC`

### Shortcuts in Last Line Mode

_write/save the file_  
`w!`  
_quit the file without saving_  
`q!`  
_save/write and quit_  
`wq!`  
_undo to the last saved version of the file_  
`e!`  
_set line numbers_  
`set nu`  
_unset line numbers_  
`set nonu`  
_syntax on|off_  
`%s/search_string/replace_string/g`

# Shortcuts in Command Mode

_remove char under the cursor_  
`x`  
_cut the current line_  
`dd`  
_cut 5 lines_  
`5dd`  
_save and quit_  
`ZZ`  
_undo_  
`u`  
_move to the end of file_  
`G`  
_move to the end of line_  
`$`  
_move to the beginning of file_  
`0 or ^`  
_move to line n_  
`:n (Ex :10)`  
_select the current line_  
`Shift+v`  
_yank/copy to clipboard_  
`y`  
_paste after the cursor_  
`p`  
_paste before the cursor_  
`P`  
_search for string forward_  
`/string`  
_search for string backward_  
`?string`  
_next occurrence_  
`n`  
_previous occurrence_  
`N`

### Opening more files in stacked windows

`vim -o file1 file2`

### Opening more files and highlighting the differences

`vim -d file1 file2`

_move between files_  
`Ctrl+w`
