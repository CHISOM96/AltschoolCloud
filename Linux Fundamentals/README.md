# Linux Fundamentals

## Problem
Your login name: altschool i.e., home directory /home/altschool. The home directory contains the following sub-directories: code, tests, personal, misc Unless otherwise specified, you are running commands from the home directory.

1. Change directory to the tests directory using absolute pathname
2. Change directory to the tests directory using relative pathname
3. Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory
4. Create an empty file named fileB in the misc directory. Populate the file with dummy content afterward
5. Copy contents of fileA into fileC
6. Move contents of fileB into fileD
7. Create a tar archive called misc.tar for the contents of misc directory
8. Compress the tar archive to create a misc.tar.gz file
9. Create a user and force the user to change his/her password upon login
10. Lock a user's password
11. Create a user with no login shell
12. Disable password-based authentication for ssh
13. Disable root login for ssh

**Mode of submission:**
You are going to push the required commands to your github repositories.

Deadline: 10th Feb 2024

## Solution
1. Change directory to the tests directory using absolute pathname
```cd /home/altschool/tests```
![Change directory to the tests directory using absolute pathname](Images/1.PNG)
2. Change directory to the tests directory using relative pathname
```cd ./tests```
![Change directory to the tests directory using relative pathname](Images/2.PNG)
3. Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory
```echo "Hello A" > fileA```
![Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory](Images/3.PNG)
4. Create an empty file named fileB in the misc directory. Populate the file with dummy content afterward
```echo > fileB```
![Create an empty file named fileB in the misc directory. Populate the file with dummy content afterward](Images/4.PNG)
5. Copy contents of fileA into fileC
```sudo cp fileA fileC```
![Copy contents of fileA into fileC](Images/5.PNG)
6. Move contents of fileB into fileD
```mv fileB fileD```
![Move contents of fileB into fileD](Images/6.PNG)
7. Create a tar archive called misc.tar for the contents of misc directory
```sudo tar -cvf misc.tar ./misc```
![Change directory to the tests directory using absolute pathname](Images/7.PNG)
8. Compress the tar archive to create a misc.tar.gz file
```sudo gzip misc.tar```
![Compress the tar archive to create a misc.tar.gz file](Images/8.PNG)
9. Create a user and force the user to change his/her password upon login
```sudo useradd piano && sudo passwd --expire piano```
![Create a user and force the user to change his/her password upon login](Images/9.PNG)
10. Lock a user's password
```sudo passwd --lock piano```
![Lock a user's password](Images/10.PNG)
11. Create a user with no login shell
```sudo adduser --system --no-create-home --shell /usr/bin/nologin amapiano```
![Create a user with no login shell](Images/11.PNG)
12. Disable password-based authentication for ssh
```sudo nano /etc/ssh/sshd_config && sudo systemctl restart sshd```
![Disable password-based authentication for ssh](Images/12.PNG)
13. Disable root login for ssh
```sudo nano /etc/ssh/sshd_config && sudo systemctl restart sshd```
![Disable root login for ssh](Images/12.PNG)