# Setup Git

### ___Install git on your computer___

- Apple: http://git-scm.com/download/mac
- Windows: https://gitforwindows.org/
- Linux: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

### ___Create a new repository___

Create with these steps:

- create a new project directory
- open it
- type the command  `git init`

You created a new git repository.

### ___Add files to your project___

Adding files to your project is not just drag and drop.
Besides moving files into your directory, you need to type some commands.
You can add files using the commands:

- `git add <filename>`
- `git add *`

This is the first step when working with git. To commit these changes use the command:

- `git commit -m "Commit message"`

Now the file is committed, but it is not your remote repository yet.

### ___Remote repository___
___Online Git services___

You can put your project online in a so called **remote repository**. By doing this, multiple people can work on the same project.

There are several free services available for this including Github, Gitlab and Bitbucket. You may also choose to setup your own Git service using Gogs.

___Putting your Project online___

By typing the `git commit` command your changes are in your local working copy.

To send  to remote repository:
```sh
- git push origin master
```
To connect to a remote repository:
```sh
- git remote add origin <server>
```
### ___Checkout online repository___
___Work on Online Git project___

If you want to work on an existing Git project, you need to download it to your computer.

To download, you can use this command:
- `git clone username@host:/path/to/repository`

Popular Git services will give you the link of your Git repository.

___Work on Local Network Git project___

If it's on a network drive, you can use the command:
- `git clone /path/to/repository`

### ___Undo___

Sometimes people make mistakes. If you made a mistake but didn't push it to the online git repository yet, you can undo with:
- `git commit --amend`

That may be like this:
- `git commit -m 'Initial commit'`
- `git add forgotten_file`
- `git commit --amend`

If you already put your mistakes online in the remote git repository, you can roll back using **git reset** (you will lose all changes).

- `git reset --hard (commit code)`

### ___What is branching___
Branches let you work on features isolated from each other. You can think of a branch as a copy of the entire project, but changes don't affect what the other programmers are doing.

The master branch is the default branch. Git lets you switch between branches and you can mix branches together (called merging).

Consider the image below, where:
- **master** branch is the default **branch**
- a branch named "your work" is created
- a branch named "someone else's work" is created

The two people work on the branches individually. And changes are **merged** into the master project.

___Commands___

To see local branches, run this command:
```sh
git branch
```

To see remote branches, run this command:
```sh
git branch -r
```

To see all local and remote branches, run this command:
```sh
git branch -a
```

To create a branch named feature_x
```sh
git checkout -b feature_x
```

To switch branch to the master branch
```sh
git checkout master
```

To delete a branch
```sh
git branch -d feature_x
```

To put your branch online (Q&A)
```sh
git push origin <branch>
```
```sh
git push -u origin <branch>
```
**Remarks:** [You can check, What different between both [You can check, What different between both ](https://github.com/attthurein/Git-Command-Line-Learning-Note/blob/main/Q%26A/Q%26A_1.md)

```sh
git push -u origin <branch>
```

To merge a branch
```sh
git merge <branch>
```

### ___Sync project and Merge___

If you use an online git repository, other people can make changes at the same time. To turn your git project into the latest version, run the command `git pull`

If you work in a branch, you can merge your changes with `git merge <branch>`


