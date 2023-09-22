# Dynamic Real-Time View of Processes(top)

## starting top

top

### top shortcuts while it's running

_getting help_  
`h`  
_manual refresh_  
`space`  
_setting the refresh delay in seconds_  
`d`  
_quitting top_  
`q`  
_display processes of a user_  
`u`  
_changing the display for the memory_  
`m`  
_individual statistics for each CPU_  
`1`  
_highlighting the running process and the sorting column_  
`x/y`  
_toggle between bold and text highlighting_  
`b`  
_move the sorting column to the left_  
`<`  
_move the sorting column to the right_  
`>`  
_entering the Field Management screen _  
`F`  
_saving top settings_  
`W`

## running top in batch mode (3 refreshes, 1 second delay)

top -d 1 -n 3 -b > top_processes.txt

## Interactive process viewer (top alternative)

_Installing htop_  
sudo apt update && sudo apt install htop  
htop
