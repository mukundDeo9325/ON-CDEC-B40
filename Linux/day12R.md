## Linux Question 

1. what is linux
2. what is OS
3. types of os
4. first process which is running in linux : systemd
5. architecture of linux
6. diff CLI vs GUI
7. what are diff types of users preasent in linux
8. what are helping commands
9. what are 19 dir
10. ediitors : vim, nano
11. how to undo in vim
12. how to redo in vim
13.  how to save file in vim
14.  how to save file in nano
15. modes in edditor vim
16. user and group management

## Linux revision 
## OS ---> bridge between hardware and user 
```

## types of os 
1 desktop os : ---> genral user (windoes os macos )
2 server os : ---> enterprices linux 
3 mobile os : ---> Andriod IOS windows 
4 embaded os : ---> tv os 
5 Real time os : --> medical equipments ECG ECU 


2 server os : ---> enterprices linux 

## History 
UNIX ---> paid os 1970 (Bell lab)
LINUX ---> Free os Linus torwald 
v1 ---> non function 
v2 ----> 1991 ---> functional 

AWS 2006 ---> cloud computing 
Linux ---> using with cloud VM's 


Liunx kernal ---> yes (free kernal)
ARC + pakages manages 
Liunx OS ---> kernal + Pakeges 
ubuntu ---> 
redhat ---> provider 

Linux Flavours :
1 ubuntu 
2 redhat 
3 fedora 
4 centos 
5 arch linux 
6 alpine 
7 kali linux 


pakage mananeger 
apt and yum 

Linux    v/s  windows  
FREEE     |  PAID
GUI & CLI | GUI 
sequred   | less sequre
encrepted 
data      | not encrepted 


support and pakages ---> pricing 

---
19 dir 
| Directory | Purpose                        |
| --------- | ------------------------------ |
| `/home`   | User home directories          |
| `/etc`    | System configuration files     |
| `/var`    | Logs and variable data         |
| `/bin`    | Essential system commands      |
| `/usr`    | Installed software & libraries |
| `/tmp`    | Temporary files                |
| `/dev`    | Device files                   |  
| `/lib`    | System libraries               |
| `/opt`    | Optional software packages     |
| `/root`   | Root user home directory       |
| `/srv`    | Service data                   |
| `/boot`   | Boot loader files              |
| `/mnt`    | Mount points for external drives|
| `/proc`   | Process and kernel information  |
| `/sys`    | System information              |
| `/media`  | Removable media mount points    |
| `/run`    | Runtime variable data           |
| `/sbin`   | System administration binaries  |
| `/lib64`  | 64-bit system libraries         |

---

ls -l ---> longlist data files and dir 
whoami ----> current user 
cd ---> change dir 
mkdir ---> create empty dir 
pwd ----> present working dir 
cat ----> print contet file 
mv -----> move file/ dir source to destination and rename 
cp ----> copy file / -r ---> dir copy 
ls. ---> list current dir contents 
rm  -----> remove file / dir 
rmdir ----> empty dir remove 
chmod -----> permission change 
chown ----> ownership of user chnage 
touch ----> time stamp change / empty file 

file oprations 
head 
tail 
more 
less 
cat 


edditors : 
vim ---> most used command line edditor 
modes
command mode ---> yy, dd, yw, dw, p, R, /word 
`i dont want to enter in exituation mode but save and exit` --> Shift + xx  

insert mode ----> file eddit 
exicution mode -----> save quit :w q (! --> forcefull) (:set nu) (:no nu) 
visual mode ----> text selction y --> copy p ---> past d--> delete 

vi ----> privisous version of vim 
nano ----> new piko 
piko ----> beginer edditor  

helping command :
man ----> manual 
--help ---> provides help 
info ---> info 
whatis ---> helping camand info 

user and group management 
root # ---> administator 0
local $ ---> normal user 1000 to 65536+
system ---> sytem user 1 to 999

local $: 
adduser --> home dir and password 
useradd --> only user is added 
(only root user can add new user in linux system )

sudo ---> parent level permission to local user 
su ----> switch between two user 

sudo -i ---> to switch to root user 

passwd ---> set password to user 

`which are the files get affected when new user is addeed ?` 
when user is added get entry in this files 
1. /etc/passwd 
2. /etc/shadow 
3. /etc/group 
4. /etc/gshadow 
5. /var/spool/mail ---> mail dir added (allerts) #
and dir
- /home

group 
1. primary group ----> bydefalt group 
2. secondary group ---> user group for an user to done task in system 

groupadd groupname ---> adding new group 
usermod -aG username groupname---> user add to group 
gpasswd -d devuser devops   # to remove user from group 
---
files permission 
drwxrwxr-x
d --- file types (dir)
- ---> normal file 
l ---> link file
p ---> pipe file 
s ---> socket file 

r ---> read permission 4
w ---> write 2
x ---> exicute 1 

# (local user defalt file permission 644 
# local user defalt dir permission 755)


full permission for file - 666 
full permission for dir - 777 


full permission - umask (022-->local 002-->root)= defalt permision 

---
link count 
file - 1 + number of hardlink 
dir - 2 + number of subdir 

`diff between hard link vs soft link `
hardlink          | softlink 
backup souce file | sortcut source file 
affect link count 
of source file    | does not affect 

hard link sorce deleted--> usaebale 
softl link souce file delete ---> unusable (link broken)

inode : meteddeta of file 
         \--> file type and size date and time of creation 



* Regular User:
  - Has limited permissions and can only perform actions allowed by the system administrator.
  - Cannot execute commands that require elevated privileges.
  
* Sudo User:        
  - Has the ability to execute commands with superuser privileges using the `sudo` command.
  - Can perform administrative tasks as permitted by the system administrator.



file ----> no file can have exicute permision by defalt 
dir ---> exute permision --> file create : aceess you dir 

shell scripting exicutable files 

touch file 
+x ---> exicute permission 
file.sh---> shell file 
file.txt ---> txt file 
file ---> text file 

to crete an sudo user from normal user 
/etc/sudoers --> entry of normal user 

normal --> sudo user 

sudo command 

usr 1 
usr 2 


root --->x 
local user --> sudo permission assing --> work 








17 model 
LINUX ---> test ----> AWS ---> half / full test ---> DevOps 2 month  --->half syllabus full syllabus -->  final moc ---> placement 


30 mcq ---> online | QNA --> diff trainer 

shell scripting 
comunication 
azure 
GCP 


```