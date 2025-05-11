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
