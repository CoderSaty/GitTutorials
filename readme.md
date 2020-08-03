# Installation...

## Software Required...

1. Ubuntu Shell
2. Git (according to your os)

## TO check git is installed or not

```
git --version
```

# The terminal Commands

## Introduction to terminal(A way to interact with os)

- To go to the root directory
  ```
  cd /
  ```
- To go to the windows system from ubuntu shell
  ```
  cd mnt
  ```
- To list all the files inside ant directory
  ```
  ls
  ```
- TO move any particular folder
  ```
  cd foldername
  ```
- TO clear the screen
  ```
  clear
  ```
- To go one direcotry backward
  ```
  cd ..
  ```
- To go the home directory
  ```
  cd ~
  ```
- To create a folder with given folder name

```
mkdir foldername
```

- To move to any particualr location
  ```
  cd path
  ```

### Note:-

1. cd ==> change directory
2. pwd ==> To display the current working directory of the terminal
3. ls -la ==> in order to see all the hidden git files

## working with files and directory

- To remove the folder with foldername and everything inside it
  ```
  rm -rf foldername
  ```
- To remove the file with filename with given extension
  ```
  rm filename.extension
  ```
- To create the file with given extension
  ```
  touch filename.extension
  ```

### Note :-

1. -rf ==> this is to specify that we are removing a folder instead of file (this type of statement starting from - is known as flag)
2. touch ==> it does not work on pwershell
3. echo \$null >> filename.extension ==> this is used to create the file with given filename on powershell

# Git Basics

- [Git command cheatsheet](https://www.github.com/joshnh/Git-Commands)

## Working with a new repository

- To intialise the git repository
  ```
  git init
  ```
- To add all the files to the staging area
  ```
  git add .
  ```
- TO add any particular file to the staging area
  ```
  git add filename
  ```
- To get the status of the staging area
  ```
  git status
  ```
- To commit the changes
  ```
  git commit -m "message"
  ```
- To confugure the useremail for all your repo
  ```
  git config --global user.email "youremail"
  ```
- To confugure the username for all your repo
  ```
  git config --global user.name "your name"
  ```
- To see all the seetings
  ```
  git config --list
  ```
- To open the list of all git commads
  ```
  git --help
  ```
- To open open the manual for the git commit
  ```
  git commit --help
  ```
- To commit all the tracked files with the commit message {shortcut for add and commit}
  ```
  git commit -a -m "your message"
  ```
- To give the list of all the commits you have made

```
git log
```

- To only show the commits made by author codersaty. {you need not to type the full name alaways}
  ```
  git log -- author="codersaty"
  ```
- To show all the commits in a single line

```
git log --oneline
```

- To remove the file from the repository
  ```
  git rm nameoffile.extension
  ```
- To remove the file from repository forcefully

```
git rm -f nameoffile.extension
```

- To remove the file from the staging area

```
git rm --cached nameoffile.extension
```

- To show the changes you have made {this only show the difference between working copy and repository}
  ```
  git diff
  ```
- To show the differences when the file is in staging area
  ```
  git diff --staged
  ```

## Tracking our git commit history

- To move to that state of time when the particular commit was made {this will not delete all the commit we are just going back in time}
  ```
  git checkout commit-id
  ```
- To take you back to the latest commit
  ```
  git checkout master
  ```

## git revert and git reset

- To reverts the changes upto that commit id
  ```
  git revert commit id
  ```
- resets all the commit upto that commit id
  ```
  git reset --hard  commit id
  ```

### Note :-

1. checkout helps us to go back in time but how to stay their permenately?
2. git revert is a little bit safer than git reset because it goes back in time to only one commit and reverts the changes and make a new commit with new message
3. you can also revert the revert commit
4. there are three different stages of git reset soft mix and hard . soft is just like git checkout and hard is like hard reset.
5. git reset resets all the commit upto that commit
6. HEAD always points to the currently selected commit

## create a .gitignore file

- To remove the cached memory from the staging area
  ````
  git rm - r --cached . ``` ```
  ````

### Note:-

1. It is a file that has a list of all the files and directory that we do not want to track.
2. The file does not have any name
3. Create the file list all the files and directory you need to ignore commit the change

## git branches

- To create a new branch with the given name
  ```
  git branch "name of the branch"
  ```
- To create the new branch with the given name and will switch to it.

```
git checkout -b "name of the branch"
```

- To switch to master branch

```
git checkout master
```

- To list all the branch with a star on the current branch
  ```
  git branch -a
  ```
- To delete the specified branch
  ```
  git branch -d "name of the branch"
  ```
- git merge "name of the branch"
  ```
   To  merge the specified branch with the current branch you are working on
  ```

### Notes:-

1. git branches are a way to create a separate development path without overiding or creating copies of your project
2. branches can be added deleted and merged just like regular commits
3. braches can be used to seperate different end goals of your project
4. create seperate bracnhes for each stage of developement.
5. you have to make the intial commit before creating any branch otherwise your development branch will be considered as master branch
6. you have to make the commit in the similar manner you have to just switch to the required branch
7. be careful and cautiois before commiting something
8. Merging Branches :- bringing all the branches together
9. there are two merge commands one merges to current directory and the in the other command we can specify the source and destination
10. a branch can be defined as a chain of commits that does not interfere with other branch

## Github

### Note :-

1. what is github? => it is an application that allows you to store remote repo on their servers.
2. benefits :-

- provides a user friendly platform to interract with and manage your repo
- it is public and open source(social coding)
- used as a portfolio
- open oppurtunities you might not have with a local repo
- easy acess from any device
- industry standard

3. creating a github account
4. github documentation
5. creating first repo on github
6. there are various licesence
7. Issues (can be listed by the contributors)
8. pull request (anyone wants to pull your repo on their local site)
9. wiki (you can place the large documentation of your software here)
10. insights (records of the repository)
11. settings (delete, acess,change Name,collaborators)
12. deploy key (to deploy repo on some site)
13. watch , Star , fork , clone and downloadig. (viewing other people repository)

## working with git remotely

### connecting to remote repo through our terminal {Procedure}

- step 1st:- intialize the repo {optional}
  ```
  git init
  ```
- Step 2nd:- To connect with the remote repo the local repo
  ```
  git remote add origin "url of the repo"
  ```
- Step 3rd :- to check whether the remote repo is connected or not (it will show us the remote origin we use to push and pull information){optional}
  ```
   git remote -v
  ```

### Note :-

1. A remote origin is a link to access your remote repository.

### Push & Pull System

- To push the change in your local machine to the remote repo
  ```
  git push
  ```
- To pull any remote repo in your local machine
  ```
  git pull
  ```

### pushing and pulling to and from a github repo

```
git pull -u origin master
```

- we have to write the command given above for the first time so that the pull can remember the branch{-u is responsible for this}

```
git pull
```

- once pulled we can use the command given above simply and we dont have to specify the branch

```
git push -u origin master
```

- we have to write the command given above for the first time so that the push can remember the branch

```
git push
```

- once pushed we can use the command given above simply and we dont have to specify the branch

### Note:-

1. create a readme file
2. create a license file (license.md){MIT license (allow people to take your project and edit it)}
3. create a .gitignore {you can also use a template for a particular tech}
4. sometime when conflict arise you can google it and resolve it manually

### working with remote branches {Process}

- Step 1st:- get everything in local repo
  ```
  git pull
  ```
- Step:- 2nd:- creating a branch named rectify and switching to it

  ```
  git checkout -b rectify
  ```

- Step 4th :- fix the error and commit the changes
  ```
  git add .
  git commit -m "message"
  ```
- Step 5th :- switch to master branch
  ```
  git checkout master
  ```
- Step 6th:- merge the rectify branch to master branch
  ```
  git merge rectify
  ```
- Step 7th:- push to github repo

  ```
  git push
  ```

  > This will push only the master branch not to the rectify branch. To push to rectify branch

  ```
  git push origin rectify
  ```

- Step 8th :- remove the branch
  ```
    git push origin --delete rectify
  ```
  > deletes the remote rectify branch and will also push the changes

### Note :-

1. typical process :-

- create a new branch
- fix that error
- merge with master branch
- delete that branch

2. we can push only one branch at a time to a remote repository.
3. we can interact with our remote repo through push pull cycle.

## Git GUI (Sourcetree or Github Desktop)

- If we do not love working with terminal we can also use git gui such as sourcetree or github desktop which is more user friendly. BTW I prefer terminal.

## GIT REBASE

### Note:-

1. git merge create a new commit that has all of the changes of both the branch and combines them together.
2. git rebase moves each seperate commit on to the tip of the branch that we are trying to move it onto.
3. git rebase not only move the branch but they instead create new commit.
4. usecase :-

- when there are several developers in the team and you are working on some other branch and other devlopers have made commit to the master branch now if you will merge it will give a conflict so here we can use rebase instead of merge.

5. I try to stick with merge

## Some Questions....

### how to rename a file using git?

> the process is like that(it thinks it deleted the previous file and created a new file with same content)

- Entire Procedure

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

### how to move a file into a folder?

```
git mv filename.extension foldername/newname.extension
```

### How to take the copy of index.html from repository and replace it with the file in your working directory?

```
git checkout -- index.html
```

### How to remove the file from the staging area?

```
git reset HEAD filename
```

## Some note points on github

1. you can see all the commits by clicking on commits tab of any repo

2. the entire pull request process

- go to any person repo fork it
- create your new branch
- commit your changes
- create a pull request
  1. by going to pull request tab
- if the person found it useful he will fork it otherwise close it
- delete the branch you dont need

3. If someone made a pull request to your project

- you will be able to see it by clicking on the pull request tab
- a pull request have 3 section {conversation(to chat), commits(to see all the commit), files changed(the changes in the file)}
- close merge/ confirm merge

4. Important github buttons

- For a file
  1. Raw :- A raw view of file without any text formating
  2. Blame :- you can see who added each line on any repo
  3. History :- to see the commits made for any particular file

* for entire repo
  1. Watch :- {following this project}
  2. Star :- {bookmarking this project}
  3. fork :- {making a copy of that repo on your profile }
  4. Issues :- {a typical to do list of bugs to fix by the person of the team you want} (title , description {code,image, text formating and more})
  5. Label :- we add it to the issue {generally of two types :- bugs and enhancement}(you can also make your own label)
  6. Assignes :- the person who is assigned to resolve the issue

5. Github Wiki

- is is a area that provide more info about our repo
- there is no such rule you can add whatever you want
- you can add a custom sidebar to your all wiki pages

6. github Organization & team

- you need it when there is a team to work on the project
- it just like a company or something
- manage teammate roles easily {you can also decide what they can access}
