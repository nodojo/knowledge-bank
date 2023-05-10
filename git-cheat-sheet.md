# Git Cheat Sheet

### List branches

```
git branch                          # list only local branches
git branch -r                       # list only remote branches
git branch -a                       # list remote and local branches
```

### Delete branch

```
git branch -d your-branch-name                    # delete local branch
git push origin --delete your-branch-name         # delete remote branch
```

### Create branch and set upstream remote

git checkout -b your-branch-name
git push -u origin your-branch-name
