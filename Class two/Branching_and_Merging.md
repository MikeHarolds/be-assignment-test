# Branching and Merging

**1. What is the purpose of branching in Git?**

### Purpose of Branching in Git

Branching in Git allows developers to create independent lines of development within a single repository. This lets teams work on new features, bug fixes, or experiments concurrently without affecting the stable main codebase until changes are ready. It isolates work, preventing instability.


**2. What is the difference between merging and rebasing? When would you use each?**

### Merging vs. Rebasing
- **Merging:** Combines separate lines of development by creating a new merge commit that has two parent commits. It preserves history exactly as it happened. 
- **Use when:** You want to maintain a clear, chronological history of all development, including parallel work. (e.g., integrating feature branches into main).
- **Rebasing:** Moves or reapplies a series of commits from one branch onto another base commit, creating a linear history. It rewrites commit history.

    -  **Use when:** You want a clean, linear project history, avoiding extra merge commits, typically for local feature branches before integrating into main. (e.g., tidying up your local feature branch before a final merge).

**3. How do merge conflicts occur, and what are the general steps to resolve them?**

### Merge Conflicts
Merge conflicts occur when Git cannot automatically reconcile differing changes made to the same lines in the same file by different branches being merged or rebased.

**General Steps to Resolve:**

- **Identify:** Git will indicate which files have conflicts.
- **Open File:** Open the conflicted file; Git adds markers (<<<<<<<, =======, >>>>>>>) showing the conflicting sections.
- **Edit:** Manually edit the file to choose which changes to keep, or combine them as desired. Remove the Git markers.
- **Add:** Stage the resolved file(s) using git add <filename>.
- **Commit:** Complete the merge/rebase by creating a new commit (git commit -m "Resolved merge conflict").