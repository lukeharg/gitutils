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
### Link the repository to GitHub
[Create a new repository](https://help.github.com/articles/creating-a-new-repository/) on GitHub. To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub.

You can now link and push your repository to Github.
```bash
$ git remote add origin https://github.com/luclabs/gitutils.git
$ git push -u origin master
```

## Tutorials
TODO: What is credential helper?

## Best Practices
- It is recommended every repository include a README, [LICENSE](https://choosealicense.com/), and .gitignore.

## Resources
1. https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
2. https://www.atlassian.com/git/tutorials/gitignore
