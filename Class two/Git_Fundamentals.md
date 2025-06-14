# Git Fundamentals

**1. Explain the difference between Git and other version control systems.**

Git fundamentally differs from other common version control systems (like SVN) in its distributed nature versus their centralized approach.

- Centralized VCS (e.g., SVN): Relies on a single central server for the entire project history. Developers "check out" files, make changes, and then "commit" them back to the central server. If the central server is down, no one can commit or get updates.
- Git (Distributed VCS): Every developer has a complete copy of the entire repository, including its full history, on their local machine. You commit changes locally, then "push" them to a remote server (like GitHub) to share.

**This means:**

- Offline work: Git allows full functionality offline.
- Redundancy: Every clone acts as a full backup.
- Faster operations: Most operations are local.
- Flexible workflows: Easier branching and merging.

**2. What is the purpose of a repository in version control?**
The purpose of a repository in version control (like Git) is to serve as the central storage for all your project's files and their complete history.

**It's where:**

- Every change, modification, and deletion is recorded.
- Different versions of the code (commits) are stored.
- Branches are managed, allowing parallel development.
- Collaborators can push and pull updates, ensuring everyone works on the latest code and changes are tracked.
- Essentially, it's the organized, historical database for your project, enabling tracking, collaboration, and easy rollback to previous states.


**3. How does Git track changes in your codebase?**
Git tracks changes by taking snapshots of your codebase at each commit, rather than storing differences (deltas) directly.

**Here's how:**
- **Content-Addressed Storage:** Every file's content, directory structure, and commit metadata is hashed (using SHA-1) into a unique ID.
- **Objects:** These hashes lead to "objects" stored in a hidden .git directory. There are "blob" objects for file content, "tree" objects for directory structures, and "commit" objects that link to a specific tree and its parent commit(s).

- **Efficiency:** If a file hasn't changed, Git simply reuses its existing object, making commits very lightweight. Diffs are calculated on-the-fly when needed.
