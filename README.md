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
