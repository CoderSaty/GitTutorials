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
    * HEAD is always the currently selected commit

```
git revert commit id ==>  reverts the changes made int that commit id
git reset --hard  commit id ==> resets all the commit upto that commit id
```

### create a .gitignore file

    * it is a file that has a list of all the files and directory that we do not want to track.
    * the file does not have any name
    * create the file list all the files and directory you need to ignore commit the change

```
git rm - r --cached . ==> this will remove the cached memory from the staging area
```

### git branches

    * git branches are a way to create a separate development path without overiding or creating copies of your project
    * branches can be added deleted and merged just like regular commits
    * braches can be used to seperate different end goals of your project
    * create seperate bracnhes for each stage of developement.
    * you have to make the intial commit before creating any branch otherwise your  development branch will be considered as master branch
    * you have to make the commit in the similar manner you have to just switch to the required branch
    * be careful and cautiois on commiting something
    * Merging Branches :- bringing all the branches together
    * there are two merge commands one merges to current directory and the in the other command we can specify the source and destination
    * a branch can be defined as a chain of commits that does not interfere with other branch
    * HEAD is a pinter that will point to the current brach

```
    * git branch "name of the branch" ==> create a new branch with the given name
    * git checkout -b "name of the branch" ==> this will create the new branch with the given name and will switch to it.
    * git checkout master ==> this will help them to switch to master branch
    * git branch -a ==> this will list all the branch with a star on the current branch
    * git branch -d "name of the branch" ==> this will delete the specified branch
    * git  merge "name of the branch" => this will merge the specified branch with the current branch you are working on

```

### Github

    * what is github? => it is an application that allows you to store remote repo on their servers.
    * benefits :-
        1. provides a user friendly platform to interract with and manage your repo
        2. it is public and open source(social coding)
        3. used as a portfolio
        4. open oppurtunities you might not have with a local repo
        5. easy acess from any device
        6. industry standard
    * creating a github account
    * github documentation
    * creating first repo on github
    * there are various licesence
    * Issues (can be listed by the contributors)
    * pull request (anyone wants to pull your repo on their local site)
    * wiki (you can place the large documentation of your software here)
    * insights (records of the repository)
    * settings (delete, acess,change Name,collaborators)
    * deploy key (to deploy repo on some site)
