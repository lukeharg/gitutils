# Git Utils
User Guide (Updated 6 December 2017)

## What is Git Utils?
Bringing together useful information for initial project setup with Github.

## Setting Up
[Download and Install](https://git-scm.com/downloads) Git on your local machine. Then set your user name and email address, as this is used by Github to identify you.
```bash
$ git config --global user.name "Rick Hunter"
$ git config --global user.email "rick@example.com"
```

## Getting Started
### Create a local repository
```bash
$ mkdir gitutils
$ cd gitutils
$ git init
$ echo "# gitutils" >> README.md
$ git add README.md
$ git commit -m "first commit"
```
### Configure GitHub SSH
[Create an SSH private key](https://gist.github.com/colinstein/8e1a0b12465561d71e91#doing-it-the-hard-way) and [configure GitHub to use it](https://help.github.com/en/enterprise/2.15/user/articles/adding-a-new-ssh-key-to-your-github-account).

In ~/.ssh/config, add:
```bash
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/example.pem
```
You can now [test to see if this has worked](https://help.github.com/en/github/authenticating-to-github/testing-your-ssh-connection).
### Link the repository to GitHub
[Create a new repository](https://help.github.com/articles/creating-a-new-repository/) on GitHub. To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub.

You can now add your Github origin and push to it.
```bash
$ git remote add origin https://github.com/luclabs/gitutils.git
$ git push -u origin master
```

## Tutorials
### Adding changes
```bash
$ git add .
$ git commit -m "My changes."
$ git push
```
Note that the origin and branch don't need to be specified because the upstream was set (-u flag) in the previous push.

### Pulling changes from Github
```bash
$ git pull
```

## Best Practices
- It is recommended every repository include a README, [LICENSE](https://choosealicense.com/), and .gitignore.

## Resources
1. https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
2. https://www.atlassian.com/git/tutorials/gitignore
3. https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf
