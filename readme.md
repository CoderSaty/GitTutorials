# Installation...

### Software Required...

1. Ubuntu Shell
2. Git (according to your os)

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
pwd ==> this will display the current working directory of the terminal
ls -la ==> in order to see all the hidden git files

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
git config --list --> this will list all of our settings
git --help --> this will open the list of all git commads
git commit --help --> this will open the manual for the git commit
git commit -a -m "your message" --> this will commit all the tracked files with the commit message
git log --> this will give the list of all the commits you have made
git log -- author="codersaty" ==> this will only show the commits made by author codersaty. you need not to type the full name laways.
git log --oneline --> this will show all the commits in a single line
git rm nameoffile.extension --> this will remove the file from the repository
git rm -f nameoffile.extension --> this will remove the file from repository forcefully
git rm --cached nameoffile.extension --> this will remove the file from the staging area
git diff ==> this will show the changes you have made {this only show the difference between working copy and repository}
git diff --staged ==> this will show the differences when the file is in staging area

```

### Tracking our git commit history

```
git checkout commit-id  ===> this will move to that state of time when the particular commit was made

*** this will not delete are commit we are just going back in time

git checkout master ==> this will take you back to the latest commit
```

### git revert and git reset

- checkout helps us to go back in time but how to stay their permenately.
- git revert is a little bit safer than git reset because it goes back in time to only one commit and reverts the changes and make a new commit with new message
- you can also revert the revert commit
- there are three different stages of git reset soft mix and hard . soft is just like git checkout and hard is like hard reset.
- git reset resets all the commit upto that commit
- HEAD is always the currently selected commit

```
git revert commit id ==>  reverts the changes made int that commit id
git reset --hard  commit id ==> resets all the commit upto that commit id
```

### create a .gitignore file

- it is a file that has a list of all the files and directory that we do not want to track.
- the file does not have any name
- create the file list all the files and directory you need to ignore commit the change

```
git rm - r --cached . ==> this will remove the cached memory from the staging area
```

### git branches

- git branches are a way to create a separate development path without overiding or creating copies of your project
- branches can be added deleted and merged just like regular commits
- braches can be used to seperate different end goals of your project
- create seperate bracnhes for each stage of developement.
- you have to make the intial commit before creating any branch otherwise your development branch will be considered as master branch
- you have to make the commit in the similar manner you have to just switch to the required branch
- be careful and cautiois on commiting something
- Merging Branches :- bringing all the branches together
- there are two merge commands one merges to current directory and the in the other command we can specify the source and destination
- a branch can be defined as a chain of commits that does not interfere with other branch
- HEAD is a pinter that will point to the current brach

```
git branch "name of the branch" ==> create a new branch with the given name
git checkout -b "name of the branch" ==> this will create the new branch with the given name and will switch to it.
git checkout master ==> this will help them to switch to master branch
git branch -a ==> this will list all the branch with a star on the current branch
git branch -d "name of the branch" ==> this will delete the specified branch
git  merge "name of the branch" => this will merge the specified branch with the current branch you are working on

```

### Github

- what is github? => it is an application that allows you to store remote repo on their servers.
- benefits :-
  1. provides a user friendly platform to interract with and manage your repo
  2. it is public and open source(social coding)
  3. used as a portfolio
  4. open oppurtunities you might not have with a local repo
  5. easy acess from any device
  6. industry standard
- creating a github account
- github documentation
- creating first repo on github
- there are various licesence
- Issues (can be listed by the contributors)
- pull request (anyone wants to pull your repo on their local site)
- wiki (you can place the large documentation of your software here)
- insights (records of the repository)
- settings (delete, acess,change Name,collaborators)
- deploy key (to deploy repo on some site)
- watch , Star , fork , clone and downloadig. (viewing other people repository)

### working with git remotely

#### conneecting to remote repo through our terminal

- A remote origin is a link to access your remote repository.

```
 git init ==> intialize the repo
 git remote add origin "url of the repo" ==> to connect with the remote repo the local repo
 git remote -v ==> to check whether the remote repo is connected or not (it will show us the remote origin we use to push and pull information)
```

#### Push & Pull System

```
git push ==> to push the change in your local machine to the  remote repo
git pull ==> to pull any remote repo in your local machine
```

#### pushing and pulling to and from a github repo

- create a readme file
- create a license file (license.md){MIT license (allow people to take your project and edit it)}
- create a .gitignore {you can also use a template for a particular tech}
- sometime when conflict arise you can google it ans=d resolve it manually

```
git pull -u origin master ==>  we have to write this command for the first time so that the pull can remember the branch
git pull ==> once pulled we can use this simply and we dont have to specify the branch
git push -u origin master ==> we have to write this command for the first time so that the push can remember the branch
git push ==> once pushed we can use this simply and we dont have to specify the branch
```

#### working with remote branches

- typical process :-
  1. create a new branch
  2. fix that error
  3. merge with master branch
  4. delete that branch

* we can push only one branch at a time to a remote repository.
* we can interact with our remote repo through push pull cycle.

-

```
git pull ==> get everything in local repo
git checkout -b rectify ==> creating a branch named rectify
** fix the error**
git add . ==> add to staging area
git commit -m "message" ==> commit the changes
git checkout master ==> switch to master branch
git merge rectify ==> merged to master branch
git push ==> push to github repo {this will push only the master branch not the rectify branch}
**now you need to remove the remote branch**
git push origin rectify ==> this will now push the rectify branch
** to remove the branch retify **
git push origin --delete rectify ==> deletes the remote rectify branch
```

### Git GUI (Sourcetree or Github Desktop)

- If we do not love working with terminal we can also use git gui such as sourcetree which is more user friendly. BTW I prefer terminal.

### GIT REBASE

- git merge create a new commit that has all of the changes of both the branch and combines them together.
- git rebase moves each seperate commit on to the tip of the branch that we are trying to move it onto.
- git rebase not only move the branch but they instead create new commit.
- usecase :-
  1. when there are several developers in the team and you are working on some other branch and other devlopers have made commit to the master branch now if you will merge it will give a conflict so here we can use rebase instead of merge.
- I try to stick with merge

### how to rename a file using git?

- the process is like that(it thinks it deleted the previous file and created a new file with same content)

```
git add newfilename
git rm oldfile
git status
git commit -m "message"
```

- easy way

```
git mv oldfile.extension newfile.extension
```

### how to move a file into a folder

```
git mv filename.extension foldername/newname.extension
```

### how to commit direcctly to the repository

```
git commit -am "commit message" ==> shortcut for both add and commit
```

```
git checkout -- index.html
```

this will take the copy of index.html from repository and replace it with the file in your working directory.

```
git reset HEAD filename
```

this command will remove the file mentioned from the staging area

Note:-

- you can see all the commits by clicking on commits tab of any repo

# explaining pull request process

- go to any person repo fork it
- create your new branch
- commit your changes
- create a pull request
  1. by going to pull request tab
- if the person found it useful he will fork it otherwise close it
- delete the branch you dont need

# if someone made a pull request to your project

- you will be able to see it by clicking on the pull request tab
- a pull request have 3 section {conversation(to chat), commits(to see all the commit), files changed(the changes in the file)}
- close merge/ confirm merge

# Important github buttons

- for a file

1. Raw :- A raw view of file without any text formating
2. Blame :- you can see who added each line on any repo
3. History :- to see the commits made for any particular file

- for entire repo

1. Watch :- {following this project}
2. Star :- {bookmarking this project}
3. fork :- {making a copy of that repo on your profile }
4. Issues :- {a typical to do list of bugs to fix by the person of the team you want} (title , description {code,image, text formating and more})
5. Label :- we add it to the issue {generally of two types :- bugs and enhancement}(you can also make your own label)
6. Assignes :- the person who is assigned to resolve the issue

# Github Wiki

- is is a area that provide more info about our repo
- there is no such rule you can add whatever you want
- you can add a custom sidebar to your all wiki pages

# github Organization & team

- you need it when there is a team to work on the project
- it just like a company or something
- manage teammate roles easily {you can also decide what they can access}
