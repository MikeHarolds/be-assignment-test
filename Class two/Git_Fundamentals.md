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



**3. How does Git track changes in your codebase?**

