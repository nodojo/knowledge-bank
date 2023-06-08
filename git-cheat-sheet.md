# Git Cheat Sheet

## List branches

#### List only local branches

```bash
git branch
```

#### List only remote branches

```bash
git branch -r
```

#### List remote and local branches

```bash
git branch -a
```
## Delete branch

#### Delete local branch

```bash
git branch -d your-branch-name
```

#### Delete remote branch

```bash
git push origin --delete your-branch-name
```

## Create branch and set upstream remote

```
git checkout -b your-branch-name
git push -u origin your-branch-name
```

## Update branch with changes from master then rebase

```
git checkout master && git pull && git checkout your-branch-name && git rebase master
```

## Undo / Edit commit(s)

#### Undo the last commit

```bash
git reset --hard HEAD^
```

#### Undo the last two commits

```bash
git reset --hard HEAD~2
```

#### Force push local branch with reverted commit(s) to remote

```
git push origin +HEAD
```

#### Undo then redo a commit

```bash
git reset HEAD~

# make the desired edits

git add .
git commit -c ORIG_HEAD
```

#### Edit message of unpushed commit

```bash
git commit --amend -m 'new message goes here'
```

## Display logs

#### Display commits on single line with graph of commits on left

```
git log --oneline --graph
```

#### List all local unpushed commits

```
git log --branches --not --remotes
```

#### Display commit count by user

```
git shortlog -s -n
```

## Manage .gitconfig

#### List configs from global .gitconfig

```
git config --global --list
```

#### List configs and their origin(s)

```
git config --list --show-origin
```

#### Open .gitconfig in Notepad (Windows)

```
start ~/.gitconfig
```

#### Set config so you only push to branch on which you are working

```
git config --global push.default current
```

#### Add alias to .gitconfig

```
git config --global alias.st status                   # this example changes status to st (git status becomes git st)
```

#### Remove alias from .gitconfig

```
git config --global --unset alias.st
```

## Manage remotes

#### Change to a new remote origin (repository) using ssh

```bash
git remote set-url origin git@github.com:repo-name-goes-here
```

#### Verify update by displaying fetch and push origins

```bash
git remote -v
```

## Manage tags

#### List local tags

```bash
git tag
```

#### Edit tag and create new tag containing your changes

1. Create a new branch from tag

```bash
git checkout -b your-new-branch-name existing-tag-name
```

2. Make and commit your edits

3. Create a new tag containing your changes

```bash
git tag -a -m 'new tag message goes here' your-new-tag-name
```

4. Push the newly created tag to the remote repository

```bash
git push origin your-new-tag-name
```

#### Delete local tag

```bash
git tag -d your-tag-name
```

#### Delete remote tag

```bash
git push --delete origin your-tag-name
```

## Resources

- [Bash CheatSheet (LeCoupa)](https://github.com/LeCoupa/awesome-cheatsheets/blob/master/languages/bash.sh)


