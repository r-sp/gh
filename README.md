# GitHub with the perkies

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

Make sure you choose SSH connection, then click `~/.ssh/id_ed25519.pub` to upload into your [GitHub SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

Learn more [about authentication to GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github).

## Commands

```sh
# Git SSH
git clone git@github.com:r-sp/gh.git

# GitHub CLI
gh repo clone r-sp/gh
```
