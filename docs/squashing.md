# Squashing

When submitting a pull request, it is good practice to squash any commits before merging into `master`.

1. Make sure your branch is up to date with `master`. See [Rebasing](rebasing.md).

2. Run `git rebase -i <your-branch-name>`. You should see a list of commits, each starting with the work `pick`.

3. Make sure the first commit says "pick", and change the rest from "pick" to squash. This will squash each commit into the previous commit.

4. Save and close the editor.

5. You will get the opportunity to change the commit message.

6. Now you can force push the final, squashed commit: `git push -f`.