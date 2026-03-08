

# Mac Development Setup

Steps used to configure the Automation Lab environment on macOS.

---

## Status Key

- [ ] Not Started
- [~] In Progress
- [x] Complete

---

# Overview

This guide documents the setup process used to configure a Mac for Python, Git, VS Code, and GitHub-based development.

---

# Install Homebrew

Run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

If `brew` is not immediately found after installation, run:

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv zsh)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv zsh)"
```

Verify installation:

```bash
brew --version
```

Notes:

- Homebrew is a package manager for macOS.
- It installs and manages developer tools like Git and Python.

---

# Install Git

Run:

```bash
brew install git
```

Verify:

```bash
git --version
which git
```

If macOS is still using Apple Git instead of the Homebrew version, refresh the shell command cache:

```bash
hash -r
```

Then verify again:

```bash
which git
git --version
```

Expected Homebrew Git location:

```text
/opt/homebrew/bin/git
```

---

# Configure Git

Set username:

```bash
git config --global user.name "Your Name"
```

Set email:

```bash
git config --global user.email "your@email.com"
```

Verify settings:

```bash
git config --global user.name
git config --global user.email
cat ~/.gitconfig
```

Set the default branch name for future repositories:

```bash
git config --global init.defaultBranch main
```

---

# Install Python

Run:

```bash
brew install python
```

Verify:

```bash
python3 --version
pip3 --version
which python3
which pip3
```

If macOS is still using the system Python instead of the Homebrew version, refresh the shell command cache:

```bash
hash -r
```

Then verify again:

```bash
which python3
python3 --version
which pip3
pip3 --version
```

Expected Homebrew Python location:

```text
/opt/homebrew/bin/python3
```

Expected Homebrew pip location:

```text
/opt/homebrew/bin/pip3
```

Notes:

- Use `python3` and `pip3` on macOS.
- `pip3` installs Python packages for the active Python 3 environment.

---

# Install VS Code

Download from:

```text
https://code.visualstudio.com
```

Open VS Code and install the Python extension from Microsoft.

Recommended extensions:

- Python
- GitHub Copilot
- GitLens (optional)

---

# Create Project Folder

Create the workspace folder:

```bash
mkdir ~/automation-lab
ls ~
```

Expected result:

- `automation-lab` appears in your home directory listing.

Open the folder in VS Code using:

- File → Open Folder
- Select `automation-lab`

---

# Initialize Git Repository

Open a terminal inside VS Code and run:

```bash
git init
```

If needed, rename the initial branch to `main`:

```bash
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

```bash
python3 hello.py
```

Expected output:

```text
Hello from Chip's Automation Lab
```

---

# First Git Workflow

Check status:

```bash
git status
```

Stage the file:

```bash
git add hello.py
```

Commit:

```bash
git commit -m "First commit - hello automation lab"
```

View history:

```bash
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

```bash
git remote add origin https://github.com/YOUR-USERNAME/automation-lab.git
```

Verify:

```bash
git remote -v
```

Push the branch:

```bash
git push -u origin main
```

---

# Add README

Create:

```text
README.md
```

Then follow the normal workflow:

```bash
git add README.md
git commit -m "Add README"
git push
```

---

# Useful Commands Learned

```bash
brew --version
git --version
python3 --version
pip3 --version
which git
which python3
which pip3
git status
git add .
git commit -m "message"
git push
git log --oneline
git log --graph --decorate --oneline
hash -r
```

---

# Notes

Use this guide as a living Mac setup reference and update it as the environment evolves.