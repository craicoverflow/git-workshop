# Pull Requests

Pull requests let you request that your code changes become merged into the main project. Once a pull request is created, you can discuss and review potential changes with collaborators.

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