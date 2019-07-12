# Git Workship

## installing git
##### Installing on Linux
`sudo dnf install git-all`<br>
<br> Or </br>
`sudo apt install git-all`<br>
<br> Or </br>
`sudo apt install git`


##### Installing on Windows
install git bash


## First-Time Git Setup
`git config --list --show-origin`<br>
`git config --global user.name your_name`<br>
`git config --global user.email youremail@example.com`<br>


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

###### for example
`git help config`<br>


# Git Basics

You can obtain a Git repository in on of two ways
<ol>
	<li>You can turn local directory into a git repository</li>
	<li>You can clone an existing Git repository from elsewhere</li>
</ol>

#### Initializing a Repository in an Existing Directory
`$ cd ~/Desktop/`<br>
`$ mkdir gitBasics && cd gitBasics`<br>
`$ git init`<br>

**Adding a file to staging**<br>
`$ git add *.c`<br>
`$ git add LISENCE`<br>
`$ git commit -m "initial project version"`<br>


**To add all the files at once**
`$git add .`


#### Checking status of your Files
`$git status`<br>
`On branch master`
`Your branch is up-to-date with 'origin/master'.`
`nothing to commit, working directory is clean`
it means that none of the tracked files are modified
