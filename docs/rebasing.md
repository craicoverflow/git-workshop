# Rebasing

Before merging a pull request, we need to make sure that your current branch is up to date with your `master` branch.

1. Fetch the latest changes from `upstream`.

```sh
$ git fetch upstream
```

2. Now we can update our branch with these changes from `upstream/master`.

```sh
$ git rebase upstream/master
```

3. Git might ask you to fix conflicts. Let's look at [conflicts](conflicts.md) next.