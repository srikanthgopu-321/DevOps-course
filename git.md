# GIT BASICS

In this course, you will learn:

* Distributed Version Control basics
* Basic Git commands
* Core concepts of Git like:

  * Creating new features without affecting the current working version (Branching)
  * Collaborating with other developers (Clone, Push, Rebase and Merge Conflicts)
  * Saving new changes temporarily (Stashing)
  * Selecting particular changes from others (Cherry-pick)

---

## Version Control

Version Control is a system which records the changes made to a file so that you can recall a specific version later.

### Common Git Commands

* `git clone` : Get the complete project from remote to your local machine
* `git pull origin <branch_name>` : Get the new changes from remote branch to local branch
* `git push origin <branch_name>` : Send your local branch changes to the remote branch
* `git remote add <name> <url>` : Used to connect local Repository to Remote Repository
* `git remote -v` : List all the remote repo URLs linked to your local repo

---

# Git Terminologies

Before starting with the basics, let's explore a few terminologies:

### Git Repository

A directory with `.git` folder, where all the contents are tracked for changes.

### Remote

It refers to a server where the project code is present. For example, Github and Gitlab.

### Commit

It is similar to version. When you make changes in a file, you need to commit the changes in order to save and create its new version, which will create a unique commit hash (like version number).

### Origin

It is a variable where Git stores the URL of your remote repository.

Example:

`origin => www.github.com/username/myrepo`

---

# Git Basic Commands

### git init

Adds `.git` folder and initializes the current folder to track its changes.

### git status

Displays the current state of the staging area and the working directory, that is, which files are added/removed/modified.

### git diff

Shows the exact changes with line and column number.

### git add

Adds the changes to the staging area. If you have added a new file, this command starts tracking the file for modifications.

### git commit

Will save all the changes with a unique hash number in the local repository.

### git push

Sends the changes to the remote repository (server).

---

# Git Workflow

The following are the three stages in the Git workflow:

### Working Area

You can edit files using your favorite editor/Integrated Development Environment (IDE).

### Staging Area

You have made the changes and added the changes to Git. You can still make changes here.

It is like taking an item out of the box, where the box is the staging area.

Command:

`git add`

### Local Repository

You have finalized the changes and committed them with a new hash and proper message.

Command:

`git commit`

### Remote Repository

You can now push the changes to online platforms like Github or Gitlab from where others can collaborate.

Command:

`git push`

---

# Local to Remote

In the previous topic, whatever you have learned was mostly limited to your local machine.

To collaborate with other developers, you need to push your work to the remote repository, and vice-versa, you need to pull others' work from remote to contribute your work to the project.

In Git, remote is a repository on a server where all your team members can place the code to collaborate.

---

# Git Pull

Your teammate has pushed the changes to the project's remote repo where you are also working.

You can now pull the changes to your local machine using any one of the following commands.

### git pull

`git pull` is the convenient shortcut key to fetch and merge the content.

```bash
git pull <remote_name> <branch_name>
```

### git fetch

`git fetch` command downloads the remote content to your local repo, without changing your code changes.

```bash
git fetch <remote_name> <branch_name>
```

Fetches the content from that specific branch in remote to your current working area.

### git merge

`git merge` command merges the fetched remote content to the local working tree.

```bash
git merge <remote_name>/<branch_name>
```

Merges the content to the specified branch.

---

# Git Push

To keep your changes and work in remote repo, you need to push the branch using the command:

```bash
git push <remote_name> <branch_name>
```

Git push takes two arguments, namely:

* `<remote_name>`
* `<branch_name>`

For example:

```bash
git push origin master
```

Where:

* `origin` will contain the remote URL
* `master` is the branch that is pushed

(We shall discuss branches later in this course)

---

# Working with Existing Projects

Peter is new to the project. For a particular task, he created ten new files in his local machine.

His technical lead said there is a common repo where all the team members place their code. He asked Peter to push his files to the same repo.

What should Peter do?

In such a scenario, you can connect your local repo with an existing remote repo using `git remote add` command.

---

# Git Remote

The syntax to link your local repo with remote repo is:

```bash
git remote add <remote_name> <remote_url>
```

---

# Branching

To build new features without affecting the current working code, you need to:

1. Create new branch from the master

```bash
git branch <branchname>
```

Here you will write code for the new feature.

2. Merge the feature branch with the master (or other branch where you want it to be).

You can merge two branches locally or in remote.

---

# Branch Operations

You can do the following with branch:

### Creating New Branch

```bash
git checkout -b <branch-name>
```

### Pushing Branch from Local to Remote Repo

```bash
git push origin <branch-name>
```

### Renaming Branch

#### Renaming Local Branch

```bash
git branch -m old-name new-name
```

#### Renaming Remote Branch

```bash
git push origin :old-name new-name
```

### Deleting Branch

#### Deleting Local Branch

```bash
git branch -d <branch-name>
```

#### Deleting Remote Branch

```bash
git push origin -d <branch-name>
```

---

# Integrating Changes

Once you have developed your feature in a separate branch, you need to integrate the feature and master branch.

You can do that using one of the following two commands:

* merge
* rebase

### Merge

Merge is an operation to integrate changes from one branch to another branch by adding a new commit.
