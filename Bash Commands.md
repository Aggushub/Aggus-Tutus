# Bash Commands with Use and Test Cases:-
Bash commands are text-based instructions used in the Bash shell (Bourne Again SHell), which is one of the most widely used command-line interpreters in Linux and Unix-like systems. They allow users to interact with the system, control processes, manipulate files, and automate tasks. I made this list while learning the Bash scripting course from Udemy.

### Adminsitration Commands
__________________________

1. hostname - Shows the name of the system

`hostname` - shows your system name (ex. AggusSystem)

2. clear - It removes all the contents in the window to maintain good visibility. But it won't revoke the actions, functions or files

`clear` - resets the window to be like a new window.

3. id - It shows the ids of the user and the groups you are in

`id` - shows the userid and groupid

4. adduser - It allows you to add a regular user in the system

`adduser aggu` - It allows you to add a regular user named 'aggu' in the system

5. userdel - It allows you to delete a regular user from the system

`userdel aggu` - It deletes the regular user named 'aggu' from the system

6. su - It allows you to switch users

`su root` - It switches the user to the root user

7. groupadd - It allows you to add a new group in the system

`addgroup dev` - It adds a new group by the name of 'dev'

8. groupdel - It allows you to delete an existing group from a system

`groupdel dev` - It deletes the group 'dev' from the system

9.usermod -  It is used to modify an existing user account

`usermod -a -G docker joel` - This adds the user joel to the docker group while keeping their membership in other groups.

 Here's a complete guide to commonly used flags with `usermod`:

---

### 🔧 Common `usermod` Options

| Option | Description                                         | Example                              |
| ------ | --------------------------------------------------- | ------------------------------------ |
| `-a`   | Append to groups (only with `-G`)                   | `usermod -a -G sudo joel`            |
| `-G`   | Set **supplementary groups**                        | `usermod -G wheel joel`              |
| `-g`   | Set **primary group**                               | `usermod -g users joel`              |
| `-d`   | Set **home directory**                              | `usermod -d /newhome/joel joel`      |
| `-m`   | Move the content of old home to new (use with `-d`) | `usermod -d /newhome/joel -m joel`   |
| `-s`   | Set default **shell**                               | `usermod -s /bin/zsh joel`           |
| `-l`   | Change the **login name** (username)                | `usermod -l newname oldname`         |
| `-L`   | **Lock** the account (disable password login)       | `usermod -L joel`                    |
| `-U`   | **Unlock** the account                              | `usermod -U joel`                    |
| `-e`   | Set account **expiry date** (format: YYYY-MM-DD)    | `usermod -e 2025-12-31 joel`         |
| `-f`   | Set **inactive days** after password expiry         | `usermod -f 30 joel` (30 days grace) |

---

 Examples

1. Change shell to bash:

   ```bash
   usermod -s /bin/bash joel
   ```

2. Move user to a new home directory:

   ```bash
   usermod -d /home/newjoel -m joel
   ```

3. Lock a user account (temporarily disable login):

   ```bash
   usermod -L joel
   ```

4. Change username:

   ```bash
   usermod -l newjoel joel
   ```



* `usermod` requires **root privileges**.
* Always back up user data before making major changes like home directory move or username change.
* Use `id username` to check a user’s group memberships before and after changes.


---


### File and Directory Commands
---

1. ls - List files and directories

`ls /home` – Lists contents of '/home'

2. cd - Change directory

`cd /etc` – Moves to '/etc' directory

3. pwd - Print current working directory

`pwd` – Shows full path

4. mkdir - Create new directory

`mkdir testdir` – Creates `testdir` folder or directory

5. rmdir - Remove empty directory

`rmdir testdir` – Removes `testdir` folder or directory

6. touch - Create empty file

`touch file1.txt` – Creates file

7. cp - Copy file/directory

`cp file1.txt file2.txt` – Copies contents from file1.txt to file2.txt

8. mv - Move/rename files

`mv file1.txt newfile.txt` – Renames file

9. rm - Remove file/directory

`rm file2.txt` – Deletes file



### File Viewing and Editing
__________________________

10. cat - View file contents

	`cat file.txt`

11. more / less - View large files page by page

	`less /var/log/syslog`

12. head - Show first lines of file

	`head -n 5 file.txt`

13. tail - Show last lines of file

	`tail -n 5 file.txt`

14. nano / vi - Text editors in terminal

	`nano file.txt` – Opens file to edit



 ### File Search and Permissions
____________________________

15. find - Search files/directories

     `find . -name ".txt"`

16. grep - Search text in file

     `grep "hello" file.txt`

17. chmod - Change file permissions

     `chmod 755 script.sh`

18. chown - Change file owner

     `sudo chown user:user file.txt`



### System Information and Monitoring
__________________________________

19. uname - Show system info

     `uname -a`

20. top - View running processes

     `top`

21. ps - Show process status

     `ps aux | grep firefox`

22. df - Disk usage

     `df -h`

23. du - Disk usage of file/dir

     `du -sh /home/username`

24. free - Show memory usage

     `free -m`

25. uptime - Show system uptime

     `uptime`



### Archiving and Compression
__________________________

26. tar - Archive files

     `tar -cvf archive.tar folder/`

27. gzip - Compress files

     `gzip file.txt`

28. gunzip - Decompress gzip

     `gunzip file.txt.gz`



User Management
_________________

29. whoami - Current user

     `whoami`

30. adduser - Add user

     `sudo adduser newuser`

31. passwd - Change password

     `passwd`

32. su - Switch user

     `su - username`



### Networking Commands
____________________

33. ping - Check network

     `ping google.com`

34. ifconfig - Show network interfaces

     `ifconfig` (or `ip a`)

35. netstat - Show network connections

     `netstat -tuln`

36. curl - Download data from URL

     `curl http://example.com`

37. wget - Download file

     `wget http://example.com/file.zip`



### Looping and Scripting
_______________________

38. for - Loop

     `for i in 1 2 3; do echo $i; done`

39. while - While loop

     `while true; do echo "Looping"; sleep 1; done`

40. if - Conditionals

     `if [ -f file.txt ]; then echo "Exists"; fi`



### Reading and Writing contents
_____________________________

41. echo - Print text

     `echo "Hello"`

42. read - Read input

     `read name; echo "Welcome $name"`



### Package Management (Debian/Ubuntu)
___________________________________

43. apt update - Refresh package index

     `sudo apt update`

44. apt install - Install package

     `sudo apt install vim`

45. apt remove - Remove package

     `sudo apt remove vim`



## Example Test Script

```bash
#!/bin/bash

echo "Creating files..."
touch file1.txt file2.txt
echo "Hello" > file1.txt
cat file1.txt

echo "Copying file1 to file3..."
cp file1.txt file3.txt

echo "Listing all .txt files:"
ls .txt

echo "Removing file2..."
rm file2.txt

echo "Final files:"
ls
```

Run this script with: `bash script.sh`
