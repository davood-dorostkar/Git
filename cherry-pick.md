cherry-pick is for taking certain commits and applying them on your branch.
## Example
take this history:
```
    a - b - c - d   Main
         \
           e - f - g Feature
```
then if we apply `f` to `main`:
```
git checkout main
git cherry-pick f
```
after the operation:
```
    a - b - c - d - f   Main
         \
           e - f - g Feature
```
## --no-commit
The `--no-commit` option will execute the cherry pick but instead of making a new commit it will move the contents of the target commit into the working directory of the current branch.

## pick a range
pick all commits from some commit to another:
```sh
git cherry-pick abc123..xyz123
```
pick some commits but make them into one (like a squash):
```sh
git cherry-pick abc123..xyz123 --no-commit
git commit -m 'squashed commits'
```
## squash a range in the middle of history:
1. check the history:
```sh
git log --oneline | nl
```
```
     1	0543cf5 will be kept
     2	eb4eff0 will be kept
     3	d2f6187 
     4	b16eba9 
     5	591dd7a 
     6	1d414e2 
     7	3e3f7f4 
     8	31d788f will be kept
     9	c570e09 will be kept

```
```sh
git checkout -b squash-branch 31d788f
git cherry-pick 31d788f..d2f6187 --no-commit
git commit -m 'cherried scripts'
git cherry-pick d2f6187..0543cf5
git checkout main
git reset --hard squash-branch
git push --force
```
