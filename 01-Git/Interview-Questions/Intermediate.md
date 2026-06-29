# Intermediate Git Interview Questions

> **Level:** Intermediate
>
> **Part 1 (Q1 - Q10)**

---

# Q1. What is Git Stash?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Stash temporarily saves uncommitted changes without creating a commit, allowing you to switch branches or perform other tasks safely.

---

## 📖 Detailed Explanation

Sometimes you are working on a feature but suddenly need to fix a production issue. Since your current work is incomplete, you don't want to commit it yet.

Git Stash stores your uncommitted changes in a temporary area and restores your working directory to the last committed state.

Later, you can apply those changes back using Git Stash commands.

---

## 🌍 Real World Example

You are developing a new Azure Terraform module.

Suddenly, a Production Firewall issue is reported.

Instead of creating an unnecessary commit, you stash your current work, switch to the production branch, fix the issue, and later continue your original work.

---

## 💡 Key Points

- Temporarily saves changes
- No commit required
- Useful before switching branches
- Safe way to pause development

---

## 🎤 Follow-up Interview Questions

- Difference between Stash and Commit?
- Does Stash save untracked files?
- How do you view all stashes?

</details>

---

# Q2. What is Detached HEAD in Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Detached HEAD is a state where HEAD points directly to a commit instead of a branch.

---

## 📖 Detailed Explanation

Normally, HEAD points to the latest commit of the current branch.

If you checkout a specific commit instead of a branch, HEAD becomes detached.

You can view old project versions, but new commits created in this state are not attached to any branch unless a new branch is created.

---

## 🌍 Real World Example

A Cloud Engineer wants to inspect the infrastructure code from six months ago.

Instead of switching branches, they checkout the specific commit.

Now HEAD is detached.

---

## 💡 Key Points

- HEAD points to commit
- Not attached to any branch
- Used for history inspection
- Create a branch before continuing work

---

## 🎤 Follow-up Interview Questions

- Is Detached HEAD dangerous?
- How do you recover from Detached HEAD?
- Can you commit in Detached HEAD?

</details>

---

# Q3. What is Git Reflog?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Reflog records every movement of HEAD, allowing developers to recover lost commits and branches.

---

## 📖 Detailed Explanation

Even if commits disappear after a reset or rebase, Git Reflog keeps a record of where HEAD has been.

It is one of the most useful recovery tools in Git.

---

## 🌍 Real World Example

A developer accidentally performs a Hard Reset and loses today's commits.

Using Git Reflog, they locate the previous commit and restore the work within minutes.

---

## 💡 Key Points

- Tracks HEAD history
- Helps recover lost commits
- Useful after reset
- Powerful troubleshooting tool

---

## 🎤 Follow-up Interview Questions

- Difference between Log and Reflog?
- Can Reflog recover deleted commits?

</details>

---

# Q4. What is Fast-Forward Merge?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Fast-Forward Merge occurs when the target branch has no new commits, allowing Git to simply move the branch pointer forward.

---

## 📖 Detailed Explanation

If no changes exist on the target branch after a feature branch is created, Git does not create a merge commit.

Instead, it moves the branch pointer directly to the latest commit.

---

## 🌍 Real World Example

You create a documentation branch, make three commits, and immediately merge it into main.

Since nobody changed main, Git performs a Fast-Forward Merge.

---

## 💡 Key Points

- No merge commit
- Clean history
- Faster merge
- Happens automatically

---

## 🎤 Follow-up Interview Questions

- When does Fast-Forward fail?
- How do you disable Fast-Forward Merge?

</details>

---

# Q5. What is a Three-Way Merge?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Three-Way Merge combines changes from two branches using their common ancestor and creates a merge commit.

---

## 📖 Detailed Explanation

If both branches have new commits, Git compares the common ancestor, the source branch, and the destination branch before merging.

A new Merge Commit is created.

---

## 🌍 Real World Example

The Networking Team and Security Team both modify the Azure Infrastructure simultaneously.

Git performs a Three-Way Merge to combine both sets of changes.

---

## 💡 Key Points

- Uses common ancestor
- Creates Merge Commit
- Most common merge type
- Preserves history

---

## 🎤 Follow-up Interview Questions

- Difference between Fast-Forward and Three-Way Merge?
- Can Three-Way Merge create conflicts?

</details>

---

# Q6. What is Squash Merge?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Squash Merge combines multiple commits into a single commit before merging into another branch.

---

## 📖 Detailed Explanation

Developers often make many small commits during feature development.

A Squash Merge combines them into one clean commit, resulting in a more readable commit history.

---

## 🌍 Real World Example

A feature branch contains 25 small commits.

Before merging into main, the reviewer squashes them into one meaningful commit.

---

## 💡 Key Points

- Combines multiple commits
- Clean history
- Common in enterprise projects
- Improves readability

---

## 🎤 Follow-up Interview Questions

- Difference between Merge and Squash Merge?
- Does Squash preserve commit history?

</details>

---

# Q7. What is Interactive Rebase?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Interactive Rebase allows developers to edit, reorder, squash, rename, or remove commits before sharing them.

---

## 📖 Detailed Explanation

Interactive Rebase provides complete control over commit history.

It helps clean up development history before pushing code to a shared repository.

---

## 🌍 Real World Example

Before creating a Pull Request, a developer squashes 18 development commits into 3 meaningful commits.

---

## 💡 Key Points

- Edit commits
- Reorder commits
- Squash commits
- Rewrite history

---

## 🎤 Follow-up Interview Questions

- When should Interactive Rebase be used?
- Can Interactive Rebase change commit messages?

</details>

---

# Q8. What is an Upstream Branch?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

An Upstream Branch is the remote branch that your local branch tracks for Push and Pull operations.

---

## 📖 Detailed Explanation

When you push a branch for the first time using `git push -u`, Git establishes a tracking relationship between the local and remote branches.

Future pushes and pulls no longer require specifying the remote branch name.

---

## 🌍 Real World Example

A developer pushes the **feature-vnet** branch using `git push -u origin feature-vnet`.

From then on, a simple `git push` is sufficient.

---

## 💡 Key Points

- Tracks remote branch
- Simplifies Push/Pull
- Created using -u option
- Improves workflow

---

## 🎤 Follow-up Interview Questions

- What does `-u` mean?
- How do you change the upstream branch?

</details>

---

# Q9. What is a Tracking Branch?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Tracking Branch is a local branch linked to a remote branch, allowing Git to monitor incoming and outgoing commits.

---

## 📖 Detailed Explanation

Tracking branches automatically know which remote branch they are associated with.

Git uses this relationship for status checks, pull operations, and push operations.

---

## 🌍 Real World Example

Your local **main** branch tracks **origin/main**, allowing Git to show whether your branch is ahead or behind.

---

## 💡 Key Points

- Linked to remote branch
- Used by Push and Pull
- Tracks synchronization
- Created automatically

---

## 🎤 Follow-up Interview Questions

- Difference between Remote Branch and Tracking Branch?
- How do you view tracking branches?

</details>

---

# Q10. What is a Bare Repository?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Bare Repository is a Git repository that contains only Git metadata and no working directory.

---

## 📖 Detailed Explanation

Bare repositories are designed for sharing code between developers.

Since they do not contain editable project files, they are commonly used as central repositories on Git servers.

Platforms like GitHub, GitLab, and Bitbucket internally use bare repositories.

---

## 🌍 Real World Example

A company hosts a central Git server for all DevOps engineers.

Every developer pushes code to this Bare Repository, while actual development happens on local cloned repositories.

---

## 💡 Key Points

- No working directory
- Used as central repository
- Stores Git history only
- Common on Git servers

---

## 🎤 Follow-up Interview Questions

- Difference between Bare and Normal Repository?
- Why can't you edit files in a Bare Repository?
- Where are Bare Repositories commonly used?

</details>

---

# Q11. What is Git Rebase?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Rebase moves commits from one branch on top of another branch, creating a clean and linear commit history.

---

## 📖 Detailed Explanation

Unlike Merge, Rebase does not create a Merge Commit. Instead, Git replays your commits one by one on top of the latest branch.

This makes the project history cleaner and easier to understand.

However, Rebase rewrites commit history, so it should not be used on branches that have already been shared with other developers.

---

## 🌍 Real World Example

You created a feature branch on Monday.

Meanwhile, the main branch received 20 new commits.

Before creating a Pull Request, you rebase your feature branch on top of the updated main branch to keep the history clean.

---

## 💡 Key Points

- Creates linear history
- No Merge Commit
- Rewrites commit history
- Best before creating Pull Requests

---

## 🎤 Follow-up Interview Questions

- Difference between Merge and Rebase?
- Is Rebase safe on shared branches?
- Can Rebase create conflicts?

</details>

---

# Q12. What is Git Cherry-pick used for?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Cherry-pick copies a specific commit from one branch and applies it to another branch.

---

## 📖 Detailed Explanation

Instead of merging an entire branch, Cherry-pick lets you select only the required commit.

This is commonly used for hotfixes and production bug fixes.

---

## 🌍 Real World Example

A security patch exists in the Development branch.

Instead of merging the entire branch, the Production team Cherry-picks only the security fix.

---

## 💡 Key Points

- Copies selected commits
- Avoids full merge
- Useful for hotfixes
- Common in Production

---

## 🎤 Follow-up Interview Questions

- Cherry-pick vs Merge?
- Can Cherry-pick cause conflicts?

</details>

---

# Q13. What is Git Bisect?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Bisect is used to identify the exact commit that introduced a bug using binary search.

---

## 📖 Detailed Explanation

Instead of checking every commit manually, Git Bisect divides the commit history into halves until it finds the problematic commit.

This saves significant debugging time in large projects.

---

## 🌍 Real World Example

Yesterday's deployment worked, but today's deployment failed.

Using Git Bisect, the DevOps Engineer identifies the exact commit responsible for the issue.

---

## 💡 Key Points

- Binary Search
- Finds bad commit
- Speeds up debugging
- Useful in large repositories

---

## 🎤 Follow-up Interview Questions

- How does Git Bisect work?
- Why is Binary Search used?

</details>

---

# Q14. What is Git Blame?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Blame shows who last modified each line of a file and when it was changed.

---

## 📖 Detailed Explanation

Git Blame displays the commit ID, author, date, and modified lines.

It is useful for debugging and understanding why a particular change was introduced.

---

## 🌍 Real World Example

A firewall rule suddenly stopped working.

Using Git Blame, the engineer finds who modified the configuration and reviews the related commit.

---

## 💡 Key Points

- Line-by-line history
- Shows author
- Shows commit ID
- Useful for debugging

---

## 🎤 Follow-up Interview Questions

- Difference between Git Log and Git Blame?
- Does Git Blame modify files?

</details>

---

# Q15. What is Git Clean?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Clean removes untracked files and directories from the working directory.

---

## 📖 Detailed Explanation

Temporary files, build artifacts, and unused folders often accumulate during development.

Git Clean permanently deletes these untracked files.

Since the deletion cannot be undone, developers usually perform a dry run first.

---

## 🌍 Real World Example

Before packaging a project, a developer removes temporary files using Git Clean.

---

## 💡 Key Points

- Removes untracked files
- Cleans workspace
- Permanent deletion
- Use dry run first

---

## 🎤 Follow-up Interview Questions

- What is `git clean -n`?
- Difference between Reset and Clean?

</details>

---

# Q16. What is Git Hooks?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Hooks are scripts that automatically execute before or after specific Git events.

---

## 📖 Detailed Explanation

Hooks automate repetitive tasks such as code formatting, testing, linting, or security scanning.

Common hooks include:

- pre-commit
- pre-push
- post-merge

---

## 🌍 Real World Example

Before every commit, a Pre-Commit Hook automatically checks Terraform formatting and prevents invalid code from being committed.

---

## 💡 Key Points

- Automation
- Custom scripts
- Improve code quality
- Common in DevOps

---

## 🎤 Follow-up Interview Questions

- What is a Pre-Commit Hook?
- Can Hooks prevent commits?

</details>

---

# Q17. What is Git Squash?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Squash combines multiple commits into a single meaningful commit.

---

## 📖 Detailed Explanation

During development, developers often create many small commits.

Before merging into the main branch, these commits are combined into one clean commit to improve readability.

---

## 🌍 Real World Example

A feature branch contains 30 commits.

Before creating the Pull Request, they are squashed into one commit called:

```
Add Azure VNet Module
```

---

## 💡 Key Points

- Combines commits
- Cleaner history
- Common before PR
- Improves readability

---

## 🎤 Follow-up Interview Questions

- Squash vs Merge?
- How is Squash performed?

</details>

---

# Q18. What is a Pull Request (PR)?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Pull Request is a request to merge changes from one branch into another after review and approval.

---

## 📖 Detailed Explanation

Instead of directly pushing code into the main branch, developers create Pull Requests.

Team members review the code, discuss improvements, approve changes, and then merge them.

---

## 🌍 Real World Example

A Cloud Engineer completes an Azure Firewall module.

Instead of merging directly into main, they create a Pull Request for team review.

---

## 💡 Key Points

- Code Review
- Team Collaboration
- Approval Process
- Better Code Quality

---

## 🎤 Follow-up Interview Questions

- Pull Request vs Merge?
- Who approves Pull Requests?

</details>

---

# Q19. What is Code Review?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Code Review is the process of examining code changes before they are merged into the main branch.

---

## 📖 Detailed Explanation

During Code Review, team members verify:

- Code Quality
- Security
- Performance
- Best Practices
- Naming Standards

This helps reduce bugs and maintain high-quality code.

---

## 🌍 Real World Example

Before deploying Terraform code to Production, a Senior Cloud Engineer reviews the Pull Request.

---

## 💡 Key Points

- Improves quality
- Finds bugs
- Knowledge sharing
- Team collaboration

---

## 🎤 Follow-up Interview Questions

- Why is Code Review important?
- What should be checked during review?

</details>

---

# Q20. What is Git Workflow?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Git Workflow defines how developers use branches, commits, reviews, and merges while working on a project.

---

## 📖 Detailed Explanation

A standard enterprise Git Workflow usually follows these steps:

1. Clone Repository
2. Create Feature Branch
3. Develop Feature
4. Commit Changes
5. Push Branch
6. Create Pull Request
7. Code Review
8. Merge into Main
9. Deploy

Following a workflow ensures consistency, reduces conflicts, and improves collaboration.

---

## 🌍 Real World Example

An Azure DevOps team follows a Feature Branch Workflow where every new feature is developed on a separate branch and merged only after review and testing.

---

## 💡 Key Points

- Standard development process
- Team collaboration
- Code review
- Controlled deployment
- Industry best practice

---

## 🎤 Follow-up Interview Questions

- What are common Git Workflows?
- What is GitFlow?
- What is Feature Branch Workflow?
- Which workflow is most commonly used today?

</details>

---

# Q21. What is GitFlow?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

GitFlow is a branching strategy that uses dedicated branches such as **main**, **develop**, **feature**, **release**, and **hotfix** to manage software development.

---

## 📖 Detailed Explanation

GitFlow provides a structured workflow for large teams.

Common branches include:

- **main** → Production-ready code
- **develop** → Integration branch
- **feature/** → New features
- **release/** → Release preparation
- **hotfix/** → Production bug fixes

Although many modern teams prefer simpler workflows, GitFlow is still widely used in enterprise environments.

---

## 🌍 Real World Example

A banking application uses GitFlow to ensure production releases remain stable while developers continue building new features.

---

## 💡 Key Points

- Structured workflow
- Multiple branch types
- Suitable for large teams
- Supports stable releases

---

## 🎤 Follow-up Interview Questions

- What is the Develop branch?
- Difference between Feature and Hotfix branch?
- Is GitFlow still used today?

</details>

---

# Q22. What is Trunk-Based Development?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Trunk-Based Development is a workflow where developers frequently merge small changes into a single main branch.

---

## 📖 Detailed Explanation

Instead of maintaining long-lived feature branches, developers create short-lived branches or commit directly to the trunk after code review.

This approach supports Continuous Integration and Continuous Delivery (CI/CD).

---

## 🌍 Real World Example

A DevOps team deploying multiple times a day uses Trunk-Based Development to keep the codebase continuously releasable.

---

## 💡 Key Points

- Short-lived branches
- Frequent integration
- CI/CD friendly
- Reduces merge conflicts

---

## 🎤 Follow-up Interview Questions

- GitFlow vs Trunk-Based Development?
- Why do modern DevOps teams prefer this workflow?

</details>

---

# Q23. What is Fork Workflow?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Fork Workflow allows developers to create their own copy of a repository before contributing changes.

---

## 📖 Detailed Explanation

Instead of working directly on the original repository, contributors fork it, make changes in their own repository, and submit a Pull Request.

This is commonly used in open-source projects.

---

## 🌍 Real World Example

You want to contribute to an open-source Terraform module on GitHub.

You first fork the repository, make changes, and submit a Pull Request.

---

## 💡 Key Points

- Used in open-source projects
- Safe collaboration
- Independent repositories
- Pull Request based

---

## 🎤 Follow-up Interview Questions

- Fork vs Clone?
- Why do open-source projects use Fork Workflow?

</details>

---

# Q24. What is a Monorepo?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Monorepo is a single Git repository that contains multiple applications, services, or projects.

---

## 📖 Detailed Explanation

Instead of creating separate repositories, organizations store all related projects in one repository.

This simplifies dependency management and code sharing.

---

## 🌍 Real World Example

A company stores Terraform, Kubernetes, Docker, Azure DevOps pipelines, and documentation in one central repository.

---

## 💡 Key Points

- Single repository
- Shared code
- Easier dependency management
- Common in large organizations

---

## 🎤 Follow-up Interview Questions

- Monorepo vs Polyrepo?
- Advantages of Monorepo?

</details>

---

# Q25. What is a Polyrepo?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Polyrepo stores each application or service in a separate Git repository.

---

## 📖 Detailed Explanation

Every project has its own repository, history, permissions, and release cycle.

This approach improves isolation and simplifies access control.

---

## 🌍 Real World Example

A company maintains separate repositories for:

- Terraform
- Kubernetes
- Azure DevOps
- Docker
- Documentation

---

## 💡 Key Points

- Multiple repositories
- Better isolation
- Independent releases
- Easier permission management

---

## 🎤 Follow-up Interview Questions

- Monorepo vs Polyrepo?
- Which approach do enterprises prefer?

</details>

---

# Q26. What is Git LFS?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git LFS (Large File Storage) is an extension that manages large binary files efficiently.

---

## 📖 Detailed Explanation

Git is designed for source code, not large files.

Git LFS stores large files separately while keeping lightweight references inside the repository.

---

## 🌍 Real World Example

A Game Development company stores 2 GB texture files using Git LFS instead of the normal Git repository.

---

## 💡 Key Points

- Large file support
- Faster repositories
- Binary file management
- Industry standard

---

## 🎤 Follow-up Interview Questions

- Why not store large files directly in Git?
- Which file types use Git LFS?

</details>

---

# Q27. What are Git Submodules?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Submodules allow one Git repository to include another Git repository as a dependency.

---

## 📖 Detailed Explanation

Instead of copying code, a repository references another repository.

Each submodule maintains its own history and version.

---

## 🌍 Real World Example

A DevOps repository includes a shared Terraform module stored in another repository using Git Submodules.

---

## 💡 Key Points

- Repository inside repository
- Independent version history
- Reusable code
- Common in enterprise projects

---

## 🎤 Follow-up Interview Questions

- Submodule vs Subtree?
- Why use Submodules?

</details>

---

# Q28. What is Git Subtree?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Subtree allows one repository to include another repository without requiring separate submodule management.

---

## 📖 Detailed Explanation

Unlike Submodules, Subtree copies the external repository into the current repository while still allowing synchronization with the original project.

---

## 🌍 Real World Example

A shared Infrastructure module is imported into multiple repositories using Git Subtree, making cloning simpler for developers.

---

## 💡 Key Points

- Easier than Submodules
- Integrated repository
- Simplified cloning
- Supports synchronization

---

## 🎤 Follow-up Interview Questions

- Subtree vs Submodule?
- Which is easier to maintain?

</details>

---

# Q29. What is Semantic Versioning?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Semantic Versioning is a standard versioning format represented as **MAJOR.MINOR.PATCH**.

---

## 📖 Detailed Explanation

Example:

- 1.0.0
- 1.1.0
- 1.1.5
- 2.0.0

Rules:

- **MAJOR** → Breaking changes
- **MINOR** → New features
- **PATCH** → Bug fixes

---

## 🌍 Real World Example

A Terraform module moves from **v1.2.3** to **v2.0.0** because incompatible changes were introduced.

---

## 💡 Key Points

- Industry standard
- MAJOR.MINOR.PATCH
- Used with Releases
- Easy version tracking

---

## 🎤 Follow-up Interview Questions

- Difference between Minor and Patch?
- When should MAJOR be increased?

</details>

---

# Q30. What is GitOps?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

GitOps is a DevOps practice where Git serves as the single source of truth for infrastructure and application deployments.

---

## 📖 Detailed Explanation

Infrastructure, Kubernetes manifests, Terraform code, and deployment configurations are stored in Git.

Automation tools continuously monitor the repository and synchronize infrastructure with the desired state defined in Git.

This improves consistency, traceability, and rollback capabilities.

---

## 🌍 Real World Example

An organization stores all Kubernetes YAML files in GitHub.

Whenever changes are merged into the **main** branch, an automated deployment system updates the Kubernetes cluster.

---

## 💡 Key Points

- Git as Single Source of Truth
- Infrastructure as Code
- CI/CD Integration
- Automated Deployment
- Easy Rollback
- Enterprise DevOps Practice

---

## 🎤 Follow-up Interview Questions

- What tools support GitOps?
- GitOps vs Traditional CI/CD?
- Why is GitOps important for Kubernetes?

</details>

---