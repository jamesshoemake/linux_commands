# File Timestamps and Date

 
*displaying atime*  
`ls -lu`
 
*displaying mtime*  
`ls -l`  
`ls -lt`
 
*displaying ctime*  
`ls -lc`
 
*displaying all timestamps*  
`stat file.txt`  
 
*displaying the full timestamp*  
`ls -l --full-time /etc/`
 
*creating an empty file if it does not exist, update the timestamps if the file exists*  
`touch file.txt`  
 
*changing only the access time to current time*  
`touch -a file`  
 
*changing only the modification time to current time*  
`touch -m file`  
 
*changing the modification time to a specific date and time*  
`touch -m -t 201812301530.45 a.txt`  
 
*changing both atime and mtime to a specific date and time*  
`touch -d "2010-10-31 15:45:30" a.txt`  
 
*changing the timestamp of a.txt to those of b.txt*  
`touch a.txt -r b.txt`  
 
*displaying the date and time*  
`date`  
 
*showing this month's calendar*  
`cal`  
 
*showing the calendar of a specific year*  
`cal 2021`  
 
*showing the calendar of a specific month and year*  
`cal 7 2021`  
 
*showing the calendar of previous, current and next month*  
`cal -3`  