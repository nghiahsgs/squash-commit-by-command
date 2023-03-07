# test-squash-by-command
test squash by command

```
git rebase -i HEAD~3
```

```
pick hash_commit_1 -> pick hash_commit_1
pick hash_commit_2 -> squash hash_commit_2
pick hash_commit_3 -> squash hash_commit_3
```

```
git push -f
```




First, ensure that you are on the branch that contains the commits you want to squash. You can use the command git branch to check which branch you are on, and git checkout to switch to the correct branch.

Next, use the command git log to view a list of the commits on the branch. Note the commit hashes of the commits you want to squash.

Use the command git rebase -i <commit hash> to begin an interactive rebase session. Replace <commit hash> with the hash of the commit that immediately precedes the first commit you want to squash. For example, if you want to squash the last three commits, you would use the hash of the commit before the first of those three commits.

This will open up an interactive rebase editor, displaying a list of all the commits you want to squash. Replace the word "pick" with "squash" or "s" for each commit you want to squash. Save and close the editor.

Git will then combine the commits and open another editor window where you can enter a new commit message for the squashed commit. Edit the commit message as needed, save, and close the editor.

Finally, use the command git push --force to push the changes to the remote repository.
