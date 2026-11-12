# Git – Version Control System

## 1. Introduction

Git is a free and open-source distributed version control system used to track changes in files and coordinate software development.

It helps developers maintain different versions of a project, recover previous versions, and collaborate with other developers.

Git was developed by Linus Torvalds in 2005.

## 2. Objectives

- Understand the need for version control.
- Learn Git and its features.
- Create and manage Git repositories.
- Understand the working directory, staging area, and repository.
- Learn essential Git commands.
- Understand branching and merging.
- Upload and maintain projects on GitHub.
- Collaborate through pull requests.

## 3. What Is Version Control?

Version control is a system that records changes made to files over time.

It allows users to:

- Track modifications to files.
- Identify who made changes and when.
- Restore previous versions.
- Compare different versions.
- Collaborate with multiple developers.

### Why Do We Need Version Control?

Without version control, developers may face problems such as:

- Accidental deletion or overwriting of files.
- Difficulty identifying the latest version.
- Loss of previous working versions.
- Difficulty combining changes from multiple developers.

Version control makes project history organized and manageable.

## 4. Types of Version Control Systems

### 1. Local Version Control System

Stores different versions of files on a single computer.

### 2. Centralized Version Control System

Stores project history on a central server.

Example: Subversion (SVN).

### 3. Distributed Version Control System

Each user has a complete copy of the repository, including its history.

Example: Git.

## 5. Introduction to Git

Git is a distributed version control system that helps developers track and manage project changes.

### Features of Git

1. Distributed system.
2. Fast performance.
3. Branch-based development.
4. Easy merging.
5. Maintains project history.
6. Supports offline development.
7. Open-source software.

## 6. Git vs GitHub

| Feature | Git | GitHub |
|---|---|---|
| Type | Version control system | Hosting platform |
| Location | Works locally | Online platform |
| Purpose | Tracks changes | Hosts and shares projects |
| Network | Can work offline | Online features need internet |
| Collaboration | Branches and merges | Pull requests and code reviews |

Git manages version history, while GitHub provides hosting and collaboration features.

## 7. Git Architecture

Git mainly works with three areas:

### 1. Working Directory

The location where project files are created and modified.

### 2. Staging Area

The area where selected changes are prepared for the next commit.

### 3. Local Repository

Stores committed project history.

### Git Workflow

Working Directory → Staging Area → Local Repository → Remote Repository

Important commands:

```bash
git add .
git commit -m "Initial commit"
git push
```

## 8. Installing Git

Git can be downloaded from:

https://git-scm.com/downloads

For Windows, download and install Git using the official installer.

For Ubuntu/Debian:

```bash
sudo apt update
sudo apt install git
```

For macOS:

```bash
brew install git
```

### Verify Installation

```bash
git --version
```

This displays the installed Git version.

## 9. Configuring Git

Git uses configuration values to identify the author of commits.

### Set Username

```bash
git config --global user.name "Your Name"
```

### Set Email

```bash
git config --global user.email "your-email@example.com"
```

### Verify Configuration

```bash
git config --global --list
```

These settings identify the commit author. They do not authenticate the user to GitHub.

## 10. Creating a Git Repository

A Git repository stores project files, commit history, and repository information.

### Step 1: Create a Directory

```bash
mkdir my-project
```

### Step 2: Enter the Directory

```bash
cd my-project
```

### Step 3: Initialize Git

```bash
git init
```

This initializes a new Git repository in the current directory.

Git creates a hidden `.git` directory to store repository metadata.

## 11. Checking Repository Status

The `git status` command displays the current state of the working directory and staging area.

```bash
git status
```

It identifies:

- Untracked files.
- Modified files.
- Staged changes.
- Whether the working tree is clean.

## 12. Tracking Files with Git

The `git add` command stages files for the next commit.

### Add a Specific File

```bash
git add main.py
```

### Add All Changes

```bash
git add .
```

### Add Multiple Files

```bash
git add file1.py file2.py
```

### Add All Python Files

```bash
git add *.py
```

Changes made after staging must be staged again.

## 13. Creating a Git Commit

A commit records the staged changes in the local repository.

```bash
git add main.py
git commit -m "Add main program"
```

A commit contains:

- Unique commit hash.
- Author information.
- Date and timestamp.
- Commit message.
- Project snapshot information.

### Good Commit Messages

Examples:

```text
Add input validation
Fix division by zero error
Update project documentation
```

Commit messages should be short, meaningful, and descriptive.

## 14. Viewing Commit History

### Display Complete History

```bash
git log
```

Displays commit hash, author, date, and commit message.

### Display Compact History

```bash
git log --oneline
```

Displays each commit in a single line.

### Display Commit Details

```bash
git show
```

Displays information about a commit, including its changes.

## 15. Comparing Changes with Git

The `git diff` command identifies differences between file versions.

### Unstaged Changes

```bash
git diff
```

Displays changes that have not been staged.

### Staged Changes

```bash
git diff --staged
```

Displays changes that are staged for committing.

### Changes Compared with HEAD

```bash
git diff HEAD
```

Displays changes in tracked files compared with the current commit, including staged and unstaged changes.

## 16. Inspecting Tracked Files

The `git ls-files` command lists files known to Git in the index.

```bash
git ls-files
```

It displays tracked files and does not normally show untracked files.

## 17. Ignoring Files with .gitignore

The `.gitignore` file specifies files and directories that Git should ignore when tracking untracked content.

Example `.gitignore`:

```text
__pycache__/
*.pyc
.env
*.log
data/
```

Common uses:

- Ignoring temporary files.
- Ignoring cache directories.
- Excluding local environment configurations.
- Excluding generated files and unnecessary datasets.

**Important:** Adding a file to `.gitignore` does not remove it from Git history if it has already been committed.

## 18. Renaming and Deleting Files

### Rename or Move a File

```bash
git mv old.py new.py
```

This renames a tracked file and stages the rename operation.

### Remove a Tracked File

```bash
git rm old.py
```

This removes the file from the working directory and stages its deletion.

## 19. Unstaging Changes

If a file is added accidentally, it can be removed from the staging area without deleting its working-directory changes.

```bash
git restore --staged main.py
```

The file is removed from staging, but its modifications are preserved.

## 20. Discarding Uncommitted Changes

To discard unstaged modifications in a tracked file:

```bash
git restore main.py
```

This restores the file from the index and removes its unstaged modifications.

**Warning:** This operation can permanently discard uncommitted work. Check changes with `git diff` before executing it.

## 21. Reverting a Commit Safely

The `git revert` command creates a new commit that reverses the changes introduced by an earlier commit.

First, check commit history:

```bash
git log --oneline
```

Then execute:

```bash
git revert COMMIT_ID
```

Replace `COMMIT_ID` with the actual commit hash.

Unlike reset, revert preserves the existing commit history and records the reversal as a new commit.

## 22. GitHub Introduction

GitHub is an online platform used to host Git repositories and collaborate on software projects.

### Major Features

- Hosting and sharing source code.
- Maintaining project history.
- Collaborating with developers.
- Reviewing code through pull requests.
- Tracking bugs using Issues.
- Organizing tasks using Projects.

## 23. Creating a GitHub Repository

Follow these steps:

1. Visit https://github.com.
2. Sign in to your account.
3. Click the New repository option.
4. Enter a repository name.
5. Select Public or Private.
6. Optionally add a README and `.gitignore`.
7. Click Create repository.

### Public vs Private Repository

| Public | Private |
|---|---|
| Anyone can view it | Access is restricted |
| Useful for open-source projects | Useful for private projects |
| Publicly accessible | Requires permission |

## 24. Understanding README.md

A README file introduces a project and explains its purpose and usage.

Example:

```markdown
# Calculator

A simple Python calculator.

## Features
- Addition
- Subtraction
- Multiplication

## Run
python main.py
```

A good README generally contains:

- Project introduction.
- Features.
- Installation instructions.
- Usage instructions.
- Contributors.
- License information.

## 25. Connecting a Local Repository to GitHub

A remote repository connects a local Git repository to a hosted repository.

### Add a Remote

```bash
git remote add origin REPOSITORY_URL
```

Here:

- `git remote add` adds a remote connection.
- `origin` is the conventional remote name.
- `REPOSITORY_URL` is the GitHub repository URL.

### Check Remote Connections

```bash
git remote -v
```

Displays configured fetch and push URLs.

## 26. Pushing Code to GitHub

The `git push` command uploads local commits to a remote repository.

### Rename Current Branch

```bash
git branch -M main
```

### Push Code

```bash
git push -u origin main
```

The `-u` option sets the upstream tracking relationship.

## 27. Cloning a GitHub Repository

Cloning creates a local copy of a remote repository, including its history.

```bash
git clone REPOSITORY_URL
```

Cloning:

- Downloads repository files.
- Downloads commit history.
- Creates a local Git repository.
- Configures the original repository as `origin`.

## 28. Fetching and Pulling Changes

### Git Fetch

```bash
git fetch origin
```

Downloads remote updates without integrating them into the current branch.

### Git Pull

```bash
git pull
```

Fetches remote updates and integrates them into the current branch.

### Difference

| Git Fetch | Git Pull |
|---|---|
| Downloads updates | Downloads and integrates updates |
| Does not change the current branch's committed history | May update current branch history |
| Allows inspection before integration | Integrates automatically according to configuration |

## 29. Branching in Git

A branch is an independent line of development.

Branches allow developers to work on new features without directly modifying the main branch.

### List Branches

```bash
git branch
```

### Create a Branch

```bash
git branch feature-login
```

### Switch Branch

```bash
git switch feature-login
```

### Switch Back to Main

```bash
git switch main
```

### Create and Switch to a New Branch

```bash
git switch -c feature-login
```

The `-c` option creates a branch and switches to it.

## 30. Merging Branches

Merging combines changes from one branch into another.

Example:

```bash
git switch main
git merge feature-login
```

Steps:

1. Switch to the target branch.
2. Execute the merge command.
3. Resolve conflicts if required.
4. Test the merged result.

## 31. Understanding Merge Conflicts

A merge conflict occurs when Git cannot automatically combine competing changes.

For example, two developers modify the same line:

Developer A:

```python
result = 10
```

Developer B:

```python
result = 20
```

Git may display conflict markers:

```text
<<<<<<< HEAD
result = 10
=======
result = 20
>>>>>>> feature-login
```

### Resolving Merge Conflicts

1. Open the conflicting file.
2. Decide which changes to keep.
3. Combine changes if required.
4. Remove conflict markers.
5. Save the file.
6. Stage the resolved file.

```bash
git add main.py
git commit -m "Resolve merge conflict"
```

If Git is waiting for completion of a merge, the commit completes that merge.

## 32. Pull Requests

A Pull Request (PR) is a proposal to merge changes from one branch into another on a hosting platform such as GitHub.

### Pull Request Process

1. Create a feature branch.
2. Make changes.
3. Commit the changes.
4. Push the branch to GitHub.
5. Open a Pull Request.
6. Request a review.
7. Address feedback.
8. Merge the approved changes.

A Pull Request is different from the `git pull` command.

## 33. Forking a Repository

A fork is a separate copy of a repository under another account or namespace on a hosting platform.

Forking allows contributors to work independently on projects they do not own.

Changes can be proposed to the original repository through Pull Requests.

## 34. Code Review and Collaboration

Code review helps improve software quality before changes are merged.

### Responsibilities of a Contributor

- Explain changes.
- Respond to feedback.
- Update the branch.
- Verify the final result.

### Responsibilities of a Reviewer

- Check correctness.
- Identify potential bugs.
- Suggest improvements.
- Verify tests and readability.

## 35. Complete Collaborative GitHub Workflow

A typical development workflow is:

1. Create or clone a repository.
2. Create a feature branch.
3. Modify files and test changes.
4. Stage changes.
5. Commit changes.
6. Push the branch.
7. Open a Pull Request.
8. Review and merge changes.

Workflow:

```text
Create Branch
     |
Edit Files
     |
Stage Changes
     |
Commit Changes
     |
Push Branch
     |
Open Pull Request
     |
Review
     |
Merge
```

## 36. Git Tags and Releases

A tag identifies a particular point in repository history, often used to mark software versions.

### List Tags

```bash
git tag
```

### Create an Annotated Tag

```bash
git tag -a v1.0.0 -m "Version 1.0.0"
```

### Display Tag Information

```bash
git show v1.0.0
```

### Push a Tag to GitHub

```bash
git push origin v1.0.0
```

Semantic versioning generally follows:

MAJOR.MINOR.PATCH

GitHub Releases can attach notes and downloadable files to version tags.

## 37. GitHub Issues

GitHub Issues help developers track bugs, features, questions, and project tasks.

Common uses:

- Report software bugs.
- Suggest new features.
- Assign tasks.
- Discuss project requirements.

Example:

**Title:** Calculator crashes for zero division.

**Description:** Handle division by zero and display an appropriate error message.

## 38. GitHub Projects

GitHub Projects provides tools to organize work and monitor project progress.

Example:

| Status | Task |
|---|---|
| Todo | Design calculator interface |
| In Progress | Implement division |
| In Review | Review input validation |
| Done | Write README |

Projects can use board or table views and can be connected to Issues and Pull Requests.

## 39. Fork vs Clone

| Feature | Fork | Clone |
|---|---|---|
| Meaning | Creates a separate hosted repository copy | Creates a local repository copy |
| Location | GitHub | Local computer |
| Purpose | Independent contribution | Local development |
| Typical use | Contribute to another project | Work on a repository locally |

## 40. Merge vs Rebase

Both commands integrate changes from different branches.

### Merge

```bash
git switch main
git merge feature
```

- Combines branch histories.
- May create a merge commit.
- Preserves existing commits.

### Rebase

```bash
git switch feature
git rebase main
```

- Replays commits on a new base.
- Can produce a linear history.
- Creates rewritten commit identities.

**Caution:** Avoid rebasing shared commits unless the team understands the consequences of rewriting history.

## 41. Common Git Errors and Solutions

| Problem | Possible Solution |
|---|---|
| Untracked files | Use `git add` |
| Push rejected | Fetch and integrate remote changes |
| Merge conflict | Resolve conflicting files |
| Wrong branch | Check using `git branch` |
| Nothing to commit | Check `git status` |
| Authentication failed | Check credentials and permissions |

Diagnostic command:

```bash
git status
```

## 42. Authentication and Security

GitHub supports HTTPS and SSH connections.

Important security practices:

- Use a Personal Access Token when required for HTTPS authentication.
- Use SSH keys securely.
- Never commit passwords or API keys.
- Use `.gitignore` for sensitive local configuration files.
- Review repository visibility and access permissions.
- Enable two-factor authentication where possible.

Never publish private credentials in a public repository.

## 43. Git Best Practices

1. Commit changes frequently.
2. Write meaningful commit messages.
3. Use descriptive branch names.
4. Review changes before committing.
5. Fetch or pull remote updates regularly.
6. Test changes before merging.
7. Keep unnecessary files out of the repository.
8. Maintain a proper README file.

## 44. Practical Mini Project: Version-Controlled Calculator

### Objective

Create a simple calculator program, track its history using Git, and publish it on GitHub.

### Step 1: Initialize Repository

```bash
mkdir calculator
cd calculator
git init
```

Create `main.py`:

```python
print("Calculator")

a = 10
b = 5

print("Sum:", a + b)
```

### Step 2: Record the First Version

```bash
git status
git add main.py
git status
git commit -m "Add initial calculator"
git log --oneline
```

### Step 3: Publish on GitHub

Create an empty GitHub repository named `calculator`.

Then execute:

```bash
git branch -M main
git remote add origin REPOSITORY_URL
git push -u origin main
```

Replace `REPOSITORY_URL` with the actual repository URL.

### Step 4: Implement a New Feature Branch

```bash
git switch -c feature-subtraction
```

Add subtraction functionality to `main.py`:

```python
print("Difference:", a - b)
```

Stage, commit, and push:

```bash
git add main.py
git commit -m "Add subtraction feature"
git push -u origin feature-subtraction
```

### Step 5: Create a Pull Request

1. Open your GitHub repository.
2. Select the Pull Requests section.
3. Click New Pull Request.
4. Select `main` as the base branch.
5. Select `feature-subtraction` as the compare branch.
6. Review the changes.
7. Create and merge the Pull Request.

### Step 6: Update Local Main Branch

```bash
git switch main
git pull origin main
```

The local main branch now receives the merged changes.

## 45. Conclusion

Git is an essential version control system used in modern software development. It helps developers track changes, maintain project history, create branches, resolve conflicts, and collaborate effectively.

GitHub extends these capabilities by providing online repository hosting, Pull Requests, Issues, Projects, and code review features.

Learning Git and GitHub is an important skill for students and software developers because it supports organized development, teamwork, and project management.