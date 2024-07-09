## Examine your repo

```
git status
```
```
git log
```
```
git reflog
```
```
git branch -vv
```
last 4 commits:
```
git log -4
```
breif logs:
```
git log --oneline
```
## Check remote status
only show remote URL:
```
git ls-remote --get-url origin
```
Show detailed info about remote and local relation:
```
git remote show origin
```
Show `push` and `fetch` URLs seperately:
```
git remote -v
```
change remote url:
```
git remote set-url origin <new url>
```
