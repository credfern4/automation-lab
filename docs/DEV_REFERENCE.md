# Developer Reference Guide

This document is a running reference for tools, commands, and concepts learned while building the Automation Lab.

---

## Status Key

- [ ] Not Started
- [~] In Progress
- [x] Complete

---

# Git Quick Reference

## Check repository status

```bash
git status
```

## Add files to staging

```bash
git add filename
```

## Commit staged files

```bash
git commit -m "message"
```

## Push changes to GitHub

```bash
git push
```

## View commit history

```bash
git log --oneline
```

## Visual history

```bash
git log --graph --decorate --oneline
```

## Typical Git workflow

```text
edit file
git add
git commit
git push
```

## .gitignore (Ignoring Files)

Use a `.gitignore` file to tell Git which files should **not** be tracked in a repository.

Example `.gitignore` entry:

```text
.DS_Store
```

Common files often ignored in projects:

```text
.DS_Store
__pycache__/
.env
node_modules/
```

If a file was already committed before adding it to `.gitignore`, remove it from Git tracking while keeping the local file:

```bash
git rm --cached filename
```

Then commit the change:

```bash
git commit -m "Remove file and update .gitignore"
```

---

# Python Quick Reference

## Run a Python script

```bash
python3 script.py
```

## Check Python version

```bash
python3 --version
```

## Check pip version

```bash
pip3 --version
```

---

# VS Code Tips

## Open folder in VS Code

```bash
code .
```

## Open integrated terminal

Use:

```text
Terminal → New Terminal
```

## Python extension provides

- syntax highlighting
- linting
- debugging
- interpreter selection

---

# Repository Structure

```text
automation-lab/
├── README.md
├── learning/
├── docs/
├── setup/
└── projects/
```

---

# AI Tools

Primary tools being explored:

- ChatGPT
- Claude
- GitHub Copilot
- Google Gemini
- NotebookLM

Primary use cases:

- coding assistance
- documentation
- automation design
- research workflows

---

# Notes

Use this document as a living quick reference and expand it as new tools, commands, and workflows are learned.