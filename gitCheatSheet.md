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


## Create a repository
Start a new repository or obtain one from an existing URL
> Creates a new local repository with the specified name. 

```
git init [project-name]
```
> Downloads a project and its entire version history

```
git clone [url]
```

## Initializing a local git repository 

> Create a empty git repository on your machine / workspace :

```
git init 
```


## Check out a repository

> Create a working copy of a local repository: 


```
git init [project-name]
```

> Downloads a project and its entire version history

```
git clone [url]
```

## Make Changes in repository
> Snapshots the file in preparation for versioning
```
git add [file]
```
> Lists all new or modified files to be committed
```
git status
```
> Unstages the file, but preserve its contents
```
git reset [file]
```
> Shows file differences not yet staged
```
git diff
```
> Shows file differences between staging and the last file version
```
git diff --staged
```
> Records file snapshots permanently in version history
```
git commit -m "[descriptive message]"
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
## Commit history 

> After you have created many commits or changes to an existing repository , to see what has happened or the commit history  do this : 

```
git log

```


> To filter out a commit after a specific time or a date you can do this  : 

```
git log --after="2019-10-8"
git log --after="yesterday"
git log --after="2017-7-1" --before="2017-7-4"
```

## Interacting with others

> Import a GNU Arch repository into Git

```
git-archimport[1]
```

> Export a single commit to a CVS checkout

```
git-cvsexportcommit[1]
```

> Salvage your data out of another SCM people love to hate

```
git-cvsimport[1]
```

> A CVS server emulator for Git

```
git-cvsserver[1]
```

> Send a collection of patches from stdin to an IMAP folder

```
git-imap-send[1]
```

> Import from and submit to Perforce repositories

```
git-p4[1]
```

> Applies a quilt patchset onto the current branch

```
git-quiltimport[1]
```

> Generates a summary of pending changes

```
git-request-pull[1]
```

> Send a collection of patches as emails

```
git-send-email[1]
```

> Bidirectional operation between a Subversion repository and Git

```
git-svn[1]
```


## Save Fragments
> Temporarily stores all modified tracked files
```
git stash
```
> Lists all stashed changesets
```
git stash list
```
> Restores the most recently stashed files
```
git stash pop
```
> Discards the most recently stashed changeset
```
git stash drop
```

## Review History

> Lists version history for the current branch
```
git log
```
> Lists version history for a file, including renames
```
git log --follow [file]
```
> Shows content differences between two branches
```
git diff [first-branch]...[second-branch]
```
> Outputs metadata and content changes of the specified commit
```
git show [commit]
```

## Links to go forward

https://learngitbranching.js.org/


