# Conflicts

Conflicts in Git can occur when trying to merge changes from two different branches.

## Practical

Let's make a new branch and add a file:

```sh
git checkout -b left master

echo "Left is the best" > conflict.txt

git add conflict.txt
git commit -m "Left is the best"
```

```sh
git checkout -b right master

echo "Right is the best" > conflict.txt
git add conflict.txt
git commit -m "Right is the best"
```

We've made changes here in the same file, in two separate branches. If we try to integreate these branches, we are going to see a conflict. It's merge `left` and `right` to see a conflict.

```sh
$ git rebase left
Auto-merging conflict.txt
CONFLICT (add/add): Merge conflict in conflict.txt
Automatic merge failed; fix conflicts and then commit the result.
```

Our rebase has been paused until we resolve conflicts.

Let's open `conflict.txt` in our editor and go through how to resolve this conflict.

```txt
<<<<<<< HEAD
Right is the best
=======
Left is the best
>>>>>>> left
```

Once we have manualy resolved the conflict, we need to `git add`.

```sh
$ git add conflict.txt
```

Now let's continue with our rebase:

```sh
$ git rebase --continue
Applying: Right is the best
```

## Diving deeper

### Aborting a merge

We can abort a merge that's in progress by using the `git merge --abort` command.

### Minimising merge conflicts

To minimise merge conflicts keep commits small and integrate changes often.