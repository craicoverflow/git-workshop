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
$ git merge left
```