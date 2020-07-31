# Installation...

### Software Required...

1. Git Bash
2. Ubuntu Shell
3. Git (according to your os)

### TO check git is installed or not

```
git --version
```

# The terminal Commands

### Introduction to terminal(A way to interact with os)

```
cd /  --> to go to the root directory
cd mnt --> to go to the windows system
ls --> list all the files
cd foldername --> move the terminal to that folder
clear --> clear the screen
cd .. --> to go one directory backward
cd ~ --> to go the home directory
mkdir foldername --> this will create a folder with given folder name
cd path --> to move to that path
cd== change directory
```

### working with files and directory

```
rm -rf foldername --> this will remove the folder with foldername and everything inside it
-rf => this is to specify that we are removing a folder instead of file (it is known as flag)
rm filename.extension --> to remove the file with filename with given extension
touch filename.extension --> this will create the file with given extension
touch => it does not work on pwershell
echo $null >> filename.extension => this is used to create the filename on powershell
```

# Git Basics

[Git command cheatsheet](https://www.github.com/joshnh/Git-Commands)

### Creating a new repository

```
git init --> intialise the git repository
git add . --> add all the files to the staging area
git add filename --> add the file to the staging area
git status --> status of the staging area
git commit -m "message" --> commiting to the file
git rm nameoffile.extension --> this will remove the file from the staging area

```
