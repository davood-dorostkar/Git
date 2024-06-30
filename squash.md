Merging the last four commits into one is a common task in version control using Git. This process is known as "squashing" commits:

1. **Start an Interactive Rebase**:
   Begin an interactive rebase for the last four commits.
   ```sh
   git rebase -i HEAD~4
   ```

2. **Edit the Rebase List**:
   An editor will open with a list of the last four commits. The commits will be listed in the order they were made, from top (oldest) to bottom (most recent). It will look something like this:
   ```
   pick <commit-hash-1> Commit message 1
   pick <commit-hash-2> Commit message 2
   pick <commit-hash-3> Commit message 3
   pick <commit-hash-4> Commit message 4
   ```

   Change the `pick` to `squash` (or simply `s`) for the second, third, and fourth commits, like this:
   ```
   pick <commit-hash-1> Commit message 1
   squash <commit-hash-2> Commit message 2
   squash <commit-hash-3> Commit message 3
   squash <commit-hash-4> Commit message 4
   ```

3. **Save and Close the Editor**:
   Save the changes and close the editor. This will start the rebase process, and Git will squash the specified commits into a single commit.

4. **Edit the Commit Message**:
   Another editor window will open, allowing you to edit the commit message for the new squashed commit. You can combine all the commit messages or write a new comprehensive message for the squashed commit.

5. **Save and Close the Editor**:
   Save the new commit message and close the editor.

6. **Force Push (if necessary)**:
   If you have already pushed the original commits to a remote repository, you will need to force push the new squashed commit.
   ```sh
   git push origin <branch-name> --force
   ```

7. **Conflict Resolution**:
   During the rebase, you might encounter conflicts. Resolve them and then continue the rebase with:
  ```sh
  git rebase --continue
  ```
