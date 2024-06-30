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

