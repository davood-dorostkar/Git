### create new branch

```
git checkout -b 00001_START
```

### list branches

```
git branch
```

### switch to branch
```
git checkout branchname
```

### merge a branch to another

```
git merge sourceBranchName
```

> Note: the destination is the currently active branch

### remove a branch locally

```
git branch -d branchName
```

### remove a branch remotely

```
git push origin --delete branchName
```
### rename branch
```
git checkout <new name>
git branch -d --force <last name>
git push origin --delete <last name>
git push -u origin <new name>
```
