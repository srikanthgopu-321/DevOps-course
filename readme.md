# Git Notes

## Course Overview

In this course, you will learn the fundamentals of Git and Distributed Version Control Systems (DVCS).

### Topics Covered

#### 1. Distributed Version Control Basics
- What a Distributed Version Control System (DVCS) is
- Benefits of distributed version control
- How Git tracks and manages changes

#### 2. Basic Git Commands
- Initialize a repository
- Track files and changes
- Commit changes
- View repository status and history

#### 3. Core Git Concepts

##### Branching
Create new features without affecting the current working version.

**Key Commands:**
```bash
git branch
git checkout
git switch
git merge
```

##### Collaboration
Work with other developers using remote repositories.

**Key Concepts:**
- Clone repositories
- Push changes
- Pull updates
- Rebase
- Resolve merge conflicts

**Key Commands:**
```bash
git clone
git push
git pull
git fetch
git rebase
```

##### Stashing
Temporarily save uncommitted changes without committing them.

**Key Commands:**
```bash
git stash
git stash list
git stash apply
git stash pop
```

##### Cherry-pick
Select and apply specific commits from one branch to another.

**Key Command:**
```bash
git cherry-pick <commit-hash>
```

---

## Learning Outcomes

By the end of this course, you will be able to:

- Understand Distributed Version Control Systems
- Use Git for version control
- Create and manage branches
- Collaborate with other developers
- Resolve merge conflicts
- Temporarily save work using stashing
- Apply specific commits using cherry-pick
- Work confidently with local and remote repositories

---

## Git Workflow Overview

```text
Working Area
      ↓ git add
Staging Area
      ↓ git commit
Local Repository
      ↓ git push
Remote Repository
```

### Common Workflow

```bash
git add .
git commit -m "Your commit message"
git push origin main
```

---

## Let's Get Started!

Git is one of the most widely used version control systems in software development. Mastering Git will help you track changes, collaborate efficiently, and manage code with confidence.
