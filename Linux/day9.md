
---
## Managing Users and Permissions in Linux
- currently user is effective 
`whoami` 
- all user list 
`cat /etc/passwd`

UID 
`root ---> 0 
 local user --> 1000 to 65536+ /home/username
 system user ---> 1 to 999 
`

# adding an user to linux system 
`adduser <username>` - affect the user related files , crete home dir /home/username , and password permision 
`useradd <username>` - only add new user to linux system without add home dir to /home, not assing with password 

swich from one user to another 
`su username` ---> only  root 
`sudo -i ` ----> to switch to root user only sudo user can switch into root 

## adding new group in linux 
- `groupadd <groupname>`
- adding an user to that group `usermod -aG <groupname> <username>`
- check all the group in wich user is added `groups <username>`
- to check history `history`(show all the command run by that user) ---history is userspecific








