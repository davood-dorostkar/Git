to remove existing file from version control

```
git rm --cached file.txt [or *.txt]
```

Remove all untracked files from indexing with respect to .gitignore file:

```
git rm -r --cached .

git add .
```

show list of tracked files

```
git ls-tree -r master --name-only
```

remove untracked files

```
git clean -f
```
