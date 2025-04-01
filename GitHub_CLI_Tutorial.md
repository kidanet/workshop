# GitHub CLI (gh) Comprehensive Tutorial with Practical Examples

## Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Authenticating with GitHub](#authenticating-with-github)
4. [Basic Commands](#basic-commands)
    - [gh auth](#gh-auth)
    - [gh repo](#gh-repo)
    - [gh issue](#gh-issue)
    - [gh pr](#gh-pr)
5. [Advanced Commands](#advanced-commands)
    - [gh gist](#gh-gist)
    - [gh action](#gh-action)
    - [gh secret](#gh-secret)
6. [Scripting with gh](#scripting-with-gh)
7. [Conclusion](#conclusion)

## Introduction
GitHub CLI (gh) is a powerful tool that brings GitHub to your terminal. It allows you to interact with GitHub repositories, issues, pull requests, gists, and more, directly from your command line.

## Installation
To install GitHub CLI, follow the instructions for your operating system:

### macOS
```sh
brew install gh
```

### Windows
```sh
winget install --id GitHub.cli
```

### Linux
```sh
sudo apt install gh
```

## Authenticating with GitHub
Before you can use `gh`, you need to authenticate with GitHub. Run the following command and follow the prompts:

```sh
gh auth login
```

## Basic Commands

### gh auth
The `gh auth` commands are used to manage authentication.

- **Login:**
    ```sh
    gh auth login
    ```

- **Logout:**
    ```sh
    gh auth logout
    ```

- **Check Auth Status:**
    ```sh
    gh auth status
    ```

### gh repo
The `gh repo` commands allow you to work with GitHub repositories.

- **Clone a Repository:**
    ```sh
    gh repo clone <owner>/<repo>
    ```

- **Create a New Repository:**
    ```sh
    gh repo create my-new-repo --public
    ```

- **Fork a Repository:**
    ```sh
    gh repo fork <owner>/<repo>
    ```

### gh issue
The `gh issue` commands help you manage GitHub issues.

- **Create an Issue:**
    ```sh
    gh issue create --title "Bug Report" --body "There is a bug in the code."
    ```

- **List Issues:**
    ```sh
    gh issue list
    ```

- **View an Issue:**
    ```sh
    gh issue view <issue-number>
    ```

### gh pr
The `gh pr` commands allow you to work with pull requests.

- **Create a Pull Request:**
    ```sh
    gh pr create --title "New Feature" --body "This PR adds a new feature."
    ```

- **List Pull Requests:**
    ```sh
    gh pr list
    ```

- **Merge a Pull Request:**
    ```sh
    gh pr merge <pr-number>
    ```

## Advanced Commands

### gh gist
The `gh gist` commands are used to manage GitHub gists.

- **Create a Gist:**
    ```sh
    gh gist create myfile.txt --public
    ```

- **List Gists:**
    ```sh
    gh gist list
    ```

- **View a Gist:**
    ```sh
    gh gist view <gist-id>
    ```

### gh action
The `gh action` commands help you manage GitHub Actions workflows.

- **List Workflows:**
    ```sh
    gh workflow list
    ```

- **View Workflow Logs:**
    ```sh
    gh run view <run-id> --log
    ```

- **Trigger a Workflow:**
    ```sh
    gh workflow run <workflow-id>
    ```

### gh secret
The `gh secret` commands allow you to manage repository secrets.

- **List Secrets:**
    ```sh
    gh secret list
    ```

- **Set a Secret:**
    ```sh
    gh secret set MY_SECRET --body "super_secret_value"
    ```

- **Remove a Secret:**
    ```sh
    gh secret remove MY_SECRET
    ```

## Scripting with gh
You can use `gh` in scripts to automate your workflows. Here's an example of a script that creates a new repository, clones it, and opens it in VS Code:

```sh
#!/bin/bash

# Create a new repository
gh repo create my-scripted-repo --public

# Clone the repository
gh repo clone my-scripted-repo

# Change directory to the repository
cd my-scripted-repo

# Open the repository in VS Code
code .
```

## Conclusion
GitHub CLI is a versatile tool that can greatly streamline your GitHub workflows. Whether you're managing repositories, issues, pull requests, or automating tasks, `gh` has you covered. Happy coding!