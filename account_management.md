# Account Management
 
## IMPORTANT FILES
*users and info: username:x:uid:gid:comment:home_directory:login_shell*  
`/etc/passwd`
*users' passwords*    
`/etc/shadow`
*groups*   
`/etc/group`  
 
## creating a user account
`useradd [OPTIONS] username`  

### OPTIONS:

*create home directory*  
`-m`  

*specify another home directory*  
`-d <directory>` 

*comments*   
`-c "comment"`  

*shell*  
`-s`   

*specify the secondary groups (must exist)*  
`-G`  

*specify the primary group (must exist)*  
`-g`  

*Exemple:*  
`useradd -m -d /home/john -c "C++ Developer" -s /bin/bash -G sudo,adm,mail john`  
 
## changing a user account
*uses the same options as useradd*   
`usermod [OPTIONS] username`  

*Example:*  
*adding the user to two secondary groups*    
`usermod -aG developers,managers john`  
 
## deleting a user account
*-r removes user's home directory as well*    
`userdel -r username`   
 
## creating a group  
`groupadd group_name`    
 
## deleting a group  
`groupdel group_name` 
 
## displaying all groups
`cat /etc/groups`
 
## displaying the groups a user belongs to
`groups`  
 
## creating admin users
`add the user to sudo group in Ubuntu and wheel group in CentOS`  
`usermod -aG sudo john`  
 
 
## Monitoring Users
*displays logged in users*  
`who -H`  
*displays the current user and its groups*  
`id`  
*displays EUID*  
`whoami`  
 
## listing who’s logged in and what’s their current process.
`w`  
`uptime`  
 
## printing information about the logins and logouts of the users
`last`  
`last -u username`  