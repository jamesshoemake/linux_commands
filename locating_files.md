# Finding Files (find, locate)

## LOCATE

### updating the locate db

`sudo updatedb`

### displaying statistics

`locate -S`

### finding file by name

_filename is expanded to filename_  
`locate filename`

_the filename is case insensitive_  
`locate -i filename`  
_finding by exact name_  
`locate -b '\filename'`

_finding using the basename_  
`locate -b filename`

_finding using regular expressions_  
`locate -r 'regex'`

_checking that the file exists_  
`locate -e filename`

_showing command path_
`which command`  
`which -a command`

## FIND

### find PATH OPTIONS

_Example:_  
`find ~ -type f -size +1M => finding all files in ~ bigger than 1 MB`

_Options:_
`-type f, d, l, s, p`  
`-name filename`  
`-iname filename => case-insensitive`  
`-size n, +n, -n`  
`-perm permissions`  
`-links n, +n, -n`  
`-atime n, -mtime n, ctime n`  
`-user owner`  
`-group group_owner`
