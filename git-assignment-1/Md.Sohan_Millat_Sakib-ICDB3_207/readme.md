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
