# Git-Cheatsheet

A comprehensive Git cheatsheet for beginners, covering essential commands for configuration, branching, merging, cloning, pull requests, pushing, and more. Ideal for starting development, contributing to open source, and collaborating with other developers.

## Initial Setup

> 1. **Initialize Git (if not already initialized)**
>
>    ```sh
>    git init
>    ```
>
> 2. **Add your files to the repository**
>
>    ```sh
>    git add .
>    ```
>
> 3. **Commit your changes**
>
>    ```sh
>    git commit -m "Initial commit"
>    ```
>
> 4. **Add the remote repository URL**
>
>    ```sh
>    git remote add origin [repository-link]
>    ```
>
> 5. **Push your changes to the remote repository**
>    ```sh
>    git push -u origin [branch]
>    ```

## Check all commits

```sh
git log
git log --oneline
```

## Create a new branch

```sh
git checkout -b [branch]
```

## Link the new branch to remote-origin <branch>

```sh
git branch --set-upstream-to=origin/[branch] [branch]
```

## Fetch all branches and updates from the remote repository

```sh
git fetch --all
```

## Check all remote branches

```sh
git ls-remote --heads origin
```

## Stash changes (temporarily save your changes)

```sh
git stash
```

## Stash changes with a custom message

```sh
git stash save "stash message"
```

## Create a new branch from a stash

```sh
git stash branch [branch] stash@{n}
```

## List all stashes

```sh
git stash list
```

## Apply stash changes without removing them from the stash list

```sh
git stash apply
```

## Remove a stash from the list

```sh
git stash drop
```

## Apply and remove the latest stash from the list

```sh
git stash pop
```

## Show the changes recorded in a stash

```sh
git stash show
```

## Stash only the staged changes with a custom message

```sh
git stash push --staged -m "Stash only staged changes"
```

## Rebase commands

```sh
git pull --rebase <upstream> <branch>
```

## Abort a merge

```sh
git merge --abort
```

## Merge a branch into the current branch

```sh
git merge [branch-to-merge]
```

## Revert a commit by its hash

```sh
git revert [commit-hash]
git revert --abort
```

## Undo a revert by cherry-picking the original commit

```sh
git cherry-pick [commit_hash]
```

## Switch to another branch before deleting a branch

```sh
git checkout [branch]
```

## Delete a local branch

```sh
git branch -d [branch]
```

## Force delete a local branch

```sh
git branch -D [branch]
```

## Delete a remote branch on GitHub

```sh
git push origin --delete [branch]
```

## Reset to the last commit and get changes in the staging area

```sh
git reset --soft HEAD^1
```

## Install a package as a dev dependency

```sh
npm install [package-name] --save-dev
```

## Update a package

```sh
npm update [-g] [<pkg>...]
```

## Show all commits with a graph

```sh
git log --graph --oneline --branches
```

## Important Descriptions

### What is a Branch?

A branch in Git is a lightweight movable pointer to a commit. It allows you to work on different versions of a project simultaneously. To create a new branch:

```sh
git checkout -b [branch]
```

### What is a Merge?

Merging in Git means combining the changes from one branch into another. This is typically done to integrate features or fixes. To merge a branch into the current branch:

```sh
git merge [branch-to-merge]
```

### What is a Stash?

Stashing in Git allows you to temporarily save changes that are not ready to be committed. This is useful when you need to switch branches but want to save your work. To stash changes:

```sh
git stash
```
