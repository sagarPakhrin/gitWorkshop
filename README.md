# Git Workshop

## Introduction
**What is git?**


## installing git
##### Installing on Linux
```shell
$ sudo dnf install git-all
# or
$ sudo apt install git-all
# or
$ sudo apt install git
```

## First-Time Git Setup
```$ git config --list --show-origin
$ git config --global user.name your_name
$ git config --global user.email youremail@example.com
```


### Checking your settings
`git config --list`<br>
You can also check values for specific keys with<br> `git config <key:>`<br>
`git config user.name`<br>
`John Doe`<br>


## Getting help
if you ever need help using git, there are three ways to get help
`$git help <verb>`<br>
`$git <verb> --help`<br>
`man git-<verb>`


for example<br>
`git help config`<br>


# Git Basics
You can obtain a Git repository in on of two ways
1. You can turn local directory into a git repository
2. You can clone an existing Git repository from elsewhere

## Initializing a Repository in an Existing Directory
```shell$ 
cd ~/Desktop/
$ mkdir gitBasics && cd gitBasics
$ git init
```

### Life cycle of files in Git
<img src="./images/workflow.PNG">

**Adding a file to staging**<br>
```shell
$ git add hello_world.py<br>
$ git commit -m "Hello world"

# Combining these two steps
$ git commit -am "combined steps"
#or 
$ git commit -a
```

**To add all the files at once**
`$git add .`


#### Checking status of your Files
```shell
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory is clean
```


**Tracking new Files**
```shell
$echo 'My Project' > README<br>
$git status<br>
```

#### Viewing your staged and unstaged changes


```shell
$git status<br>
$git diff<br>
```

if you want to see what you've staged that will go to tour next commit use <br>
```git diff --staged```<br>

**`git diff` will only show unstaged changed**


## Connecting to github
* Go to [GitHub](http://github.com) 
* Log in to you account
* Create new repository
* push existing ripo 

`$ git remote add origin git@github.com:username/ripo`<br>
`$ git push origin master`<br>


## Collaborating with others 
1. Fork the project
2. Pull the forked ripo from you ripo
3. Make desired changes
4. Push the changes to your ripo
5. Create pull request
6. Add upstream of the original ripo
7. Pull upstream

```shell
$ git remote add upstream https://github.com/sagarPakhrin/gitBasics
$git remote -v
$git pull upstream master<br>
# OR
$git fetch upstream master<br>
```


## Merging Conflicts
Git keeps track of all the changes you make to your file. But what happens if you make changes to a
file in say line 101 and some other collaborators also makes the changes to the same files and
pushes to the same ripo? In that case git doesn't know what to do with the changes and so it creates
`merge conflict`

example of merge conflict
```shell
<<<<<<< HEAD 
int a = 2; #everyting between head and the = is our local changes
========
int b = 0; # everythin between = and >>>> is the changes on the remote ripo
>>>>>>>>

```
Resolving `merge conflicts`
---
* Delete everything you don't want and commit the changes and push


#### Git resetting
git reset #resetting to a stable version of the code
- `git reset --hard <commit>` resets code back to a previous commit
- `git reset --hard origin/master` reverts code back to remote repository version


## Branching
It allows you to have a multiple version of files in the same ripo. It allows you to keep you a
stable version of the code unmodified and create a branch off to a new branch and add new features.
and when you feel ready you can merge with the master branch.

* Branch if a version of the repository
* Each branch has its own commit history of the current version

```shell
$ git branch 
#this will show all the branches
$ git branch new_branch
# this will create a new branch called new_branch 

# to change to the new branch hit
$ git checkout new_branch

# if you'd like to combine two steps you can use the command
$ git checkout -b new_branch
```

After creating new branch and making required changes, you checkout to the master branch and merge
new_branch
