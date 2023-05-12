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

## Update branch with new changes on master (includes rebase)

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
git config --global alias.st status                   # example changes status to st (git status becomes git st)
```

#### Remove alias from .gitconfig

```
git config --global --unset alias.st
```

#### Change to a new remote origin

```
git remote -v                                                                 # display current fetch / pull origins
git remote set-url origin git@github.com:acst/DecisionInsite.Maps.git         # set remote to new origin
git remote -v                                                                 # verify remote origins have been properly set
```





