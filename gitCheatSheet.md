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
