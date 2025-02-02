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
