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
### remove any branch in local that is no longer on the remote
```
git fetch --prune
```
### receive the updates of other branches when cloned it as shallow previously
```
nano .git/config
```
make sure you have all branches(*) in fetch list:
```
[remote "origin"]
	url = <URL>.git
	fetch = +refs/heads/*:refs/remotes/origin/*
```
### rename branch
```
git checkout <new name>
git branch -d --force <last name>
git push origin --delete <last name>
git push -u origin <new name>
```
