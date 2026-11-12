# GitHub

## 1. Introduction

GitHub is a web-based platform used for hosting, managing, and collaborating on software development projects. It uses Git as its version control system.

GitHub allows developers to store their code online, track changes, work with other developers, and manage different versions of a project.

## 2. Objectives

The main objectives of learning GitHub are:

- To understand the purpose of GitHub.
- To learn how to create and manage repositories.
- To upload local projects to GitHub.
- To understand remote repositories.
- To learn cloning, pushing, pulling, and fetching.
- To understand branches and collaboration.

## 3. What is GitHub?

GitHub is a cloud-based platform that provides hosting for Git repositories.

It helps developers:
- Store project files online.
- Track changes in source code.
- Collaborate with other developers.
- Review and discuss code changes.
- Manage project issues and tasks.

**Website:** https://github.com

## 4. Difference Between Git and GitHub

| Git | GitHub |
|---|---|
| Git is a version control system. | GitHub is a web-based hosting platform. |
| It is installed and used locally. | It is accessed through the internet. |
| It tracks changes in files. | It hosts Git repositories online. |
| It can work without an internet connection. | Internet is generally required to access hosted repositories. |
| It is a tool. | It is a platform that uses Git. |

## 5. GitHub Account

To use GitHub:

1. Visit https://github.com.
2. Click on Sign Up.
3. Enter your email address.
4. Create a username and password.
5. Complete the verification process.
6. Sign in to your account.

### Account Security

- Enable two-factor authentication (2FA).
- Never share your password or personal access tokens.
- Never share private SSH keys.
- Keep authentication credentials secure.

## 6. GitHub Repository

A repository is a storage location for a project. It contains project files, folders, documentation, and version history.

A repository can be:

- **Public:** Anyone can view the repository.
- **Private:** Access is restricted to permitted users.

### Steps to Create a Repository

1. Sign in to GitHub.
2. Click the **New repository** option.
3. Enter a repository name.
4. Add an optional description.
5. Select Public or Private.
6. Optionally initialize the repository with a README file.
7. Click **Create repository**.

## 7. README File

A README file provides information about a repository and its contents.

It is generally written in Markdown and is displayed on the repository's main page.

A README file may contain:

- Project title.
- Project description.
- Objectives.
- Folder structure.
- Installation instructions.
- Commands to run the project.
- Author information.

Example:

```markdown
# Technical Writing Assignment

This repository contains documentation prepared
during the Technical Writing course.

## Topics

- LaTeX
- Beamer
- Doxygen
- Google Docs
- Git
- GitHub
```

## 8. Connecting a Local Repository to GitHub

A local repository can be connected to a remote GitHub repository using the `git remote` command.

### Add Remote Repository

```bash
git remote add origin https://github.com/username/repository-name.git
```

Here:
- `origin` is the conventional name of the remote repository.
- The URL represents the GitHub repository address.

### Check Remote Repository

```bash
git remote -v
```

This command displays the remote repository URLs used for fetching and pushing.

## 9. Uploading a Local Project to GitHub

The following commands are used to upload a local Git project to GitHub.

### Step 1: Initialize Git

```bash
git init
```

### Step 2: Check Repository Status

```bash
git status
```

### Step 3: Add Files

```bash
git add .
```

### Step 4: Commit Changes

```bash
git commit -m "Initial commit"
```

### Step 5: Add Remote Repository

```bash
git remote add origin https://github.com/username/repository-name.git
```

### Step 6: Rename the Main Branch

```bash
git branch -M main
```

### Step 7: Push Files to GitHub

```bash
git push -u origin main
```

After successful execution, the local project files are uploaded to the GitHub repository.

## 10. Pushing Changes

The `git push` command uploads local commits to a remote repository.

```bash
git push
```

It is used when new commits need to be uploaded to GitHub.

## 11. Cloning a Repository

Cloning creates a local copy of an existing remote repository.

Command:

```bash
git clone https://github.com/username/repository-name.git
```

Steps:

1. Open the GitHub repository.
2. Click the Code button.
3. Copy the repository URL.
4. Open the terminal.
5. Execute the `git clone` command.

The repository files and version history are downloaded to the local system.

## 12. Fetching Changes

The `git fetch` command downloads new information and commits from a remote repository without automatically merging them into the current local branch.

```bash
git fetch origin
```

It allows users to inspect remote changes before integrating them.

## 13. Pulling Changes

The `git pull` command downloads changes from a remote repository and integrates them into the current local branch.

```bash
git pull origin main
```

It is commonly used to update the local project with the latest changes from GitHub.

### Difference Between Fetch and Pull

| Git Fetch | Git Pull |
|---|---|
| Downloads remote changes. | Downloads and integrates remote changes. |
| Does not automatically merge changes into the current branch. | Usually merges changes into the current branch. |
| Allows inspection before integration. | Updates the current branch directly. |

## 14. Branches in GitHub

A branch is an independent line of development.

Branches allow developers to work on new features or fix bugs without directly changing the main branch.

Useful commands:

```bash
git branch
```

Displays the available local branches.

```bash
git branch feature
```

Creates a new branch named `feature`.

```bash
git switch feature
```

Switches to the `feature` branch.

```bash
git switch -c feature
```

Creates a new branch and switches to it.

## 15. Merging Branches

Merging combines changes from one branch into another branch.

For example:

```bash
git switch main
git merge feature
```

These commands switch to the main branch and merge the changes from the feature branch into it.

## 16. Merge Conflicts

A merge conflict occurs when Git cannot automatically combine changes from different branches.

It may happen when two branches modify the same part of a file.

Steps to resolve a merge conflict:

1. Open the file containing the conflict.
2. Identify the conflicting sections.
3. Decide which changes should be kept.
4. Edit the file and remove conflict markers.
5. Save the file.
6. Stage the resolved file.
7. Commit the changes if required.

Example:

```bash
git add filename
git commit -m "Resolve merge conflict"
```

## 17. Pull Requests

A Pull Request (PR) is a feature used to propose changes from one branch to another branch on GitHub.

It allows team members to review changes before merging them.

Basic steps:

1. Create a new branch.
2. Make the required changes.
3. Commit the changes.
4. Push the branch to GitHub.
5. Open the repository on GitHub.
6. Create a Pull Request.
7. Review the changes.
8. Merge the Pull Request after approval.

## 18. Forking a Repository

Forking creates a copy of another user's repository under your own GitHub account.

It is useful when contributing to projects that you do not own.

A typical workflow is:

1. Open the original repository.
2. Click the Fork option.
3. Create a fork under your account.
4. Clone your fork to your computer.
5. Make changes.
6. Push the changes to your fork.
7. Submit a Pull Request to the original repository.

## 19. Fork vs Clone

| Fork | Clone |
|---|---|
| Creates a copy of a repository on your GitHub account. | Creates a local copy of a repository on your computer. |
| Performed on GitHub. | Performed using Git. |
| Commonly used for contributing to other projects. | Used to work with a repository locally. |

## 20. GitHub Interface

Some important sections of a GitHub repository are:

- **Code:** Displays project files and folders.
- **Issues:** Used to report bugs, suggest improvements, and discuss tasks.
- **Pull Requests:** Used to propose and review code changes.
- **Actions:** Used to automate workflows.
- **Settings:** Used to configure repository options and access permissions.

## 21. GitHub Issues

Issues are used to track bugs, tasks, questions, and feature requests.

They help developers organize project work and communicate about problems.

Examples:
- Report a bug.
- Suggest a new feature.
- Track a documentation task.
- Discuss a project improvement.

## 22. GitHub Projects

GitHub Projects helps organize and manage project work.

It can be used to:
- Create task lists.
- Track project progress.
- Organize issues and pull requests.
- Manage development activities.

## 23. Git Tags and Releases

Tags are used to mark specific points in a repository's history, often for version identification.

Example:

```bash
git tag v1.0
```

To push a tag to GitHub:

```bash
git push origin v1.0
```

A GitHub Release can be created to publish a particular version of a project along with release notes or downloadable files.

## 24. Common GitHub Commands

| Command | Purpose |
|---|---|
| `git remote -v` | Displays remote repository URLs. |
| `git remote add origin URL` | Connects a remote repository. |
| `git push -u origin main` | Pushes the main branch and sets its upstream. |
| `git push` | Uploads local commits. |
| `git clone URL` | Downloads a repository locally. |
| `git fetch origin` | Downloads remote information. |
| `git pull origin main` | Fetches and integrates changes from main. |
| `git branch` | Lists local branches. |
| `git switch branch-name` | Switches branches. |
| `git merge branch-name` | Merges another branch. |

## 25. Best Practices

- Write meaningful commit messages.
- Keep the README file updated.
- Use branches for new features.
- Review changes before merging.
- Do not upload passwords, tokens, or private keys.
- Keep repositories organized.
- Pull the latest changes before starting collaborative work.
- Use issues to track tasks and bugs.

## 26. Advantages of GitHub

- Provides online storage for Git repositories.
- Supports collaboration among developers.
- Maintains project history.
- Makes code review easier.
- Supports open-source development.
- Provides issue and project management features.
- Helps developers showcase their work.

## 27. Applications of GitHub

GitHub is widely used for:

- Software development.
- Team-based projects.
- Open-source contributions.
- Documentation hosting.
- Academic assignments.
- Portfolio development.
- Project collaboration.

## 28. Conclusion

GitHub is an important platform for modern software development. It provides an effective way to host Git repositories, manage project versions, collaborate with other developers, and maintain software documentation. Learning GitHub along with Git helps students and developers manage projects efficiently and work collaboratively.