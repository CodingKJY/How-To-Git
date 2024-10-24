# How To Git

This is a repo for learning how to git well
---
**Definitions**
- `local` local is the local repo of git, which records local status (`.git`) of workspace
- `remote` remote is said to be github or gitlab, etc.
- `workspace` workspace is the working directory

## Create Local Repo

Suppose we have a workspace and we wish to create a repo to manage it

```c
git init
```

We also could set the initial branch name by setting option

```c
git init -b <name>
git branch -m <change_name>
```

Then setting configuration of this repo

```c
git config --global user.name <username>
git config --global user.email <email>
```

## Create Remote Repo

- `gh` required

Using github cli could easily create/delete repo

```c
gh repo create
> create remote repo from scratch
> create remote repo from template repo
> push an existing local repo to remote
```

## Commit Changes

before commit our changes, let check the status

```c
git status
> Untracked files
```

using git status we could see which file hasn’t staged change. use git add to stage files

```c
git add <files>
```
