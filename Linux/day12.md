## link count
Link count indicates the number of hard links associated with a file or directory. A hard link is an additional name for an existing file on the filesystem. Each hard link points to the same inode (data structure) on the disk.
- file = link count 1
- directory = link count 2 + number of subdirectories

## difference between hard link and soft link
* Hard Link:
  - Points directly to the inode of a file.
  - Cannot span across different file systems.
  - If the original file is deleted, the hard link still retains access to the data.

* Soft Link (Symbolic Link):
  - Points to the file name and path.
  - Can span across different file systems.
  - If the original file is deleted, the soft link becomes a broken link and no longer points to valid data.
<img width="617" height="295" alt="Screenshot 2026-01-30 at 8 04 54 PM" src="https://github.com/user-attachments/assets/e4d7efc1-7e0e-4011-9047-e833b8a242f3" />

## sudo 
The `sudo` command allows a permitted user to execute a command as the superuser or another user, as specified by the security policy. It is commonly used to perform administrative tasks that require elevated privileges.

how to create and normal user without sudo privileges:
* modify /etc/sudoers file using visudo command:
  ```bash
  vim /etc/sudoers
  ```
  - `username ALL=(ALL:ALL) ALL`  --> to give sudo privileges

## to change to root user use 
```bash
sudo -i
```



## su --> switch user
The `su` command is used to switch to another user account in a Linux system. By default, it switches to the root user if no username is provided. It prompts for the target user's

## difference between regular user and sudo user
* Regular User:
  - Has limited permissions and can only perform actions allowed by the system administrator.
  - Cannot execute commands that require elevated privileges.
  
* Sudo User:        
  - Has the ability to execute commands with superuser privileges using the `sudo` command.
  - Can perform administrative tasks as permitted by the system administrator.

example:
sudo <command>  --> execute command with superuser privileges
