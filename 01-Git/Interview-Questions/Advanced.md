# Advanced Git Interview Questions

> **Level:** Advanced
>
> **Part 1 (Q1 - Q10)**

---

# Q1. What are Git Objects?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git stores all repository data as objects. The four main Git objects are **Blob, Tree, Commit, and Tag**.

---

## 📖 Detailed Explanation

Git doesn't store files like a normal file system. Instead, everything is stored as objects inside the `.git/objects` directory.

The four Git objects are:

- **Blob** → Stores file content.
- **Tree** → Stores directory structure.
- **Commit** → Stores project snapshot and metadata.
- **Tag** → Marks important commits like releases.

These objects are linked together using SHA-1 hashes.

---

## 🌍 Real World Example

When you commit a Terraform project, Git creates Blob objects for the files, Tree objects for folders, and a Commit object representing the project state.

---

## 💡 Key Points

- Blob
- Tree
- Commit
- Tag
- Stored inside `.git/objects`

---

## 🎤 Follow-up Interview Questions

- What is a Blob?
- What is a Tree object?
- How are Git objects identified?

</details>

---

# Q2. What is a Blob Object in Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Blob (Binary Large Object) stores the contents of a file without any filename or directory information.

---

## 📖 Detailed Explanation

Whenever a file is committed, Git stores its content as a Blob object. The filename and folder structure are managed separately by Tree objects.

If two files have identical content, Git stores only one Blob object, saving storage space.

---

## 🌍 Real World Example

Two README files with exactly the same content will reference the same Blob object.

---

## 💡 Key Points

- Stores file content only
- No filename
- No directory information
- SHA-1 based

---

## 🎤 Follow-up Interview Questions

- Can two files share one Blob?
- Where are Blob objects stored?

</details>

---

# Q3. What is a Tree Object?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Tree object represents the directory structure of a Git repository.

---

## 📖 Detailed Explanation

Tree objects organize Blob objects into folders and subfolders.

A Tree stores:

- File names
- Folder names
- Blob references
- Child Tree references

---

## 🌍 Real World Example

Your Azure project contains:

```
Terraform/
Scripts/
README.md
```

Git stores this folder structure inside Tree objects.

---

## 💡 Key Points

- Represents folders
- Links Blobs
- Maintains directory hierarchy
- Uses SHA references

---

## 🎤 Follow-up Interview Questions

- Tree vs Blob?
- Can a Tree contain another Tree?

</details>

---

# Q4. What is a Commit Object?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Commit object stores a snapshot of the repository along with metadata such as author, timestamp, parent commit, and commit message.

---

## 📖 Detailed Explanation

Every Git commit creates a Commit object.

It stores:

- Tree reference
- Parent commit
- Author
- Date
- Commit message

This structure forms Git's commit history.

---

## 🌍 Real World Example

After completing an Azure Firewall deployment, you commit the changes.

Git creates a Commit object representing the project's current state.

---

## 💡 Key Points

- Snapshot
- Metadata
- Parent commit
- Commit message

---

## 🎤 Follow-up Interview Questions

- What information does a Commit store?
- Why is every Commit unique?

</details>

---

# Q5. What is a Tag Object?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Tag object points to a specific commit and is generally used to mark software releases.

---

## 📖 Detailed Explanation

Tags are permanent references.

Unlike branches, tags never move.

Common examples include:

```
v1.0.0
v2.0.0
v3.1.5
```

---

## 🌍 Real World Example

After deploying Version 2.0 of an Azure Infrastructure project, the release is tagged as **v2.0.0**.

---

## 💡 Key Points

- Release marker
- Permanent reference
- Doesn't move
- Supports versioning

---

## 🎤 Follow-up Interview Questions

- Lightweight Tag vs Annotated Tag?
- Why use Tags?

</details>

---

# Q6. What is SHA-1 in Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

SHA-1 is a hashing algorithm used by Git to uniquely identify every object stored in the repository.

---

## 📖 Detailed Explanation

Each Git object receives a unique 40-character hexadecimal hash.

This ensures object integrity and allows Git to detect changes efficiently.

---

## 🌍 Real World Example

Every commit you create receives a unique SHA-1 hash such as:

```
5b6e3f3f1c2ab56...
```

This hash uniquely identifies that commit.

---

## 💡 Key Points

- Unique identifier
- 40-character hash
- Used for all Git objects
- Ensures integrity

---

## 🎤 Follow-up Interview Questions

- Can two commits have the same SHA?
- Why does Git use hashing?

</details>

---

# Q7. What is Git Packfile?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

A Packfile is a compressed file that stores multiple Git objects efficiently to reduce repository size.

---

## 📖 Detailed Explanation

Instead of storing every object separately, Git compresses them into Packfiles.

This improves performance and reduces storage usage, especially in large repositories.

---

## 🌍 Real World Example

A repository with 100,000 commits is compressed into Packfiles to improve clone and fetch performance.

---

## 💡 Key Points

- Compression
- Better performance
- Reduced storage
- Faster cloning

---

## 🎤 Follow-up Interview Questions

- When are Packfiles created?
- Why are Packfiles important?

</details>

---

# Q8. What is Git Garbage Collection (GC)?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Garbage Collection removes unnecessary objects and optimizes repository storage.

---

## 📖 Detailed Explanation

Over time, repositories accumulate unreachable objects.

Git GC:

- Cleans unused objects
- Compresses objects
- Optimizes Packfiles

This improves repository performance.

---

## 🌍 Real World Example

A repository used for five years is optimized using Git Garbage Collection to reduce its storage size.

---

## 💡 Key Points

- Cleans repository
- Removes unreachable objects
- Compresses storage
- Improves performance

---

## 🎤 Follow-up Interview Questions

- What does Git GC remove?
- Is Git GC automatic?

</details>

---

# Q9. What is Git Repository Optimization?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Repository optimization improves Git performance by reducing repository size and cleaning unnecessary data.

---

## 📖 Detailed Explanation

Optimization techniques include:

- Git GC
- Packfiles
- Git LFS
- Removing large files
- Cleaning unreachable objects

---

## 🌍 Real World Example

A DevOps team reduces clone time from 15 minutes to 2 minutes after optimizing a large repository.

---

## 💡 Key Points

- Faster cloning
- Better performance
- Smaller repository
- Better storage utilization

---

## 🎤 Follow-up Interview Questions

- How do you optimize large repositories?
- Why do repositories become slow?

</details>

---

# Q10. How does Git store data internally?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git stores data as immutable objects connected through SHA-1 hashes rather than storing traditional file versions.

---

## 📖 Detailed Explanation

Internally Git stores:

- Blob Objects
- Tree Objects
- Commit Objects
- Tag Objects

Each object references another using SHA hashes, forming Git's internal object database.

This design makes Git fast, reliable, and highly efficient.

---

## 🌍 Real World Example

Every commit in an enterprise Azure Infrastructure repository creates a new snapshot by linking Git objects instead of copying the entire project.

---

## 💡 Key Points

- Object Database
- SHA-based references
- Immutable objects
- High performance
- Efficient storage

---

## 🎤 Follow-up Interview Questions

- How is Git different from traditional Version Control?
- Why is Git so fast?
- What is the Object Database?

</details>

---

# Q11. What is Git Hooks?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Hooks are custom scripts that automatically execute before or after specific Git events, allowing teams to automate validation, testing, formatting, and deployment tasks.

---

## 📖 Detailed Explanation

Git provides several hook points such as:

- pre-commit
- commit-msg
- pre-push
- post-merge
- post-checkout

Organizations use hooks to enforce coding standards, run security scans, execute unit tests, or block invalid commits.

---

## 🌍 Real World Example

Before every Terraform commit, a **pre-commit** hook automatically runs:

- terraform fmt
- terraform validate
- tflint

If validation fails, Git blocks the commit.

---

## 💡 Key Points

- Automation
- Quality checks
- Security validation
- Prevents bad commits

---

## 🎤 Follow-up Interview Questions

- Difference between Pre-Commit and Pre-Push Hooks?
- Can Hooks be shared across a team?
- Where are Git Hooks stored?

</details>

---

# Q12. What is Git Worktree?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Worktree allows multiple working directories to use the same Git repository simultaneously.

---

## 📖 Detailed Explanation

Normally one repository has one working directory.

Using Git Worktree, developers can check out multiple branches into separate folders without cloning the repository multiple times.

---

## 🌍 Real World Example

A DevOps Engineer works on:

- Feature Branch
- Hotfix Branch
- Release Branch

All simultaneously using separate worktrees.

---

## 💡 Key Points

- Multiple working directories
- One repository
- Saves disk space
- Faster than multiple clones

---

## 🎤 Follow-up Interview Questions

- Worktree vs Clone?
- When should Worktree be used?

</details>

---

# Q13. What is Git Archive?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Archive creates a ZIP or TAR package of a repository without including Git history.

---

## 📖 Detailed Explanation

Unlike Clone, Git Archive exports only the project files.

The generated archive does not contain the `.git` directory or commit history.

---

## 🌍 Real World Example

A client requests only the application source code.

The engineer creates a ZIP using Git Archive instead of sharing the repository.

---

## 💡 Key Points

- Creates ZIP/TAR
- No Git history
- Clean source package
- Good for releases

---

## 🎤 Follow-up Interview Questions

- Archive vs Clone?
- Does Archive include `.git`?

</details>

---

# Q14. What is Git Bundle?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Bundle packages an entire repository into a single file for offline transfer.

---

## 📖 Detailed Explanation

A bundle contains commits, branches, tags, and repository history.

It is useful when network connectivity is unavailable.

---

## 🌍 Real World Example

A secure government environment blocks internet access.

Developers exchange repositories using Git Bundles.

---

## 💡 Key Points

- Offline repository transfer
- Single bundle file
- Includes history
- Secure environments

---

## 🎤 Follow-up Interview Questions

- Bundle vs Clone?
- When is Git Bundle useful?

</details>

---

# Q15. What is Git Notes?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Notes allow additional information to be attached to commits without changing commit history.

---

## 📖 Detailed Explanation

Notes are useful for storing:

- Review comments
- Audit information
- Build numbers
- Deployment references

They exist separately from the commit itself.

---

## 🌍 Real World Example

A release engineer attaches the production deployment ID to a release commit using Git Notes.

---

## 💡 Key Points

- Extra metadata
- Doesn't modify commit
- Useful for auditing
- Separate storage

---

## 🎤 Follow-up Interview Questions

- Why use Notes instead of Commit Messages?
- Are Notes shared automatically?

</details>

---

# Q16. What is Git Replace?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Replace temporarily substitutes one Git object with another without permanently modifying repository history.

---

## 📖 Detailed Explanation

Git Replace is mainly used for debugging, testing, or repairing repository history.

It creates replacement references rather than changing the original objects.

---

## 🌍 Real World Example

A developer temporarily replaces an old commit during repository analysis without rewriting history.

---

## 💡 Key Points

- Temporary replacement
- Debugging
- Doesn't modify original objects
- Advanced feature

---

## 🎤 Follow-up Interview Questions

- Replace vs Rebase?
- When is Git Replace useful?

</details>

---

# Q17. What is Git Rerere?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git Rerere (Reuse Recorded Resolution) automatically remembers and reapplies previously resolved merge conflicts.

---

## 📖 Detailed Explanation

When identical merge conflicts occur again, Git can reuse the previous resolution instead of asking the developer to resolve it manually.

---

## 🌍 Real World Example

A long-running release branch repeatedly encounters the same merge conflict.

Git Rerere resolves it automatically based on earlier conflict resolutions.

---

## 💡 Key Points

- Conflict automation
- Saves time
- Learns previous resolutions
- Useful for long-lived branches

---

## 🎤 Follow-up Interview Questions

- How do you enable Git Rerere?
- When should Rerere be used?

</details>

---

# Q18. What is Repository Mirroring?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Repository Mirroring creates an exact copy of a Git repository, including branches, tags, and references.

---

## 📖 Detailed Explanation

Mirroring is commonly used for:

- Backup
- Disaster Recovery
- Migration
- Multi-region repositories

Everything from the original repository is copied.

---

## 🌍 Real World Example

An organization mirrors GitHub repositories to an internal GitLab server for backup and compliance.

---

## 💡 Key Points

- Exact copy
- Backup
- Disaster Recovery
- Migration

---

## 🎤 Follow-up Interview Questions

- Mirror vs Clone?
- Why do enterprises mirror repositories?

</details>

---

# Q19. What are Protected Branches?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Protected Branches prevent direct changes and enforce approval policies before code can be merged.

---

## 📖 Detailed Explanation

Organizations usually protect branches like:

- main
- master
- production

Common rules include:

- No direct push
- Mandatory Pull Request
- Required code reviews
- Passing CI/CD checks
- Restricted merge permissions

---

## 🌍 Real World Example

The Production branch only accepts merges after approval from two Senior DevOps Engineers and successful pipeline execution.

---

## 💡 Key Points

- Security
- Code review
- Prevent accidental changes
- Enterprise best practice

---

## 🎤 Follow-up Interview Questions

- Why protect the Main branch?
- What rules are commonly configured?

</details>

---

# Q20. How is Git used in Enterprise CI/CD Pipelines?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git acts as the central source of truth for CI/CD pipelines by triggering automated build, testing, security scanning, and deployment processes.

---

## 📖 Detailed Explanation

A common enterprise workflow is:

1. Developer pushes code.
2. Pull Request is created.
3. Code Review is completed.
4. CI Pipeline runs.
5. Security Scan executes.
6. Automated Tests run.
7. Build is generated.
8. Deployment is triggered.
9. Production is updated after approval.

Git integrates with tools like GitHub Actions, Azure DevOps, Jenkins, GitLab CI/CD, Argo CD, and Flux.

---

## 🌍 Real World Example

An Azure DevOps project automatically deploys Terraform Infrastructure whenever approved code is merged into the **main** branch.

---

## 💡 Key Points

- Source of Truth
- Automation
- CI/CD Integration
- Security Validation
- Infrastructure as Code
- Enterprise Workflow

---

## 🎤 Follow-up Interview Questions

- How does Git trigger CI/CD?
- Which CI/CD tools integrate with Git?
- What happens after a Pull Request is merged?

</details>

---

# Q21. How do you recover deleted commits in Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Deleted commits can often be recovered using **Git Reflog**, which records every movement of the HEAD pointer.

---

## 📖 Detailed Explanation

Even after performing commands like `git reset --hard`, Git usually keeps a reference to previous commits in the Reflog.

You can locate the lost commit and restore it by creating a branch or resetting to that commit.

---

## 🌍 Real World Example

A developer accidentally performs a Hard Reset before pushing. Using Git Reflog, the lost commit is found and restored within minutes.

---

## 💡 Key Points

- Uses Git Reflog
- Recovers lost commits
- Works after Reset
- Important recovery tool

---

## 🎤 Follow-up Interview Questions

- Can Reflog recover deleted branches?
- How long are Reflog entries stored?

</details>

---

# Q22. How do you recover a deleted branch?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

If the branch's commits still exist in the repository, Git Reflog can be used to recover the deleted branch.

---

## 📖 Detailed Explanation

Deleting a branch removes only the branch reference, not necessarily the commits.

If those commits haven't been garbage collected, they can be recovered using the commit hash from Reflog.

---

## 🌍 Real World Example

A feature branch is deleted by mistake after code review. The engineer restores it using the last commit recorded in Reflog.

---

## 💡 Key Points

- Uses Reflog
- Branch reference can be recreated
- Commits usually remain
- Useful recovery technique

---

## 🎤 Follow-up Interview Questions

- What if Garbage Collection has already removed the commit?
- How do you create the branch again?

</details>

---

# Q23. What is the difference between Author and Committer in Git?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

The **Author** is the person who originally wrote the code, while the **Committer** is the person who last committed or applied the changes.

---

## 📖 Detailed Explanation

Normally both values are the same.

However, after operations like **Cherry-pick**, **Rebase**, or **Applying a Patch**, the Author and Committer may be different.

Git stores both pieces of information in every commit.

---

## 🌍 Real World Example

A developer writes a feature, but a Release Engineer cherry-picks it into the Production branch. The developer remains the Author, while the Release Engineer becomes the Committer.

---

## 💡 Key Points

- Author writes code
- Committer applies commit
- Stored separately
- Useful for auditing

---

## 🎤 Follow-up Interview Questions

- When are Author and Committer different?
- How can you view both values?

</details>

---

# Q24. What is a Detached Repository?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

There is **no Git feature called a Detached Repository**. Interviewers usually mean a **Detached HEAD** state.

---

## 📖 Detailed Explanation

Sometimes interviewers intentionally use incorrect terminology to check conceptual understanding.

The correct Git concept is **Detached HEAD**, where HEAD points directly to a commit instead of a branch.

---

## 🌍 Real World Example

During an interview, the interviewer asks about a Detached Repository. A knowledgeable candidate politely explains that Git uses the term Detached HEAD.

---

## 💡 Key Points

- Trick interview question
- Correct term is Detached HEAD
- Tests Git fundamentals

---

## 🎤 Follow-up Interview Questions

- Explain Detached HEAD.
- Can commits be created in Detached HEAD?

</details>

---

# Q25. What happens internally when you run Git Commit?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git creates Blob, Tree, and Commit objects, calculates SHA hashes, and updates the current branch reference.

---

## 📖 Detailed Explanation

Internally Git performs these steps:

1. Creates Blob objects for file contents.
2. Creates Tree objects for directory structure.
3. Creates a Commit object.
4. Updates the branch pointer.
5. Moves HEAD to the new commit.

---

## 🌍 Real World Example

A single `git commit` updates Git's object database instead of copying the entire project.

---

## 💡 Key Points

- Blob
- Tree
- Commit
- SHA Hash
- HEAD updated

---

## 🎤 Follow-up Interview Questions

- Which object is created first?
- Why is Git fast?

</details>

---

# Q26. How do large organizations manage Git repositories?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Large organizations use branching strategies, protected branches, code reviews, CI/CD pipelines, access control, automated testing, and repository governance.

---

## 📖 Detailed Explanation

Enterprise Git management typically includes:

- Branch Protection
- Pull Requests
- Mandatory Reviews
- CI/CD Pipelines
- Security Scanning
- Signed Commits
- Role-Based Access Control
- Release Management

---

## 🌍 Real World Example

A banking organization allows only Release Managers to merge into the Production branch after security and compliance checks.

---

## 💡 Key Points

- Governance
- Security
- Automation
- Compliance
- Reviews

---

## 🎤 Follow-up Interview Questions

- What is Branch Protection?
- Why are approvals mandatory?

</details>

---

# Q27. What is Repository Governance?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Repository Governance refers to the policies and standards that control how repositories are managed within an organization.

---

## 📖 Detailed Explanation

Governance includes:

- Branch naming
- Commit message standards
- Review requirements
- Merge policies
- Repository permissions
- Secret scanning
- Release process

These practices improve consistency and security.

---

## 🌍 Real World Example

A cloud engineering team follows standardized branch names, mandatory reviews, and signed commits across all repositories.

---

## 💡 Key Points

- Policies
- Standards
- Security
- Compliance
- Consistency

---

## 🎤 Follow-up Interview Questions

- Why is governance important?
- Who defines governance rules?

</details>

---

# Q28. What are Signed Commits?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Signed commits use GPG or SSH signatures to verify the identity of the person who created the commit.

---

## 📖 Detailed Explanation

Unsigned commits prove that a commit exists.

Signed commits additionally prove that the commit was created by a trusted identity and has not been tampered with.

Many enterprises require commit signing for critical repositories.

---

## 🌍 Real World Example

Every production deployment commit must be GPG-signed before it can be merged into the main branch.

---

## 💡 Key Points

- Identity verification
- Security
- GPG / SSH signatures
- Enterprise best practice

---

## 🎤 Follow-up Interview Questions

- Why use signed commits?
- GPG vs SSH signing?

</details>

---

# Q29. What are common Git security best practices?

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

Git security focuses on protecting repositories through proper authentication, access control, branch protection, secret management, and code review.

---

## 📖 Detailed Explanation

Common best practices include:

- Use SSH or Personal Access Tokens
- Enable MFA
- Protect main branch
- Require Pull Requests
- Scan for secrets
- Sign commits
- Apply least privilege access
- Regularly audit repository permissions

---

## 🌍 Real World Example

An enterprise blocks direct pushes to the Production branch and automatically scans every Pull Request for exposed credentials.

---

## 💡 Key Points

- Authentication
- Branch Protection
- Secret Scanning
- Least Privilege
- Signed Commits

---

## 🎤 Follow-up Interview Questions

- Why avoid passwords?
- What is Secret Scanning?
- What is Least Privilege?

</details>

---

# Q30. Explain a complete Enterprise Git Workflow.

<details>
<summary><b>✅ Show Answer</b></summary>

## 🎯 Interview Answer (30 Seconds)

An Enterprise Git Workflow includes branching, development, code review, automated testing, security validation, deployment, monitoring, and release management.

---

## 📖 Detailed Explanation

A typical workflow is:

1. Clone Repository
2. Create Feature Branch
3. Develop Feature
4. Commit Changes
5. Push Branch
6. Create Pull Request
7. Code Review
8. Automated Testing
9. Security Scan
10. Merge Approval
11. CI/CD Deployment
12. Production Release
13. Monitoring
14. Tag Release

This workflow ensures high-quality, secure, and traceable software delivery.

---

## 🌍 Real World Example

An Azure DevOps team develops Infrastructure as Code using feature branches. Every Pull Request triggers validation, security scanning, Terraform planning, and automated deployment after approval.

---

## 💡 Key Points

- Feature Branch
- Pull Request
- Code Review
- CI/CD
- Security
- Deployment
- Monitoring
- Release Tags

---

## 🎤 Follow-up Interview Questions

- Which step prevents bad code from reaching Production?
- Where does CI/CD fit into the workflow?
- Why are release tags important?

</details>

---