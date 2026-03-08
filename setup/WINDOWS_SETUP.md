

# Windows Development Setup

Steps to replicate the Automation Lab environment on Windows.

---

## Status Key

- [ ] Not Started
- [~] In Progress
- [x] Complete

---

# Overview

This guide documents the setup process for a Windows-based development environment using Git, Python, VS Code, and GitHub.

---

# Recommended Approach

Start with native Windows tools first:

- PowerShell
- Git for Windows
- Python for Windows
- VS Code

Later, optionally explore:

- WSL (Windows Subsystem for Linux)

This guide focuses on the native Windows approach.

---

# Install Git

Download Git for Windows from:

```text
https://git-scm.com/download/win
```

Install using the default recommended options unless you have a specific reason to change them.

After installation, open PowerShell and verify:

```powershell
git --version
where.exe git
```

Notes:

- `where.exe git` is the Windows equivalent of `which git`.
- Git for Windows usually installs Git Bash in addition to PowerShell support.

---

# Configure Git

Set username:

```powershell
git config --global user.name "Your Name"
```

Set email:

```powershell
git config --global user.email "your@email.com"
```

Verify:

```powershell
git config --global user.name
git config --global user.email
git config --list
```

Set the default branch name for future repositories:

```powershell
git config --global init.defaultBranch main
```

---

# Install Python

Download Python from:

```text
https://www.python.org/downloads/windows/
```

Important during installation:

- check the box for `Add Python to PATH`

Verify in PowerShell:

```powershell
python --version
pip --version
where.exe python
where.exe pip
```

Notes:

- On Windows, the command is typically `python` instead of `python3`.
- On Windows, the command is typically `pip` instead of `pip3`.

If Python is not recognized after installation, close and reopen PowerShell and test again.

---

# Install VS Code

Download from:

```text
https://code.visualstudio.com
```

Install recommended extensions:

- Python
- GitHub Copilot
- GitLens (optional)

---

# Create Project Folder

In PowerShell:

```powershell
mkdir automation-lab
cd automation-lab
```

Verify location:

```powershell
pwd
```

Expected result:

- the current folder should now be `automation-lab`

Open the folder in VS Code using:

- File → Open Folder
- select `automation-lab`

Or, if the `code` command is enabled:

```powershell
code .
```

---

# Initialize Git Repository

Open a terminal in VS Code and run:

```powershell
git init
```

If needed, rename the branch to `main`:

```powershell
git branch -m main
git branch
```

---

# Create First Python Script

Create:

```text
hello.py
```

Add:

```python
print("Hello from Chip's Automation Lab")
```

Run:

```powershell
python hello.py
```

Expected output:

```text
Hello from Chip's Automation Lab
```

---

# First Git Workflow

Check status:

```powershell
git status
```

Stage the file:

```powershell
git add hello.py
```

Commit:

```powershell
git commit -m "First commit - hello automation lab"
```

View history:

```powershell
git log --oneline
git log --graph --decorate --oneline
```

---

# Connect to GitHub

Create an empty GitHub repository named:

```text
automation-lab
```

Do not initialize it with:

- README
- .gitignore
- license

Add the remote:

```powershell
git remote add origin https://github.com/YOUR-USERNAME/automation-lab.git
```

Verify:

```powershell
git remote -v
```

Push the branch:

```powershell
git push -u origin main
```

You may be prompted to authenticate in the browser.

---

# Add README

Create:

```text
README.md
```

Then follow the normal workflow:

```powershell
git add README.md
git commit -m "Add README"
git push
```

---

# Useful Commands Learned

```powershell
git --version
python --version
pip --version
where.exe git
where.exe python
where.exe pip
git status
git add .
git commit -m "message"
git push
git log --oneline
git log --graph --decorate --oneline
```

---

# Optional Next Step: WSL

After you are comfortable with native Windows, consider exploring:

- WSL
- Ubuntu on Windows
- Linux-style development workflows

This is common for developers, but not required to begin learning Python automation and Git.

---

# Notes

Use this guide as a living Windows setup reference and update it as the environment evolves.