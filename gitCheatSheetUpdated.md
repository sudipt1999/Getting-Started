# Git Cheat Sheet

Refer this cheat sheet when ever you are stuck somewhere. 

## Setting up softwares

To work on Github hosted projects, one has to use Git - a Version Control System. So the first task is to install git on your machine. For Windows users, download git from here - https://git-scm.com/downloads. For Linux users, you can use your distro's package manager to install git.

Note: Although Linux isn't mandatory, it is preferred while working with Open Source Software.

Note: You can learn about Version Control Systems (VCS) here.

## Tell Git Who You Are ?

> Configure the author name and email address to be used with your commits.
Note that Git strips some characters (for example trailing periods) from user.name.

```
git config --global user.name "your Name"
git config --global user.email your@example.com
```

## Check out a repository

> Create a working copy of a local repository: 

```
git clone /path/to/repository
```

## Add files

> Add one or more files to repo: 

```
git add <file>
```
> Or you can add all files at a single time: 

```
git add .
```

## Removing a file from staging area

> Remove one or more files from staging area :
```
git rm --cached <filename>
```

## Status

> List the files you've changed and those you still need to add or commit: 

```
git status
```

## Reseting added files

> Often you would add files mistakenly to repo now you feel to discard the added file(s):

```
git reset <file>
```

## Commit

> Commit changes to head (but not yet to the remote repository):

```
git commit -m "Commit message"
```

> Commit any files you've added with git add, and also commit any files you've changed since then:

```
git commit -a
```
Note : Writing a good commit message is a art, kindly refer to [link](https://github.com/erlang/otp/wiki/writing-good-commit-messages) to know more about writing good commit message.


## Push

> Send changes to the master branch of your remote repository:

```
git push origin master
```

> You can also push updates to specific branch on remote repository:

```
git push origin <branch>
```

## Connect to a remote repository

> If you haven't connected your local repository to a remote server, add the server to be able to push to it:

```
git remote add origin <url>
```

Note: This is used when you have forked a repo, it adds the repo to the list you can pull and push(if you have access) to the remote repo.

> List all currently configured remote repositories:

```
git remote -v
```

## Branches

> List all the branches in your repo, and also tell you what branch you're currently in:

```
git branch
```

> Create a new branch and switch to it:

```
git checkout -b <branchname>
```

> Switch from one branch to another:

```
git checkout <branchname>
```

> Delete the feature branch:

```
git branch -d <branchname>
```
Note: To delete forcefully use `-D` instead of `-d`

> Push the branch to your remote repository, so others can use it:

```
git push origin <branchname>
```

> Push all branches to your remote repository:

```
git push --all origin
```

> Delete a branch on your remote repository:

```
git push origin :<branchname>
```

## Update from the remote repository

> Fetch and merge changes on the remote server to your working directory:

```
git pull
```

> To merge a different branch into your active branch:

```
git merge <branchname>
```


> View all the merge conflicts:

```
git diff
```


> View the conflicts against the base file:

```
git diff --base <filename>
```

> Preview changes, before merging:
```
git diff <sourcebranch> <targetbranch>
```

> After you have manually resolved any conflicts, you mark the changed file:

```
git add <filename>
```

## Undo local changes

> If you mess up, you can replace the changes in your working tree with the last content in head:
Changes already added to the index, as well as new files, will be kept.   

```
git checkout -- <filename>
git checkout -- . 
```

> Instead, to drop all your local changes and commits, fetch the latest history from the server and point your local master branch at it, do this:

```
git fetch origin

git reset --hard origin/master
```

## Search

> Search the working directory for foo():

```
git grep "foo()"
```






