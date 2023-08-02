# GitHub Git Cheatsheet

Git is the free and open source distributed version control system that's responsible for everything GitHub related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.

With platform specific installers for Git, GitHub also provides the ease of staying up-to-date with the latest releases of the command line tool while providing a graphical user interface for day-to-day interaction, review, and repository synchronization.

- [GitHub for Windows](https://windows.github.com).
- [GitHub for Mac](https://mac.github.com).
- [Git for All Platforms](http://git-scm.com).

## Setup

Configuring user information used across all local repositories.

```bash
git config --global user.name "[firstname lastname]"
```

Set a name that is identifiable for credit when review version history.

```bash
git config --global user.name "[valid-email]"
```

Set an email address that will be associated with each history marker.

```bash
git config --global color.ui auto
```

Set automatic command line coloring for Git for easy reviewing.

## Setup & Init

Configuring user information, initializing and cloning repositories.

```bash
git init
```

Initialize an existing directory as a Git repository.

```bash
git clone [url]
```

Retrieve an entire repository from a hosted location via URL

## Stage & Snapshot

Working with snapshots and the Git staging area.

```bash
git status
```

Show modified files in working directory, staged for your next commit.

```bash
git add [file]
```

Add a file as it looks now to your next commit (stage).

```bash
git reset [file]
```

Unstage a file while retaining the changes in working directory.

```bash
git diff
```

Diff of what is changed but not staged.

```bash
git diff --staged
```

Diff of what is staged but not yet committed.

```bash
git commit -m "[descriptive message]"
```

Commit your staged content as a new commit snapshot.

## Branch & Merge

Isolating work in branches, changing context, and integrating changes.

```bash
git branch
```

List your branches, a \* will appear next to the currently active branch.

```bash
git branch [branch-name]
```

Create a new branch at the current commit.

```bash
git checkout
```

Switch to another branch and check it out into your working directory.

```bash
git merge [branch]
```

Merge the specified branch's history into the current one.

```bash
git log
```

Show all commits in the current branch's history.
