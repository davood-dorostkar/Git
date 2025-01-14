### check differences between commits
```sh
git diff <comm1> <comm2>
```
### remove everything after a commit
```sh
git reset --hard <commit Hash>
```
### Undo last commit but keep changes into staging
```sh
git reset --soft HEAD^
```
or for more commits:
```sh
git reset --soft HEAD~3
```
### Undo last 2 commits from local and then remote repo
```sh
git reset --hard HEAD~2
git push origin HEAD --force
```
### See the changes done with last commit
```sh
git show
```
or 
```sh
git diff HEAD^ HEAD
```
### Unstage files from staging
```sh
git restore --staged FILE
```
