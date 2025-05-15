
# 🧠 Git Cheat Sheet for GLA Notebook Workflow

This guide helps you understand how Git works, why you need it, and which commands you’ll use most in a solo project like the GLA newsletter.

---

## 🧭 What is Git, and why use it?

Git is **version control software** — it tracks every change you make to your code or files, lets you go back to previous versions, and safely backs things up to GitHub.

Think of it as "save + backup + history" for everything in your project folder.

- ✅ Helps you avoid losing work
- ✅ Lets you see what changed and when
- ✅ Makes it easy to work across devices (or with collaborators)

---

## 📁 How a Git Repo Works

When you run `git init`, Git starts watching everything in that folder (and subfolders).

### Your working files go through 3 states:

1. **Untracked** → New files Git hasn't seen yet  
2. **Staged** → Files you marked for commit  
3. **Committed** → Files officially saved in Git history  
4. **Pushed** → Commits uploaded to GitHub (for backup or sharing)

---

## ✅ Daily Git Routine

### 📅 End of Day (before turning off)

Save your work and upload it to GitHub:

```bash
git add .
git commit -m "Brief summary of today's changes"
git push
```

This commits and backs up your work.

---

### ☀️ Start of Day (when you reopen your laptop)

Check for any updates (even if you're the only one using it):

```bash
git pull
```

---

## ✅ Basic Git Commands

| Command | Description |
|--------|-------------|
| `git status` | See what's changed, staged, or untracked |
| `git add .` | Stage all changes for commit |
| `git commit -m "message"` | Save changes with a message |
| `git push` | Upload local commits to GitHub |
| `git pull` | Download any remote changes |
| `git log --oneline --graph` | View commit history in a clean format |

---

## 🛠 Undo / Fix

| Command | Description |
|--------|-------------|
| `git checkout -- filename` | Undo uncommitted changes to a file |
| `git reset filename` | Unstage a file you added |
| `git reset --soft HEAD~1` | Undo last commit but keep your edits |

---

## 📄 .gitignore — What It Is

The `.gitignore` file tells Git what *not* to track — great for hiding:

- Temporary files
- HTML exports
- Jupyter autosave folders

Example:

```
.ipynb_checkpoints/
*.html
.vscode/
__pycache__/
```

---

## 🧠 Best Practices

- Commit **small and often** with clear messages
- Pull **before** you start work for the day
- Push changes **before** shutting down or switching devices
- Never commit sensitive info (e.g. passwords, personal emails)

---

## 🗂 Typical Workflow for GLA Project

1. Do your work in Jupyter/VS Code  
2. When you're happy with a section:
    ```bash
    git add .
    git commit -m "finished editorial section draft"
    git push
    ```

3. Next morning:
    ```bash
    git pull
    ```

---

This is all you need to safely manage your repo, back up your files, and track progress on the GLA newsletter.

