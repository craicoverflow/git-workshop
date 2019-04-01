# Pull Requests

Create a pull request to request and collaborate on changes to a repository. These changes are proposed in a *branch*, which ensures that the `master` branch only contains finished and approved work.

## Creating a pull request

1. On GitHub, navigate to the main page of the repository.

2. In the "Branch" menu, choose the branch that contains your commits.

![](https://help.github.com/assets/images/help/pull_requests/branch-dropdown.png)

3 To the right of the Branch menu, click **New pull request**.

4. Use the *base* branch dropdown menu to select the branch you'd like to merge into. This should nearly always be master.

5. Use the *compare* branch drop-down menu to choose the branch you made your changes in.

6. Type a title and description for your pull request.

7. Click **Create Pull Request**.

## Viewing a pull request locally

You might want to test that someone else's pull request code actually works. For that you can check it out on your machine.

1. Under the repository name, click **Pull Requests**.

![pull-requests](https://help.github.com/assets/images/help/repository/repo-tabs-pull-requests.png)

2. From the list of pull requests, click the one you want to view locally.

3. Near the bottom of the pull request, in the merge box, click **command line instructions**. Follow the sequence of steps to bring down the proposed pull request.

![](https://help.github.com/assets/images/help/pull_requests/pull_request_show_command_line_merge.png)

```sh
git checkout -b craicoverflow-dummy-pull-request master
git pull https://github.com/craicoverflow/git-workshop.git dummy-pull-request
```