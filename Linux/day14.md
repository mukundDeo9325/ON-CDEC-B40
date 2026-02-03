## umask 
```
full permission - umask = defalt file / dir permission 

r - 4
w - 2
x - 1

local user umask = 002
dir = 777 - 002 = 775
            rwx rwx r-x

file = 666 - 002 = 664
            rw-rw-r--
            

root user umask = 022

dir  777 - 022 = 755 
                  rwx r-x r-x

file = 666 - 022 = 644
                   rw-r--r--

```
```
umask 044 ## temporary umask set

777 - 044 = 733 rwx-wx-wx
666 -  044   = 622 rw--w--w-

r-4 w-2 x-1
```
## how to change umask 
### temporary umask 
umask 033 

### permenanant umask 
.bashrc         ##change 
source .bashrc  ## (file run )

## for chnaging the file permission after creation 
`chmod ugo +-= file/dir`


linux serching and filter utilities 

## commands 

- cat --> concatinate file containtaints 
- grep --> file containent scerch ;

`cat file.txt | grep <charector>`

- sort --> to sort the files in alfabatical order 
- uniq ---> not showing duplicate data
- https://www.redhat.com/en/blog/uniq-command-lists 
`sort file.txt | uniq`

- find --> fiend the file (size, type, date ,name)

- head ---> print first 10 lines
 `head -n 1 /etc/passwd` ## number of  1 line from top

- tail ---> print last 10 line
 `tail -n 2 /etc/passwd`  ## number of 2 lines from bottom  
- Overview of Key Utilities: grep, cat, sort, UNIQUE

`cat file.txt | grep <charector>`
`sort file.txt | uniq`
`head -n 1 /etc/passwd`
`tail -n 2 /etc/passwd`

## practice (HW)
- read file using grep 
- read file using cat
- read file using sort  
- read file using uniq 
- see the difference between all the commands 

scerch file using find 
- scerch using name 
- scerch using type 
- scerch using size 


- Basic Syntax of FIND

---------------------------------
```
find /etc -size 1M
   31  find /etc -type f -iname "*.txt"
   32  find /etc -type f -iname "*.conf"
   33  find /etc -type f -iname "*.conf" --help
   34  touch file 
   35  lsw
   36  ls
   37  l
   38  ls
   39  ls -ltr
   40  find /etc -type f -mtime -1
   41  find /root -type f -mtime -1
   42  find /etc -type f -mtime -10
   43  find /root -type f -mtime -10
   44  find /root -type f -mtime -100
   45  find /root -type f -mtime -10
   46  head /etc/passwd
   47  tail /etc/passwd
   48  tail -n 2 /etc/passwd
   49  head -n 1 /etc/passwd
   22  man find 
```







