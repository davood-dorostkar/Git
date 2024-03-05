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
### Undo last commit from remote repo
```
git reset --soft HEAD^
git push origin +HEAD^:<branch_name>
```
