# How to Git

Learn git here!

Definitions

- `local` local is the local repo of git, which records local status (`.git`) of workspace
- `remote` remote is said to be github or gitlab, etc.
- `workspace` workspace is the working directory

## Create Local Repo

Suppose we have a workspace and we wish to create a repo to manage it

```bash
git init
```

We also could set the initial branch name by setting option

```bash
git init -b <name>
git branch -m <change_name>
```

Then setting configuration of this repo

```bash
git config --global user.name <username>
git config --global user.email <email>
```

## Create Remote Repo

- `gh` required

Using github cli could easily create/delete repo

```bash
gh repo create
> create remote repo from scratch
> create remote repo from template repo
> push an existing local repo to remote 
```

Here we push the local repo which created from the previous step

```bash
> set remote repo name
> set description fo this repo
> set visibility (public/private)
> add remote to local repo
> set remote alais
```

## Commit Changes

before commit our changes, let check the status

```bash
git status
> Untracked files
```

using git status we could see which file hasn’t staged change. use git add to stage files

```bash
git add <files>
git rm --cache <staged_files> # used to unstage files
```

after staging files, we now could commit!

- `-m` add commit message

```bash
git commit -m '<commit_msg>'
git commit -m '<commit_msg_title>' -m '<commit_msg_body>'

git log # show logs to check previous commits
```

## Push

Since our local repo has no any information of remote repo, thus we have to set the upstream to let git know where to push

```bash
git branch --set-upstream-to <remote_repo> <remote_branch>
git branch --unset-upstream
```
or just push with upstream

```bash
git push -u <remote_repo> <remote_branch>
```
