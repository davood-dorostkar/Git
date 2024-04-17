### check differences between commits
```
git diff <comm1> <comm2>
```
### remove everything after a commit
```
git reset --hard <commit Hash>
```
### Undo last commit but keep changes into staging
```
git reset --soft HEAD^
```
### Undo last 2 commits from local and then remote repo
```
git reset --hard HEAD~2
git push origin HEAD --force
```
### See the changes done with last commit
```
git show
```
or 
```
git diff HEAD^ HEAD
```
