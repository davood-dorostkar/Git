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
### Remove the history older than a time
install:
```sh
sudo apt install git-filter-repo
```
change the date below and run:
```sh
git filter-repo --force --commit-callback '
    import datetime
    cutoff = datetime.datetime(2024, 12, 1)
    timestamp = int(commit.author_date.decode().split()[0])
    commit_date = datetime.datetime.utcfromtimestamp(timestamp)
    if commit_date < cutoff:
        commit.skip()
'
```
