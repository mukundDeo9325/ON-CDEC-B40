## Importance of File Permissions in Linux
```
drwxrwxr-x
d - file type --> dir 
rwx ---> owner permission ---> the creator 
rwx ----> group permission 
r-x ---> others permission ---> other users 
```
-----
```
test rw- ---> read,  write 
rw- ---> read write 
r-- ---> read 
```
## Explanation of rwx (read, write, execute) Permissions
```
r ---> read ---> 4 
w ----> write ---> 2
x ---> exicute ---> 1

u ---> user 
g ----> group 
o ---> other 

+ ---> add 
- ---> remove 
= ---> at least this level 

r --> read 
w ---> write 
x ---> exicute permission 
```
```
chmod ugo +-= rwx file.txt
```
## How Permissions are Displayed with ls -l
```
777 dir full permission rwxrwxrwx
                         7  7  7
666 file full permission rw-rw-rw-
                          6  6  6
```
## Example: Breaking Down the Permission String (e.g., -rwxr-xr--)
```
drwx(owner)rwx(group)r-x(other)
|
file type 
```
## Introduction to File Types
- system define file ## system has an acess to this file and managing them
```
d ----> dir 
- --> normal file 
l ---> link file 
p ---> pipe file 
s ---> soket file 
```
- user define file 
`.txt .mp4  .mp3 .md .yaml ---> user has an acess to this file `
