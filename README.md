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
You can also check values for specific keys with `git config <key:>`<br>
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
** For Linux **
`$ cd ~/Desktop/`<br>
** For macOs **
`$ cd /Users/user/Desktop`<br>
