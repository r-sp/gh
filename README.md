# GitHub CLI quickstart

Set up [Git](https://git-scm.com/downloads/)

```sh
git config --global user.name "name"
git config --global user.email "id+username@users.noreply.github.com"
git config --list
```

Generate SSH keys

```sh
ssh-keygen -t ed25519 -C "id+username@users.noreply.github.com"
```

Adding your SSH key to ssh-agent

```sh
# Windows
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent

# Linux/macOS
eval "$(ssh-agent -s)"
```

Confirm your SSH key

```sh
ssh-add ~/.ssh/id_ed25519
```

Install [GitHub CLI](https://cli.github.com/) and login into your account

```sh
gh auth login
```

Make sure you choose SSH connection, then click `~/.ssh/id_ed25519.pub` to [Add your SSH keys into your account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

## Commands

```sh
# Git SSH
git clone git@github.com:r-sp/gh.git

# GitHub CLI
gh repo clone r-sp/gh
```

## Summary

**Git**

- A powerful, open-source version control system.
- Tracks changes in your code over time, allowing you to revert to previous versions, collaborate with others, and manage branches.
- Works with any Git repository, regardless of where it's hosted (GitHub, GitLab, Bitbucket, etc.). Great for core version control functionality like version tracking, branching, merging, and committing changes.

**GitHub CLI**

- A command-line tool specifically designed for interacting with GitHub.
- Provides a way to manage GitHub repositories, issues, pull requests, releases, and more directly from your terminal.
- Ideal for those who primarily use GitHub and prefer a command-line workflow. Offers functionalities like creating pull requests, managing issues, and cloning repositories directly from GitHub.

**In simpler terms:**

- Think of Git as the engine that powers version control, working behind the scenes with any compatible repository.
- GitHub CLI is like a specific control panel for that engine, designed to interact smoothly with features offered by GitHub.

**Here's when to use which:**

- Use Git for all your version control needs, no matter the hosting platform.
- Use GitHub CLI if you primarily work with GitHub and want a faster, more streamlined way to interact with its features from the command line.
