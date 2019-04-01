# Forking

> A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.

Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.

## For a repository

Forking a repository is simple.

1. On the top right corner of this project page, click **Fork**.
2. That's it! You now have a copy of this project on your own profile.

![forking](https://help.github.com/assets/images/help/repository/fork_button.jpg)

## Clone your fork to your machine

1. On GitHub, navigate to **your fork** of this project.
2. Under the repository name, click **Clone or download**.

![cloning](https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png)

3. In the clone with HTTPs section, click the icon to copy the URL for the repository.

[copy url](https://help.github.com/assets/images/help/repository/https-url-clone.png)

4. Open Terminal.
5. Type `git clone`, and then paste the URL you copied. It will look like this, with your GitHub username instead of `YOUR-USERNAME`.

```sh
git clone https://github.com/YOUR-USERNAME/git-workshop
```

6. Press **Enter**. Your local clone will be created.

## Syncing a fork

It's good practice to regularly sync your fork with the original (upstream) repository.

### Track the original project

1. In your terminal, change directory into the project.

```sh
$ cd /Users/Enda/code/github.com/git-workshop
```

2. Type `git remote -v` and press **Enter**. You will see the currently configured remote project on GitHub.

```sh
$ git remote -v
origin  git@github.com:YOUR_USERNAME/git-workshop.git (fetch)
origin  git@github.com:YOUR_USERNAME/git-workshop.git (push)
```

3. We need to add the original project, known as the *upstream*, to our remotes.

```sh
$ git remote add upstream https://github.com/craicoverflow/git-workshop.git
```

### Update your fork from upstream

1. Fetch the latest branches and commits. Commits to master will be stored in a local branch, called `upstream/master`.

2. Checkout your local `master` branch.

```sh
$ git checkout master
> Switched to branch 'master'
```

3. Merge the changes from `upstream/master` into your local `master` branch. This brings your fork's `master` branch into sync with the upstream repository.