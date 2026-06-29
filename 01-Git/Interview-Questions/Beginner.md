# Beginner Git Interview Questions

> Level: Beginner
>

---

# Q1. What is Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git is a **Distributed Version Control System (DVCS)** used to track changes in source code, collaborate with multiple developers, and maintain complete project history efficiently.

---

## 📖 Detailed Explanation

Git is a Version Control System that records every change made to your project files. Every change is stored as a **Commit**, allowing developers to track history, restore previous versions, and collaborate safely without overwriting each other's work.

Unlike traditional systems, Git is distributed, meaning every developer has a complete copy of the repository on their local machine.

---

## 🌍 Real World Example

Imagine five Cloud Engineers working on the same Azure Infrastructure Project. Instead of sharing ZIP files through email, each engineer works on a separate Git branch. Once their work is complete, all branches are merged into the main branch.

---

## 💡 Key Points

- Distributed Version Control System
- Tracks every file change
- Maintains complete history
- Supports collaboration
- Industry standard for Software, Cloud & DevOps

---

## 🎤 Follow-up Interview Questions

- What is Version Control?
- Why is Git called Distributed?
- Difference between Git and GitHub?
- Can Git work without GitHub?

</details>

---

# Q2. What is Version Control?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Version Control is a system that tracks changes made to files over time, allowing developers to restore previous versions and collaborate efficiently.

---

## 📖 Detailed Explanation

Version Control records every modification made to a project. It keeps a history of changes so developers can identify who made a change, when it was made, and revert to an earlier version if required.

Git is the most widely used Version Control System today.

---

## 🌍 Real World Example

Suppose a Terraform configuration stops working after today's update. Using Version Control, you can easily compare today's code with yesterday's version and restore the previous working state.

---

## 💡 Key Points

- Tracks file changes
- Stores project history
- Supports collaboration
- Enables rollback
- Prevents data loss

---

## 🎤 Follow-up Interview Questions

- Why do we need Version Control?
- What problems does Version Control solve?
- Types of Version Control Systems?

</details>

---

# Q3. What is the difference between Git and GitHub?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git is a Version Control System, whereas GitHub is a cloud platform that hosts Git repositories and enables team collaboration.

---

## 📖 Detailed Explanation

Git is software installed on your computer that manages version history locally. GitHub is an online platform where Git repositories are stored, shared, and managed for collaboration.

Git can work without GitHub, but GitHub cannot manage source code without Git.

---

## 🌍 Real World Example

Think of Git as Microsoft Word installed on your laptop, while GitHub is OneDrive where you upload and share your documents.

---

## 💡 Key Points

- Git = Version Control Tool
- GitHub = Repository Hosting Platform
- Git works offline
- GitHub enables collaboration

---

## 🎤 Follow-up Interview Questions

- Can Git work without GitHub?
- Name other Git hosting platforms.
- Difference between GitHub and GitLab?

</details>

---

# Q4. What is a Repository?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Repository is a storage location that contains project files, commit history, branches, and Git metadata.

---

## 📖 Detailed Explanation

A Git Repository stores everything related to a project, including files, commits, branches, tags, and complete version history. It can exist locally or remotely on platforms like GitHub.

---

## 🌍 Real World Example

An Azure Infrastructure project containing Terraform files, documentation, and scripts is stored inside a Git Repository.

---

## 💡 Key Points

- Stores project files
- Stores Git history
- Supports collaboration
- Can be Local or Remote

---

## 🎤 Follow-up Interview Questions

- Local Repository vs Remote Repository?
- How do you create a Repository?

</details>

---

# Q5. What is the Working Directory?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

The Working Directory is the area where developers create, modify, or delete project files before staging them.

---

## 📖 Detailed Explanation

Every change you make to project files first appears in the Working Directory. These changes are not tracked by Git until they are added to the Staging Area.

---

## 🌍 Real World Example

When editing a Terraform file or README.md, you are working inside the Working Directory.

---

## 💡 Key Points

- First stage of development
- Contains modified files
- Changes are not committed yet

---

## 🎤 Follow-up Interview Questions

- Difference between Working Directory and Staging Area?
- How do you check modified files?

</details>

---

# Q6. What is the Staging Area?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

The Staging Area is a temporary area where selected changes are prepared before creating a commit.

---

## 📖 Detailed Explanation

Git allows developers to choose exactly which changes should be included in the next commit. These selected changes are placed into the Staging Area.

---

## 🌍 Real World Example

You modify five files but only want to commit two. You add only those two files to the Staging Area.

---

## 💡 Key Points

- Temporary area
- Controls commit contents
- Improves commit quality

---

## 🎤 Follow-up Interview Questions

- Which command adds files to the Staging Area?
- Can only one file be staged?

</details>

---

# Q7. What is a Commit?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Commit is a snapshot of staged changes saved permanently in the Git repository.

---

## 📖 Detailed Explanation

Each commit represents a milestone in project development. Git assigns every commit a unique hash, making it easy to track, compare, or restore project history.

---

## 🌍 Real World Example

After completing Azure Virtual Network documentation, you commit the changes with a meaningful message.

---

## 💡 Key Points

- Snapshot of changes
- Permanent history
- Unique Commit ID
- Easy rollback

---

## 🎤 Follow-up Interview Questions

- What is a Commit Hash?
- Why are commit messages important?

</details>

---

# Q8. What is a Branch?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Branch is an independent line of development that allows developers to work without affecting the main project.

---

## 📖 Detailed Explanation

Branches enable parallel development. Each developer can implement new features or fix bugs independently before merging the changes into the main branch.

---

## 🌍 Real World Example

One engineer develops Terraform code while another configures Azure Networking. Both work on separate branches.

---

## 💡 Key Points

- Parallel development
- Safe experimentation
- Easy collaboration
- Supports feature development

---

## 🎤 Follow-up Interview Questions

- Why do we create branches?
- What is the default branch?

</details>

---

# Q9. What is Git Merge?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Merge combines changes from one branch into another branch.

---

## 📖 Detailed Explanation

Once feature development is complete, the feature branch is merged into the main branch. Git combines the commit history while preserving development history.

---

## 🌍 Real World Example

The Networking team completes their work on the feature/network branch. After review, it is merged into the main branch.

---

## 💡 Key Points

- Combines branches
- Preserves history
- Used after development
- Team collaboration

---

## 🎤 Follow-up Interview Questions

- What is Merge Conflict?
- Difference between Merge and Rebase?

</details>

---

# Q10. What is GitHub?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

GitHub is a cloud-based platform that hosts Git repositories and enables collaboration, version control, code review, and project management.

---

## 📖 Detailed Explanation

GitHub allows developers to store repositories online, collaborate using Pull Requests, manage issues, review code, and integrate CI/CD pipelines.

Although Git manages version control, GitHub provides collaboration and repository hosting services.

---

## 🌍 Real World Example

A company stores all Azure, Terraform, Docker, Kubernetes, and DevOps projects on GitHub so every engineer can access and contribute from anywhere.

---

## 💡 Key Points

- Git Repository Hosting
- Team Collaboration
- Pull Requests
- Code Review
- CI/CD Integration

---

## 🎤 Follow-up Interview Questions

- Difference between Git and GitHub?
- What is a Pull Request?
- Can GitHub host private repositories?
- What are GitHub Actions?

</details>

# Beginner Git Interview Questions

> Level: Beginner
>
> Part 2 (Q11 - Q20)

---

# Q11. What is Git Clone?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Clone is used to create a complete copy of an existing remote repository on your local machine.

---

## 📖 Detailed Explanation

The `git clone` command downloads the entire repository, including all branches, commits, tags, and project history. It automatically configures the remote repository as **origin**, allowing you to pull and push changes later.

---

## 🌍 Real World Example

You join a new company and need to work on an existing Azure Infrastructure project. Instead of creating everything from scratch, you clone the repository from GitHub.

---

## 💡 Key Points

- Copies complete repository
- Downloads full commit history
- Automatically adds remote origin
- Used when joining an existing project

---

## 🎤 Follow-up Interview Questions

- Difference between Clone and Download ZIP?
- What happens after cloning a repository?
- Can you clone a private repository?

</details>

---

# Q12. What is Git Push?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Push uploads your local commits to a remote repository such as GitHub.

---

## 📖 Detailed Explanation

After creating commits locally, they remain only on your computer. The `git push` command transfers these commits to the remote repository, making them available to the rest of the team.

---

## 🌍 Real World Example

After completing Terraform documentation, you push your changes to GitHub so your teammates can review them.

---

## 💡 Key Points

- Uploads commits
- Synchronizes local and remote repositories
- Used after commit
- Enables team collaboration

---

## 🎤 Follow-up Interview Questions

- Why does git push sometimes fail?
- What is upstream?
- What does `git push -u origin main` do?

</details>

---

# Q13. What is Git Pull?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Pull downloads the latest changes from a remote repository and automatically merges them into your current branch.

---

## 📖 Detailed Explanation

The `git pull` command is a combination of **git fetch** and **git merge**. It retrieves the latest commits from the remote repository and merges them into your local branch.

---

## 🌍 Real World Example

Before starting your work every morning, you pull the latest changes made by your teammates.

---

## 💡 Key Points

- Downloads latest changes
- Automatically merges
- Keeps repository up to date
- Combination of Fetch + Merge

---

## 🎤 Follow-up Interview Questions

- Difference between Pull and Fetch?
- Can Pull create Merge Conflicts?
- Should you pull before starting work?

</details>

---

# Q14. What is Git Fetch?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Fetch downloads the latest changes from the remote repository without merging them into your current branch.

---

## 📖 Detailed Explanation

Git Fetch updates your local copy of the remote repository. It allows you to review incoming changes before deciding whether to merge them.

---

## 🌍 Real World Example

Before merging production changes, you fetch the latest updates to review them first.

---

## 💡 Key Points

- Downloads latest changes
- Does not merge automatically
- Safe operation
- Useful before reviewing changes

---

## 🎤 Follow-up Interview Questions

- Difference between Fetch and Pull?
- When should Fetch be preferred?

</details>

---

# Q15. What is the difference between Git Pull and Git Fetch?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Fetch only downloads changes, whereas Git Pull downloads and immediately merges those changes into the current branch.

---

## 📖 Detailed Explanation

Fetch allows developers to inspect changes before merging them. Pull combines fetching and merging into one command, making it faster but sometimes causing unexpected merge conflicts.

---

## 🌍 Real World Example

A Production Engineer uses Fetch to review incoming code before merging it, while a developer working alone may directly use Pull.

---

## 💡 Key Points

- Fetch = Download only
- Pull = Download + Merge
- Fetch is safer
- Pull is faster

---

## 🎤 Follow-up Interview Questions

- Which command is safer in Production?
- Can Pull create conflicts?

</details>

---

# Q16. What is Git Remote?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Git Remote is a reference to a remote repository that allows you to push, pull, and synchronize your local repository with a server.

---

## 📖 Detailed Explanation

Remote repositories are usually hosted on GitHub, GitLab, or Bitbucket. Git stores the remote URL using a name such as **origin**.

---

## 🌍 Real World Example

Your local Azure project connects to a GitHub repository using the remote name **origin**.

---

## 💡 Key Points

- Connects local and remote repositories
- Stores repository URL
- Used for Push and Pull
- Supports multiple remotes

---

## 🎤 Follow-up Interview Questions

- What is origin?
- Can a repository have multiple remotes?

</details>

---

# Q17. What is Origin in Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Origin is the default name given to the remote repository when a repository is cloned.

---

## 📖 Detailed Explanation

Origin is simply an alias for the remote repository URL. Instead of typing the complete URL every time, Git uses the name **origin**.

---

## 🌍 Real World Example

When you clone an Azure project from GitHub, Git automatically creates a remote called **origin**.

---

## 💡 Key Points

- Default remote name
- Represents GitHub repository
- Can be renamed
- Simplifies Git commands

---

## 🎤 Follow-up Interview Questions

- Can origin be changed?
- How do you view remote repositories?

</details>

---

# Q18. What is HEAD in Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

HEAD is a pointer that indicates the currently checked-out branch or commit.

---

## 📖 Detailed Explanation

HEAD always points to your current working location in the repository. Whenever you switch branches or create commits, HEAD moves accordingly.

---

## 🌍 Real World Example

If you are working on the **feature/network** branch, HEAD points to the latest commit of that branch.

---

## 💡 Key Points

- Current position indicator
- Moves with commits
- Changes when switching branches
- Important Git reference

---

## 🎤 Follow-up Interview Questions

- What is Detached HEAD?
- How does HEAD move?

</details>

---

# Q19. What is Git Status?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Status displays the current state of your working directory and staging area.

---

## 📖 Detailed Explanation

The `git status` command shows modified files, staged files, untracked files, and the current branch. It is one of the most frequently used Git commands.

---

## 🌍 Real World Example

Before committing changes to your Azure project, you check `git status` to verify which files will be included.

---

## 💡 Key Points

- Shows repository status
- Displays staged files
- Displays modified files
- Displays untracked files

---

## 🎤 Follow-up Interview Questions

- Why should you run git status frequently?
- What are untracked files?

</details>

---

# Q20. What is Git Log?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Log displays the complete commit history of a repository.

---

## 📖 Detailed Explanation

The `git log` command shows commit IDs, author information, commit dates, and commit messages. It helps developers understand the history of a project and identify when changes were introduced.

---

## 🌍 Real World Example

While investigating a production issue, you use `git log` to identify which commit introduced the recent configuration changes.

---

## 💡 Key Points

- Displays commit history
- Shows commit IDs
- Shows author details
- Helps in troubleshooting
- Useful for project auditing

---

## 🎤 Follow-up Interview Questions

- What is `git log --oneline`?
- How do you view a specific commit?
- How can you filter Git logs?

</details>

---

# Q21. What is Git Diff?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Diff is used to compare changes between files, commits, branches, or the working directory.

---

## 📖 Detailed Explanation

The `git diff` command helps developers identify exactly what has changed before creating a commit. It highlights added, removed, and modified lines, making code reviews and troubleshooting much easier.

---

## 🌍 Real World Example

Before committing changes to a Terraform configuration, you run `git diff` to verify that only the intended modifications are included.

---

## 💡 Key Points

- Compares changes
- Shows added and removed lines
- Useful before committing
- Helps prevent accidental commits

---

## 🎤 Follow-up Interview Questions

- Difference between `git diff` and `git status`?
- Can Git Diff compare two branches?
- How do you compare two commits?

</details>

---

# Q22. What is Git Tag?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Git Tag is a reference that marks a specific commit, usually representing a software release or important milestone.

---

## 📖 Detailed Explanation

Tags are commonly used to identify stable versions such as **v1.0.0**, **v2.0.0**, or production releases. Unlike branches, tags do not move when new commits are created.

---

## 🌍 Real World Example

After successfully deploying an Azure Infrastructure project to Production, the team creates a tag named **v1.0.0**.

---

## 💡 Key Points

- Marks important commits
- Used for software releases
- Permanent reference
- Supports versioning

---

## 🎤 Follow-up Interview Questions

- Difference between Tag and Branch?
- What is an Annotated Tag?
- What is a Lightweight Tag?

</details>

---

# Q23. What is Git Revert?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Revert safely undoes a previous commit by creating a new commit that reverses the selected changes.

---

## 📖 Detailed Explanation

Instead of deleting commit history, Git Revert preserves history while undoing unwanted changes. It is considered the safest way to reverse changes in shared repositories.

---

## 🌍 Real World Example

A faulty firewall configuration is deployed. Instead of deleting history, the team uses **Git Revert** to safely restore the previous working configuration.

---

## 💡 Key Points

- Creates a new commit
- Preserves commit history
- Safe for shared repositories
- Recommended in Production

---

## 🎤 Follow-up Interview Questions

- Difference between Revert and Reset?
- Why is Revert safer?

</details>

---

# Q24. What is Git Reset?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Reset moves the current branch pointer to a previous commit and can remove staged changes, commits, or working directory changes depending on the reset mode.

---

## 📖 Detailed Explanation

Git Reset is mainly used during local development. It can modify commit history, making it a powerful but potentially dangerous command if used incorrectly.

---

## 🌍 Real World Example

You accidentally commit temporary test files. Before pushing them, you use Git Reset to remove the unwanted commit.

---

## 💡 Key Points

- Moves HEAD
- Can modify history
- Used before pushing
- Powerful but risky

---

## 🎤 Follow-up Interview Questions

- What is Soft Reset?
- What is Mixed Reset?
- What is Hard Reset?

</details>

---

# Q25. What is the difference between Git Reset and Git Revert?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Reset removes or rewrites commit history, whereas Git Revert preserves history by creating a new commit that reverses previous changes.

---

## 📖 Detailed Explanation

Reset changes the repository history and is generally used before pushing commits. Revert creates a new commit and is recommended for shared or production repositories.

---

## 🌍 Real World Example

Before pushing your work, you can safely use Reset to clean up mistakes. After code has been shared with the team, Revert is the safer choice.

---

## 💡 Key Points

- Reset changes history
- Revert preserves history
- Reset for local work
- Revert for shared repositories

---

## 🎤 Follow-up Interview Questions

- Which command is safer in Production?
- Can Reset affect other developers?

</details>

---

# Q26. What is Git Cherry-pick?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Cherry-pick copies a specific commit from one branch and applies it to another branch.

---

## 📖 Detailed Explanation

Instead of merging an entire branch, Cherry-pick allows developers to select only the required commit. This is useful when only one bug fix or feature needs to be transferred.

---

## 🌍 Real World Example

A critical security fix exists in the Development branch. Instead of merging all changes, the Production team Cherry-picks only the security fix commit.

---

## 💡 Key Points

- Copies selected commits
- Does not merge entire branch
- Useful for hotfixes
- Common in Production

---

## 🎤 Follow-up Interview Questions

- When should Cherry-pick be used?
- Can Cherry-pick create conflicts?

</details>

---

# Q27. What is .gitignore?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

The `.gitignore` file tells Git which files and folders should not be tracked or committed.

---

## 📖 Detailed Explanation

Projects often contain temporary files, log files, IDE settings, passwords, or build outputs that should never be committed. These are listed inside the `.gitignore` file.

---

## 🌍 Real World Example

A DevOps project ignores `.terraform`, `*.log`, `.env`, and `node_modules` to keep the repository clean and secure.

---

## 💡 Key Points

- Ignores unwanted files
- Prevents sensitive data exposure
- Keeps repositories clean
- Industry best practice

---

## 🎤 Follow-up Interview Questions

- Can Git ignore already tracked files?
- What files should be added to `.gitignore`?

</details>

---

# Q28. Why do we use SSH with GitHub?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

SSH provides secure, password-free authentication between your local machine and GitHub.

---

## 📖 Detailed Explanation

SSH uses a Public Key and Private Key pair for authentication. After configuring SSH, developers can securely perform Git operations without entering their username and password every time.

---

## 🌍 Real World Example

A DevOps Engineer performs hundreds of Git Push operations daily. SSH authentication eliminates repeated password prompts while maintaining strong security.

---

## 💡 Key Points

- Secure authentication
- Password-free access
- Public and Private Key pair
- Industry standard

---

## 🎤 Follow-up Interview Questions

- Difference between HTTPS and SSH?
- How do you generate an SSH Key?
- Where is the SSH Public Key stored?

</details>

---

# Q29. What is the difference between HTTPS and SSH in Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

HTTPS uses username and password (or Personal Access Token) for authentication, whereas SSH uses cryptographic key pairs for secure authentication.

---

## 📖 Detailed Explanation

HTTPS is easier for beginners, while SSH is the preferred method in enterprise environments because it is more secure and convenient for frequent Git operations.

---

## 🌍 Real World Example

Most companies configure SSH authentication on developers' laptops so they can work without entering credentials repeatedly.

---

## 💡 Key Points

- HTTPS uses credentials or PAT
- SSH uses key-based authentication
- SSH is more secure
- SSH is preferred in enterprise environments

---

## 🎤 Follow-up Interview Questions

- Which method is recommended in Production?
- Can both HTTPS and SSH access the same repository?

</details>

---

# Q30. Why is Git important for DevOps Engineers?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git is essential for DevOps because it enables version control, collaboration, automation, and integration with modern CI/CD pipelines.

---

## 📖 Detailed Explanation

Almost every DevOps tool integrates with Git. Technologies such as GitHub Actions, Azure DevOps, Jenkins, GitLab CI/CD, Terraform, Docker, Kubernetes, and Ansible use Git repositories as the central source of truth.

Without Git, managing infrastructure, application code, automation scripts, and deployments becomes difficult and error-prone.

---

## 🌍 Real World Example

An organization stores Azure Infrastructure as Code (Terraform), Kubernetes manifests, Dockerfiles, CI/CD pipelines, and documentation in Git. Every infrastructure change is reviewed, approved, and deployed through Git-based workflows.

---

## 💡 Key Points

- Foundation of DevOps
- Enables CI/CD
- Supports Infrastructure as Code
- Improves collaboration
- Provides complete audit history
- Industry standard

---

## 🎤 Follow-up Interview Questions

- How does Git integrate with CI/CD?
- What is GitOps?
- Why is Git considered the Single Source of Truth?
- Which DevOps tools integrate with Git?

</details>

---