# Viewing files (cat, less, more, head, tail, watch)

_displaying the contents of a file_
`cat filename`

_displaying more files_  
`cat filename1 filename2`

_displaying the line numbers_  
`can -n filename`

_concatenating 2 files_  
`cat filename1 filename2 > filename3`

_viewing a file using less_  
`less filename`

### less shortcuts:

`h => getting help`  
`q => quit`  
`enter => show next line`  
`space => show next screen`  
`/string => search forward for a string`  
`?string => search backwards for a string`  
`n / N => next/previous appearance`

_showing the last 10 lines of a file_  
`tail filename`

_showing the last 15 lines of a file_  
`tail -n 15 filename`

_showing the last lines of a file starting with line no. 5_  
`tail -n +5 filename`

_showing the last 10 lines of the file in real-time_  
`tail -f filename`

_showing the first 10 lines of a file_  
`head filename`

_showing the first 15 lines of a file_  
`head -n 15 filename`

_running repeatedly a command with refresh of 3 seconds_  
`watch -n 3 ls -l`
