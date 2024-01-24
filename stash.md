In Git, the `git stash` command is used to temporarily save changes that you have not committed to a separate area, allowing you to switch branches, apply changes, and then return to your original branch. This can be useful when you are in the middle of working on a feature or bug fix but need to switch to another branch to address an urgent issue or work on a different task.

Here's how to use `git stash`:

### Stashing Changes

To stash your changes, you can use:

```bash
git stash
```
to stash specific file
```bash
git stash -- filename.txt
```

This command will save your changes, including both staged and unstaged modifications, in a new stash. The working directory will then be reverted to the state of the last commit.

### Stashing Changes with a Message

You can add a message to the stash to provide more context about the changes:

```bash
git stash save "Your stash message here"
```

### Viewing Stash List

To view a list of your stashes, you can use:

```bash
git stash list
```

This will display a list of stashes, each with a unique identifier (stash@{n}) and the message you provided (if any).

### Applying Stashed Changes

To apply the changes from the most recent stash, you can use:

```bash
git stash apply
```

This will apply the changes to your working directory, but the changes will still be in the stash. If you want to remove the stash after applying, you can use:

```bash
git stash pop
```

### Applying Changes from a Specific Stash

If you have multiple stashes and want to apply changes from a specific stash, you can use:

```bash
git stash apply stash@{n}
```

Replace `{n}` with the index of the stash you want to apply.

### Creating a Branch from a Stash

You can create a new branch and apply changes from a stash in one step:

```bash
git stash branch new_branch_name
```

This will create a new branch named `new_branch_name` and apply the changes from the most recent stash to the new branch.

### Dropping a Stash

To remove a stash without applying the changes, you can use:

```bash
git stash drop stash@{n}
```

This removes the specified stash from the list.

### Clearing All Stashes

To remove all stashes, you can use:

```bash
git stash clear
```

Remember that stashing is a powerful tool, but it's essential to use it judiciously. Always commit your changes when possible to have a clean history, and use `git stash` when you need a quick way to switch contexts without committing incomplete work.
