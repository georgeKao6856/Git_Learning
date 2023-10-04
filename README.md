# Git & Github
###### tags: `Command` `Git`
---

## What is git?
Git is a specific open-source version control system created by Linus Torvalds in 2005.

Specifically, Git is a distributed version control system, which means that the entire codebase and history is available on every developer’s computer, which allows for easy branching and merging.

## What is github?
GitHub is a for-profit company that offers a cloud-based Git repository hosting service.

## Git Architecture
![](https://i.imgur.com/xhda1dW.png)


## When do we use git & github?
There are two scenarios:
1. Cooperating with teams where all members are the company's employees.
    ![](https://i.imgur.com/Br0lpc9.png)

2. Cooperating with someone or teams that are outside the companies.
    ![](https://i.imgur.com/6Oou0xY.png)

## GitFlow Example
![](https://i.imgur.com/3SCWcHI.jpg)

## Commands
#### git init
Usage: <font color="#f00">git init [repository name]</font>
    
    Initial empty git repository (This command is used to start a new repository.)

#### git clone 
Usage: <font color="#f00">git clone [url]</font>

    This command is used to obtain a repository from an existing URL.
    
#### git add 
Usage: <font color="#f00">git add [file]</font>

    This command adds a file to the staging area.

Usage: <font color="#f00"> git add *</font>
Usage: <font color="#f00"> git add .</font>

    This command adds one or more to the staging area.
    
#### git config 
Project level:
    Usage: <font color="#f00">git config user.name “[name]”</font>
    Usage: <font color="#f00">git config user.email “[email address]”</font>
    Stored location: ./.git/config

System level:
    Usage: <font color="#f00">git config --global user.name “[name]”</font>
    Usage: <font color="#f00">git config --global user.email “[email address]”</font>
    Stored location: ~/.gitconfig

    This command sets the author name and email address respectively to be used with your commits.
    Note: This only affect the "local" repository

#### git status
Usage: <font color="#f00">git status</font>

    This command lists all the files that have to be committed.

#### git rm
Usage: <font color="#f00">git rm [file]</font>

    This command deletes the file from your working directory and stages the deletion.
    
#### git commit
Usage: <font color="#f00">git commit -m “[ Type in the commit message]”</font>

    This command records or snapshots the file permanently in the version history.
    
Usage: <font color="#f00">git commit -a</font>

    This command commits any files you’ve added with the git add command and also commits any files you’ve changed since then.

#### git diff 
Usage: <font color="#f00">git diff</font>
    
    example: git diff HEAD apple.txt (跟本地庫比較)
    example: git diff apple.txt (跟暫存區比較)
    example: git diff HEAD$ apple.txt (跟上一個版本比較)
    This command shows the file differences which are not yet staged. (沒有add)

Usage: <font color="#f00">git diff –staged</font>

    This command shows the differences between the files in the staging area and the latest version present. (已經add)
    
Usage: <font color="#f00">git diff [first branch] [second branch]</font>

    This command shows the differences between the two branches mentioned.

#### git log
Usage: <font color="#f00">git log</font>

    This command is used to list the version history for the current branch.

Usage: <font color="#f00">git log --pretty=oneline</font>
Usage: <font color="#f00">git log --oneline</font>

    This command is used to list the version history for the current branch with beautiful output.

Usage: <font color="#f00">git log –follow [file]</font>

    This command lists version history for a file, including the renaming of files also.

#### git reflog
Usage: <font color="#f00">git reflog</font>
    
    This command manages the information recorded in the reflogs

#### git reset
Usage: <font color="#f00">git reset [file]</font>
    
    This command unstages the file, but it preserves the file contents.

Usage: <font color="#f00">git reset [commit]</font>

    This command undoes all the commits after the specified commit and preserves the changes locally.

Usage: <font color="#f00">git reset --hard [commit]</font>
Usage: <font color="#f00">git reset --hard HEAD^^</font> (back)
Usage: <font color="#f00">git reset --hard HEAD~2</font> (back)

    This command discards all history and goes back to the specified commit.

#### git branch
Usage: <font color="#f00">git branch</font>
    
    example: git branch -v
    This command lists all the local branches in the current repository.

Usage: <font color="#f00">git branch [branch name]</font>

    This command creates a new branch.

Usage: git branch -d [branch name]

    This command deletes the feature branch.

#### git checkout
Usage: <font color="#f00">git checkout [branch name]</font>

    This command is used to switch from one branch to another.

Usage: <font color="#f00">git checkout -b [branch name]</font>

    This command creates a new branch and also switches to it.

#### git merge
Usage: <font color="#f00">git merge [branch name]</font>

    This command merges the specified branch’s history into the current branch.

#### git show
Usage: <font color="#f00">git show [commit]</font>

    This command shows the metadata and content changes of the specified commit.

#### git remote add 
Usage: <font color="#f00">git remote add [variable name] [Remote Server Link]</font>

    example: git remote add origin https://github.com/georgeKao6856/iSkin.git
    查看: git remote -v
    This command is used to connect your local repository to the remote server.
    
#### git push 
Usage: <font color="#f00">git push [variable name] master</font>

    example: git push origin master
    This command sends the committed changes of master branch to your remote repository.
    
Usage: <font color="#f00">git push [variable name] [branch]</font>
    
    example: git push origin hot_fix
    This command sends the branch commits to your remote repository.

Usage: <font color="#f00">git push –all [variable name]</font>

    example: git push -all origin
    This command pushes all branches to your remote repository.

Usage: <font color="#f00">git push [variable name] :[branch name]</font>

    example: git push origin : hot_fix
    This command deletes a branch on your remote repository.
    
#### git pull
Usage: <font color="#f00">git pull [Repository Link]</font>

    git pull = git fetch + git merge
    This command fetches and merges changes on the remote server to your working directory.

 