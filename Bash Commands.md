#Bash Commands with Use and Test Cases:-
_____________________________________________________________________________________________________________________

 File and Directory Commands
_______________________________

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

-----------------------------------------------------------------

File Viewing and Editing
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

------------------------------------------------------------------

 File Search and Permissions
____________________________

15. find - Search files/directories

     `find . -name ".txt"`

16. grep - Search text in file

     `grep "hello" file.txt`

17. chmod - Change file permissions

     `chmod 755 script.sh`

18. chown - Change file owner

     `sudo chown user:user file.txt`

-----------------------------------------------------------------

System Information and Monitoring
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

-------------------------------------------------------------------

Archiving and Compression
__________________________

26. tar - Archive files

     `tar -cvf archive.tar folder/`

27. gzip - Compress files

     `gzip file.txt`

28. gunzip - Decompress gzip

     `gunzip file.txt.gz`

--------------------------------------------------------------------

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

--------------------------------------------------------------------

Networking Commands
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

--------------------------------------------------------------------

Looping and Scripting
_______________________

38. for - Loop

     `for i in 1 2 3; do echo $i; done`

39. while - While loop

     `while true; do echo "Looping"; sleep 1; done`

40. if - Conditionals

     `if [ -f file.txt ]; then echo "Exists"; fi`

----------------------------------------------------------------------

Reading and Writing contents
_____________________________

41. echo - Print text

     `echo "Hello"`

42. read - Read input

     `read name; echo "Welcome $name"`

----------------------------------------------------------------------

Package Management (Debian/Ubuntu)
___________________________________

43. apt update - Refresh package index

     `sudo apt update`

44. apt install - Install package

     `sudo apt install vim`

45. apt remove - Remove package

     `sudo apt remove vim`

-----------------------------------------------------------------------

Example Test Script

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
