# Working with files and directory (touch, mkdir, cp, mv, rm, shred)

_creating a new file or updating the timestamps if the file already exists_  
`touch filename`

_creating a new directory_  
`mkdir dir1`

_creating a directory and its parents as well_  
`mkdir -p mydir1/mydir2/mydir3`

## The cp command

_copying file1 to file2 in the current directory_  
`cp file1 file2`

_copying file1 to dir1 as another name (file2)_  
`cp file1 dir1/file2`

_copying a file prompting the user if it overwrites the destination_  
`cp -i file1 file2`

_preserving the file permissions, group and ownership when copying_  
`cp -p file1 file2`

_being verbose_  
`cp -v file1 file2`

_recursively copying dir1 to dir2 in the current directory_  
`cp -r dir1 dir2/`

_copy more source files and directories to a destination directory_  
`cp -r file1 file2 dir1 dir2 destination_directory/`

## The mv command

_*renaming file1 to file2*_  
`mv file1 file2`

_*moving file1 to dir1*_  
`mv file1 dir1/`

_*moving a file prompting the user if it overwrites the destination file*_  
`mv -i file1 dir1/`

_*preventing a existing file from being overwritten*_  
`mv -n file1 dir1/`

_*moving only if the source file is newer than the destination file or when the destination file is missing*_  
`mv -u file1 dir1/`

_*moving file1 to dir1 as file2*_  
`mv file1 dir1/file2`

_*moving more source files and directories to a destination directory*_  
`mv file1 file2 dir1/ dir2/ destination_directory/`

## The rm command

_removing a file_  
`rm file1`

_being verbose when removing a file_  
`rm -v file1`

_removing a directory_  
`rm -r dir1/`

_removing a directory without prompting_  
`rm -rf dir1/`

_removing a file and a directory prompting the user for confirmation_  
`rm -ri fil1 dir1/`

_secure removal of a file (verbose with 100 rounds of overwriting)_  
`shred -vu -n 100 file1`
