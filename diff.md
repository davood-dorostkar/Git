# Git Diff

## Syntax
### unstaged changes
```
git diff
```
### changes in last commit
```
git show
```
### changes of current branch with other branch
```
git diff <other_branch>
```
### changes of specific file
```
git diff <file_relative_path>
```
### changes of branch1 and branch2 and specific file
```
git diff branch1 branch2 file
```
### changed files
```
git diff --name-only
```

## diff output explanation

When you run the command `git diff branch1 branch2 file`. important parts of the output:

1. **File Header:**
   ```diff
   diff --git a/file b/file
   ```
   This line indicates that the comparison is being made between the two versions of `file` in the two branches. `a/file` represents the file in `branch1`, and `b/file` represents the file in `branch2`.

2. **File Path:**
   ```diff
   --- a/file
   +++ b/file
   ```
   These lines indicate the file paths in the respective branches. `--- a/file` corresponds to `branch1` and `+++ b/file` corresponds to `branch2`.

4. **Change Hunk Headers:**
   ```diff
   @@ -1,5 +1,6 @@
   ```
   This line shows the range of lines that are being changed. The `-1,5` indicates that the changes start at line 1 and span 5 lines in `branch1`, and the `+1,6` indicates that the changes start at line 1 and span 6 lines in `branch2`.

5. **Actual Changes:**
   ```diff
   -line in branch1 that is being removed
   +line in branch2 that is being added
   ```
   Lines starting with `-` are present in `branch1` but not in `branch2`. Lines starting with `+` are present in `branch2` but not in `branch1`. Lines without any prefix are unchanged and provide context.

   Example:
   ```diff
   -print("Hello from branch1")
   +print("Hello from branch2")
   ```
