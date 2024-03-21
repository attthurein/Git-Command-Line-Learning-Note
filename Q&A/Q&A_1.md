### What different between `git push origin <branch>`  and `git push -u origin <branch>`.
#

> The `git push origin <branch>` command is used to push the commits from your local branch to the remote repository's branch specified by <branch>. When you run this command, Git assumes you want to push the commits to the remote branch matching the same name as your local branch.

#
#

> On the other hand, `git push -u origin <branch>` does the same thing but with an additional option `-u` or `--set-upstream`. This option establishes a tracking relationship between your local branch and the remote branch. It means that after you use -u option once, in the future, when you run git push without specifying the remote and branch, Git will push your changes to the corresponding remote branch that you've set as upstream.
#
So, the main difference is that `git push -u origin <branch>` not only pushes your changes to the remote branch but also sets up a tracking relationship between your local branch and the remote branch, making it more convenient for future pushes.
