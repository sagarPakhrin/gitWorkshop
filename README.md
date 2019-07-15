# Git Workship

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

### Lifecycle of files in Git
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
`$echo 'My Project' > README`<br>
`$git status`<br>


#### Viewing your staged and unstaged changes


`$git status`<br>
`$git diff`<br>

if you want to see what you've staged that will go to tour next commit use 
```git diff --staged```<br>

**`git diff` will only show unstaged changed**


## Connecting to github
* got git [GitHub](http://github.com) 
* Log in to you account
* Create new repository
* push existing ripo 

`$ git remote add origin git@github.com:username/ripo`<br>
`$ git push origin master`<br>


## Collaborating with others 

```shell
$ git remote add upstream https://github.com/sagarPakhrin/gitBasics
$git remote -v
$git pull upstream master<br>
# OR**
$git fetch upstream master<br>
```
