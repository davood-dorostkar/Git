## Config
### Get
show current global user name
```bash
git config --global user.name
```
show current global user email
```bash
git config --global user.email
```
show repo-specific user name: just ommit the `--global`

### Set
set global user email
```bash
git config --global user.email "davood.dorostkar.ut@gmail.com"
```
set global user name
```bash
git config --global user.name "davood"
```
set repo-specific user name: just ommit the `--global`

### remove
other cases are the same
```bash
git config --global --unset user.name
```

CLEAN STEPS FROM SCRATCH  

  

When you start from Github: 

 

1. make a repo in github 

2. clone it somewhere (git clone url) 

3. go inside the new folder 

4. start committing and pushing (requests login) 

 

OR 

When you start from local Git: 

 

Make a repo in github 

Copy repo "address" and close 

Go to your local code 

git init  

git add .  

git config --global user.email "dado2hacker@gmail.com" (for first time) 

git commit -am "first commit" 

git remote add origin "address" 

git push –u origin master 

Enter davood-dorostkar and Chalenger.69 

 

Help 

 

1-init git repository in current directory [in case you dont want to clone] 

git init . 

 

2. add all files into stage 

git add . 

 

3-to commit with message use these below: 

git commit -am "ver1" 

 

4-use (git status) and (git log) to view repository status 

 

5-to create new branch 

git checkout -b 00001_START 

 

6-list branch 

git branch 

 

7-to go to specific branch 

git checkout branchname 

 

8-to upload 

git push -u origin branchname 

 

9-to download repository [don't init before this] 

git clone url 

 

10-to get all changes in repository (the downloaded files are separate from local ones) 

git fetch --all 

 

11-to merge a branch to another 

git merge sourceBranchName Note: the destination is the currently active branch 

 

12-to remove existing file from version control 

git rm --cached file.txt [or *.txt] 

 

Remove all untracked files from indexing with respect to .gitignore file: 

git rm -r --cached . 

git add . 

 

13-show list of tracked files 

git ls-tree -r master --name-only 

 

14-remove a branch locally 

git branch –d branchName 

 

15-remove a branch remotely 

git push origin –delete branchName 

 

16-remove untracked files 

git clean -f 

 

17-get and replace files from remote 

git pull -all 

 

18-save username and token 

 

>> git pull then enter your credential 

git config --global credential.helper store 
