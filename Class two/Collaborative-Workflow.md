# Collaborative Workflow

**1. Explain the purpose and process of creating a pull request.**

##### Purpose and Process of a Pull Request
A Pull Request (PR) is a mechanism to propose changes to a repository, commonly used in open-source or team-based development.

**Purpose: It allows you to:**

A. Inform maintainers of changes you'd like to merge.
B. Initiate code reviews and discussions.
C. Trigger automated tests.

**Process:**

1. Push your changes to a feature branch on your repository.
2. Go to the hosting service (e.g., GitHub) and create a new PR from your feature branch to the target branch (e.g., main) of the original repository.
3. Reviewers then examine your code, comment, and suggest changes before the maintainer merges it.

**2. What is the difference between forking and cloning a repository?**

##### Forking vs. Cloning a Repository

- **Cloning:** Creates a local copy of an existing repository onto your machine. You get the entire history and can work on it directly. You generally clone a repository you already have write access to (or will contribute to via branches and direct pushes).
    ` git clone <repository-url>`
- **Forking:** Creates a personal copy of a repository on a remote server (e.g., GitHub) under your account. It's used when you don't have write access to the original project but want to contribute. You make changes in your fork, then propose them back via a Pull Request.

**3. How would you use Git to collaborate with other developers on the same project?**

##### How to Use Git for Collaboration

**To collaborate with Git:**

1. Clone the shared repository to your local machine.
2. Create a new branch for your work (git checkout -b my-feature).
3. Make changes and commit them regularly to your local branch.
4. Pull latest changes from the shared remote branch (git pull origin main) to keep your local main up-to-date and resolve any conflicts locally.
5. Push your feature branch to the remote (git push origin my-feature).
6. Create a Pull Request on the hosting platform (e.g., GitHub) to propose merging your feature into the main project.
7. Review, address feedback, and merge.