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
git config --global user.email "youremail" --> this will set the user email this command is run once for configuration
git config --global user.name "your name" --> this will set the user name this command is run once for configuration
git --help --> this will open the list of all git commads
git commit --help --> this will open the manual for the git commit
git commit -a -m "your message" --> this will commit all the tracked files with the commit message
git log --> this will give the list of all the commits you have made
git log --oneline --> this will show all the commits in a single line
git rm nameoffile.extension --> this will remove the file from the repository
git rm -f nameoffile.extension --> this will remove the file from repository forcefully
git rm --cached nameoffile.extension --> this will remove the file from the staging area
```

### Tracking our git commit history

```
git checkout commit-id  ===> this will move to that state of time when the particular commit was made

*** this will not delete are commit we are just going back in time

git checkout master ==> this will take you back to the latest commit
```

### git revert and git reset

    * checkout helps us to go back in time but how to stay their permenately.
    * git revert is a little bit safer than git reset because it goes back in time to only one commit and reverts the changes and make a new commit with new message
    * you can also revert the revert commit
    * there are three different stages of git reset soft mix and hard . soft is just like git checkout and hard is like hard reset.
    * git reset resets all the commit upto that commit

```
git revert commit id ==>  reverts the changes made int that commit id
git reset --hard  commit id ==> resets all the commit upto that commit id
```

### create a .gitignore file

    * it is a file that has a list of all the files and directory that we do not want to track.
    *

```

```
