# Git Cheat Sheet

#### List branches

```
git branch                          # list only local branches
git branch -r                       # list only remote branches
git branch -a                       # list remote and local branches
```

#### Delete branch

```
git branch -d your-branch-name                    # delete local branch
git push origin --delete your-branch-name         # delete remote branch
```

#### Create branch and set upstream remote

```
git checkout -b your-branch-name
git push -u origin your-branch-name
```

#### Update branch with new changes on master (includes rebase)

```
git checkout master && git pull && git checkout your-branch-name && git rebase master
```

#### Undo commit(s)

```
git reset --hard HEAD^                # remove previous commit from local branch
git reset --hard HEAD~2               # remove previous two commits from local branch

git push origin +HEAD                 # force push local branch with reverted commit to remote
```

#### Display commit count by user

```
git shortlog -s -n
```

#### List all local commits that haven't been pushed to remote

```
git log --branches --not --remotes
```

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
git config --global alias.st status                   # example changing status to st (git status becomes git st)
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





