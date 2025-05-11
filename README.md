
# Git Commands & Workflow Guide

_A little late to post, but here's a handy reference for myself and others to understand and review common Git commands and workflows._

---

## 📁 Creating a Project Directory

```bash
mkdir project-name
````

Use `ls` for Linux/macOS or `dir` for Windows to list files.

---

## 🔧 Initializing Git

```bash
git init
```

* Initializes a Git repository in the current directory.
* Creates a hidden `.git` folder to store version history.
* Run only once per project.

To view hidden files like `.git`, use:

```bash
dir /a:h
```

⚠️ **Do not manually modify the `.git` directory.**

---

## 📌 Git Workflow Basics

1. **Working Directory** – Where you write your code.
2. **Staging Area** – Use `git add` to stage changes.
3. **Repository** – Use `git commit` to save checkpoints.

---

## ✅ Tracking Files

```bash
git add filename
git add file1 file2
```

* Moves files to the **staging area**.
* To remove a file from staging without deleting it:

```bash
git rm --cached filename
```

---

## 📍 Committing Changes

```bash
git commit -m "Your message here"
```

* `-m` is used to specify a commit message.
* To open the commit editor (like VS Code), set your editor:

```bash
git config --global core.editor "code --wait"
```

This ensures Git waits until you close the editor window.

---

## 👤 Git Identity Configuration

```bash
git config --global user.name "Jeeva Vinod"
git config --global user.email "jeevaj3v12@gmail.com"
```

These settings associate commits with your name and email.

---

## 📜 Git Status and Logs

```bash
git status
```

* Shows staged, unstaged, and untracked files.

```bash
git log --oneline
```

* Shows commit history in brief (one line per commit).

---

## 🚫 Ignoring Files

To prevent tracking sensitive or unnecessary files:

1. Create a `.gitignore` file.
2. Add files or patterns to it, e.g.:

```
.env
node_modules/
*.log
```

* VS Code: `code .gitignore`
* Changes take effect only **before** staging files.

---

## 🧪 Working with Branches

```bash
git branch
```

* Lists all branches.
* Default branch is usually `master` or `main`.

```bash
git branch jee-va
```

* Creates a new branch named `jee-va`.

```bash
git checkout jee-va
```

* Switches to `jee-va` branch.

You can now create or modify files in this branch.

---

## 🔄 Merging Branches

1. Switch to the branch you want to merge **into**:

```bash
git checkout master
```

2. Merge the other branch:

```bash
git merge jee-va
```

> ⚠️ If both branches modify the same file, Git will raise a **merge conflict**.

---

## 🔗 How Commits Work

* Every commit creates a unique **hash**.
* New commits are connected to previous ones like a chain.
* This enables rollbacks and history tracking.

---

## 🧵 Summary Commands

```bash
git init
git status
code filename.extension
git add filename.extension
git commit -m "Commit message"
```

---

## ✨ Example Workflow

```bash
mkdir git-practice
cd git-practice
git init
code index.html
git add index.html
git commit -m "Add index.html"
```

---

Feel free to modify and extend this guide as you learn more about Git!

```
