# Advanced Git Operations

## 1. When and how would you use Git stash?
When and How to Use Git Stash
You use git stash when you have uncommitted changes on your current branch but need to switch to another branch or perform a different task without committing incomplete work.

**When:**
1. Switching branches quickly.
2. Pulling latest changes that conflict with your work.
3. Realizing you're on the wrong branch for your current changes.

**How:**

1. **git stash:** Saves your modified tracked files and staged changes onto a stack. Your working directory becomes clean.
Work on something else.
2. **git stash pop:** Reapplies the last stashed changes and removes them from the stash list.
3. **git stash apply:** Reapplies changes but keeps them in the stash list.

## 2. Explain the purpose of Git tags and how to create them?

**Purpose:** Git tags are used to mark specific points in a repository's history as important. They are typically used to mark release points (e.g., v1.0, v2.0-beta) or significant milestones. Unlike branches, tags are static snapshots that don't change.

**How to Create Them:**

1. **Lightweight Tag:** A simple pointer to a commit, like a branch that never moves.
    - git tag <tag-name> (tags current commit)
    - git tag <tag-name> <commit-hash> (tags specific commit)
2. **Annotated Tag:** Recommended; stores more metadata (tagger name, email, date, message) and can be signed for verification.
   - git tag -a <tag-name> -m "Tag message"
   - git tag -a <tag-name> <commit-hash> -m "Tag message"
- To push tags to remote: git push origin --tags

## 3. How do you manage remote repositories in Git?
## When and How to Use Git Stash

You use `git stash` when you have uncommitted changes on your current branch but need to switch to another branch or perform a different task without committing incomplete work.

**When:**
* Switching branches quickly.
* Pulling latest changes that conflict with your work.
* Realizing you're on the wrong branch for your current changes.

**How:**
1.  `git stash`: Saves your modified tracked files and staged changes onto a stack. Your working directory becomes clean.
2.  Work on something else.
3.  `git stash pop`: Reapplies the last stashed changes and removes them from the stash list.
4.  `git stash apply`: Reapplies changes but keeps them in the stash list.

---

## Purpose of Git Tags and How to Create Them

**Purpose:** Git tags are used to mark specific points in a repository's history as important. They are typically used to mark release points (e.g., v1.0, v2.0-beta) or significant milestones. Unlike branches, tags are static snapshots that don't change.

**How to Create Them:**
* **Lightweight Tag:** A simple pointer to a commit, like a branch that never moves.
    * `git tag <tag-name>` (tags current commit)
    * `git tag <tag-name> <commit-hash>` (tags specific commit)
* **Annotated Tag:** Recommended; stores more metadata (tagger name, email, date, message) and can be signed for verification.
    * `git tag -a <tag-name> -m "Tag message"`
    * `git tag -a <tag-name> <commit-hash> -m "Tag message"`
* To push tags to remote: `git push origin --tags`

---

## How to Manage Remote Repositories in Git

Managing remote repositories involves interacting with the versions of your project hosted on a server (like GitHub, GitLab, Bitbucket).

**Common Commands:**
* `git remote -v`: Lists existing remotes (e.g., `origin`).
* `git remote add <name> <url>`: Adds a new remote repository (e.g., `git remote add upstream <url-of-original-repo>`).
* `git fetch <remote-name>`: Downloads objects and refs from another repository without merging.
* `git pull <remote-name> <branch-name>`: Fetches from a remote and immediately merges it into your current branch.
* `git push <remote-name> <branch-name>`: Uploads your local commits to a remote repository.
* `git remote rename <old-name> <new-name>`: Renames a remote.
* `git remote rm <name>`: Removes a remote connection.