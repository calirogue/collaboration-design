# git event

## What is git?
1. Version control
2. helps with work flow between different developers on a project
3. keeps track of code history

### Installing git
1. Linux: sudo apt install git-all
2. Mac: as long as you have xcode command line tools or you can https://git-scm.com/download/mac
3. Windows: https://git-scm.com/download/win
    - If a prompt comes up, (adjusting your PATH command)
    - Choose the last one - use git and optional unix tools from windows command propt
    - rest of the options just leave at default
    - then click "launch git bash"
    - in the terminal write: 
    git --version
    - it should output the version of git

GUI for git:
https://www.gitkraken.com/download


## Setting up:
$ git config --global user.name 'your name'
$ git config --global user.email 'your email'

## Basics
$ git init // intialize local git repository
$ git add // add files to index
$ git status // check status of working tree
$ git commit // commit changes in index

## Remote repo 
$ git push // push to remote repo
$ git pull // pull latest from remote repo
$ git clone // clone repo into a new directory

## Remove an item after it's been added to index
$ git rm --cached filename

## Add
git add *.js or *. // this will add any files with the ending of .js for example


---------------------------
Advance:

## Go to the previous branch
$ git checkout -

## History
$ git log

### Here all commit that contain 'about'
$ git log --all --grep='about'

### Retrieve all commit by author
$ git log --author="Maxence"



## Reset 
1. $ git reset --soft to-log-file-you-want-to-go-back-to
- won't erase everything you just did 

2. $ git reset --hard to-log-file-you-want-to-go-back-to
- will erase everything you just did to that file you want to reset to

3. Get everything you did:
$ git reflog


## mixed-up with in local repo
$ git fetch origin
$ git checkout master
$ git reset --hard origin/master
- You're now up-to-date with master

## diff between a branch and master:
$ git diff master..my-branch


## commits:
### Edit last commit
$ git commit --amend -m "A better message"

### Add something to the last commit without writing message again
$ git add . && git commit --amend --no-edit

### empty commit - can be useful to re-trigger CI build...
$ git commit --allow-empty -m "chore: re-trigger build"


## rebase:
Rebase command integrates changes from one branch into another.
- rebase last 3 commits:
$ git rebase -i HEAD~3

- Will run "npm test" command on the last 3 commit 
$ git rebase HEAD~3 --exec "npm run test"


## Upstream
- upstream: original repo that you have forked
- origin is your fork

- Now you can collect the latest changes of the upstream repository with fetch. 
$ git remote add upstream git@github.com:bellagrunt/collaboration-design.git
Repeat this every time you want to get updates:
$ git fetch upstream

## Fork
A fork is a copy of a repo that allows you to freely experiment with changes without affecting the original project.