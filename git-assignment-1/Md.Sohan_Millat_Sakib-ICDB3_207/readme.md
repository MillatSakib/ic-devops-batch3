# Git Notes

## What is `Git`

Git is a version control system by using this we can manage our project in effecient way. Git is not only one version control system, there have also another type of version control system like: SVN.

## Git Configuration

We can set some perameter using git configuration system. Specially we can set our Username and Email using this system. We can set the Username and Email using the command below:

Set Username Command:

```bash
git config user.name "Md. Sohan Millat Sakib"
```

Set Email Command:

```bash
git config user.email "sohanmillat55@gmail.com"
```

## Git Basic Comands:

If we want that Git track our project then at first we have to initiate the Git. For this We have to execute the command below:

```bash
git init
```

After executing this command Git are ready for track our project. Now if we want to sent our project file to staging are then we have to add this file using the command below:

```bash
git add <file-name>
```

If we want to sent all file on staging are then we can use the command below:

```bash
git add -A
```

We can also the the command below instead of it.

```bash
git add .
```

Now if we want to add a commit then we can execute the command below:

```bash
git commit
```

After this command the `vim` will open. Then We can Write the commit message and commit description. After add commit message we will press `Esc` button and write `:wq` and press enter.

We can also execute the short command below:

```bash
git commit -m "Commit message"
```

If we want to see the commit log history then we can execute the command below:

```bash
git log
```

If we wat a simplified log history then we have to use `--oneline` flag Like below:

```bash
git log --oneline
```

## Git Remote

Git remote is a way to connect our local repository to a remote repository. It allows you to collaborate with others, share code and synchronize changes between your local and remote repositories. Actually a remote is a pointer to a remote repository. It is essentially a shortcut or alias for the URL of the remote repository. We can check the remote URL using the command below:

```bash
git remote -v
```

We can add the Remote origin using the command below:

```bash
git remote add origin https://gitmillat.com/username/repo.git
```

We have to add multiple remote origin for an project. For that we can add multiple remote origin using different name. Like:

```bash
git remote add millat https://gitmillat.com/username/repo.git
```

We can rename our Origin name. Like below:

```bash
git remote rename <old-name> <new-name>
```

We can update the remote origin using the command below:

```bash
git remote set-url <origin-name> <new-url>
```

### Upstream:

In git upstream refers to original repository or the main source repository from which your local repository or fork was created. We can add the upstream using the command below:

```bash
git remote add upstream https://gitmillat.com/username/repo.git
```

## Git Branch

If we want to add new feature in our project then we can make a new branch and write the code on that branch. We can make a new branch using the command below:

```bash
git branch feature-branch
```

We can checkout to a specific branch using the command below:

```bash
git checkout feature-branch
```

If we want that if the branch are not available the branch are created at first then the checkout will perform otherwise checkout will be directly then we can use the command below:

```bash
git checkout -b feature-branch
```

#### Cherry-Pick command

Suppose you make a commit on another branch then what you will do? Will you totally merge the whole branch? No need it. You can use cherry-pick command for solve this problem. Acually cherry-pick are use to add one or more commit on current branch from another branch. The command procedure of cherry-pick are given below:

At first know about the commit history. For see commit history we can use the command below:

```bash
git log --oneling
```

After copy the the targeted commit hash checkout to the branch in which branch you want to add the commit.

```bash
git checkout main
```

Then execute the command below:

```bash
git cherry-pick <paste-previous-coppied-commit-hash>
```

That is the process. But we can also add multiple commit by adding the commit hashes on the command:

```bash
git cherry-pick abc123 xyz456
```

We can also use the range of commit like below:

```bash
git cherry-pick abc123..xyz456
```

When we perform Cherry-pick then any kind of conflict can perform. So after solve the conflicting issue we have to use the command below:

```bash
git cherry-pick --continue
```

or if we want to cancel the cherry-pick then we can use the command below:

```bash
git cherry-pick --abort
```

### Git Reset:

We can delete the commit using the git reset feature. There have three types of git resetting. They are

- Soft Reset.
- Hard Reset.
- Mixed Reset.

**Soft Reset:** On soft reset the filse are on staged but the commit are deleted. The command are below:

```bash
git reset --soft HEAD~1
```

**Hard Reset:** On hard reset the file and commit are deleted.

```bash
git reset --hard HEAD~1
```

**Mixed Reset:** On Mixed reset the file goes to on unstaged and the commits are removed.

```bash
git reset --mixed HEAD~1
```

## Git Pull, Fetch

Git pull and fetch are related concept but not same. When we pull then the code are fetch at first and then merge the code with current branch. And fetch to bring the code only. Don't merge with the existing branch.

We can execute the command below for pull

```bash
git pull origin main
```

We can execute the command below for fetch

```bash
git fetch origin
```

Then if we want to merge the code then we have to execute the command below:

```bash
git merge origin/main
```

## Git Rebasing:

There are two type of rebasing. They are:

- Standard Rebasing.
- Interactive Rebasing.

**Standard Rebasing:** Using Standard Rebasing we can merge two branch. We can also rebase with remote origin.

Now why we will use Standard Rebasing?

For three reason:

- Clean History: Rebasing creates a linear commit history, making it easier to understand the project’s evolution.

- Avoid Merge Commits: Rebasing avoids unnecessary merge commits, which can clutter the history.

- Syncing Branches: It’s useful for keeping a feature branch up to date with the latest changes from the main branch.

#### Standard Rebasing Process:

If we want to rebasing with another branch then follow the steps:

At first checkout to your new branch:

```bash
git checkout feature-branch
```

Then rebase with main:

```bash
git rebase main
```

If any conflict occurs then at first resolve all conflicts and then execute the command below:

```bash
git add -A
git rebase --continue
```

If we want to rebase with remote origin the follow the steps below:
At first fetch the remote origin.

```bash
git fetch origin
```

Then checkout your new branch:

```bash
git checkout feature-branch
```

Then rebase with the remote origin:

```bash
git rebase origin/main
```

**Interactive Rebasing Process:**
Interactive rebase allows to modify commits as we want to rebase them. You can do using interactive Rebasing:

- Reorder commits.

- Squash multiple commits into one.

- Edit commit messages.

- Split commits.

- Drop commits.

For this you have to write the command below at first.

```bash
git rebase -i HEAD~3
```

After enter this command then open a vim terminal where they ask on which commit which action we want to perform. Then we have to edit this file as per our requirement. For that we have to press `Esc` key at first. Then we have to write `:wq`. Then It is ready to rebasing. Now we can add file and perform the command below:

```bash
git add -A
git commit --amend
git rebase --continue
```

If we decide that we don't rebase then we can execute the command below:

```bash
git rebase --abort
```
