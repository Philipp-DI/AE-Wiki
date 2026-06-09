# LF5.3.2: Version Control Paradigms

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a System Administrator,  
> I want to compare Centralized Version Control Systems (like SVN) with Distributed Version Control Systems (like Git),  
> so that I understand the architectural shift in modern software collaboration.

## 🎉 Celebration Criteria (Learning Objectives)

- I can **define** the purpose of a Version Control System (VCS). (K1)
- I **know how to contrast** centralized architectures (SVN) against distributed ones (Git). (K2)
- I can **identify** the single point of failure in a centralized VCS. (K2)

## 🧠 Knowledge Briefing

Without Version Control, teams overwrite each other's files. We need systems to track changes over time.

### Centralized VCS (e.g. SVN):

- There is _one_ central server holding the complete history.
- Developers only have the latest snapshot (the "working copy") on their local machines.
- **Problem:** If the server goes down, no one can look at the history or commit new changes. If the server burns down without a backup, the history is gone.

### Distributed VCS (e.g. Git)

- _Every_ developer clones the _entire_ repository (including the full history) to their local machine.
- You commit changes locally. You only need a network connection to sync (push/pull) with a shared server (like GitHub).
- **Advantage:** Fast local operations, and every developer has a full backup.

## ⚠️ Common Pitfalls

- Thinking Git and GitHub are the same thing. **Git** is the local software managing the version control. **GitHub** is a cloud hosting service that stores Git repositories.

## 🛠️ Mandatory Tasks (K1 - K3)

1. Define what a "Version Control System" is in a single sentence. (K1)
2. Describe the architecture of a Centralized VCS (like SVN) regarding where the repository history is stored. (K2)
3. Explain the architecture of a Distributed VCS (like Git) regarding where the repository history is stored. (K2)
4. Identify the main disadvantage (Single Point of Failure) of a Centralized VCS if the network connection drops. (K2)
5. State the exact difference between "Git" and "GitHub". (K1)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze why large enterprise projects historically preferred SVN over Git regarding access control to specific folders. (K4)
2. Evaluate the storage implications on a developer's local laptop when cloning a massive Git repository with a 10-year history containing large binaries. (K5)
3. Propose a migration strategy for a team moving a 5-year-old SVN project to Git without losing commit history. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Git vs SVN | YouTube | "Centralized vs Distributed Version Control" |
| What is Git | Studyflix / YouTube | "Git Version Control explained" |

</details>

## Answers

### M1: Define what a "Version Control System" is in a single sentence. (K1)

A Version Control System (VCS) is software that records changes to files over time, so that specific versions can be retrieved, compared, and restored at any point.

---

### M2: Describe the architecture of a Centralized VCS (like SVN) regarding where the repository history is stored. (K2)

In a Centralized VCS, the **complete repository history lives on exactly one central server**. Developers only ever download a working copy - the latest snapshot of the files - to their local machine. To look at history, compare versions, or commit new changes, they need a live connection to that central server.

**Analogy:**  
A single filing cabinet in the office. Everyone walks up to it to grab and return documents. The cabinet is the only place where the full record exists.

---

### M3: Explain the architecture of a Distributed VCS (like Git) regarding where the repository history is stored. (K2)

In a Distributed VCS, **every developer clones the entire repository** - including the full history of every commit - onto their local machine. Westermann (LF 7): each participant has a local working copy of the central repository and can work on it independently.

**Analogy:**  
Instead of one shared cabinet, every team member has an identical cabinet at home. They sync up with each other occasionally, but can work, browse history, and save progress completely offline.

---

### M4: Identify the main disadvantage (Single Point of Failure) of a Centralized VCS if the network connection drops. (K2)

The central server is a **Single Point of Failure**. If the network goes down, or worse, the server itself fails without a backup, two things happen simultaneously:

- Nobody can commit new changes.
- Nobody can access the project history.

In the worst case - a server failure with no backup - the entire change history of the project is simply gone. With a Distributed VCS like Git, this risk is naturally mitigated because every developer's local clone _is_ a full backup.

---

### M5: State the exact difference between "Git" and "GitHub". (K1)

**Git** is the version control software itself - a tool that runs locally on your machine and manages the tracking, staging, and committing of changes. Created in 2005 by Linus Torvalds, free, and open source.

**GitHub** is a cloud-based hosting platform for Git repositories. It stores your repository on remote servers and adds collaboration features on top - like Pull Requests, issue tracking, and access management. GitHub is a product built _around_ Git, not a part of Git itself.

**Analogy:**  
Git is the car, GitHub is a garage where you park and share it.

---

### O1: Analyze why large enterprise projects historically preferred SVN over Git regarding access control to specific folders. (K4)

This comes down to a fundamental architectural difference between the two systems.

In SVN, the repository is stored and managed **on the central server** as a directory tree. Because everything lives in one place, administrators can grant or restrict access on a **per-folder basis** - for example, the finance team can read `/project/billing` but not `/project/hr`, and the HR team gets the opposite. This is straightforward to configure with standard server-side permission tools.

Git, by contrast, is designed around **cloning the entire repository** as an atomic unit. When a developer clones a repo, they get everything - every branch, every file, the full history. Git has no native concept of "you may only see this subfolder." Restricting access at the folder level requires **external tooling** (like Gitolite or specific GitHub Enterprise configurations) and is considerably more complex to enforce reliably.

For enterprises handling sensitive code - payroll systems, proprietary algorithms, legal documents sitting alongside general codebase - SVN's granular access control was a compelling reason to stay put, even as Git became dominant elsewhere. The trade-off was accepting SVN's centralized single point of failure in exchange for simpler, more auditable permission structures.

---

### O2: Evaluate the storage implications on a developer's local laptop when cloning a massive Git repository with a 10-year history containing large binaries. (K5)

This is one of Git's genuine weak spots, and it stems directly from the "every clone is a full copy" architecture that otherwise makes Git so resilient.

**What gets downloaded:** A `git clone` fetches not just the current state of the files, but the **complete history of every commit** for the entire lifetime of the repository. For a 10-year project, that can mean tens of thousands of commits, each storing the differences (or in Git's case, snapshots) of every changed file.

**Why binaries make it worse:** Git is optimised for **text files**. It stores diffs between versions efficiently, so a 1 KB change to a Python file adds relatively little to the repository size. Binary files (compiled executables, Photoshop files, video assets, datasets) are a different story - Git cannot meaningfully “diff” them, so it tends to store each version as a full new object. A 50 MB binary that was updated 200 times over 10 years could contribute 10 GB to the repository history, even if today's version is still only 50 MB.

**Practical consequences:**

- Clone times can stretch from seconds to hours over a normal connection.
- The `.git/` folder on the developer's laptop can balloon to many gigabytes, eating into SSD space on a machine that otherwise just needs to run the app.
- Operations like `git log` or `git gc` slow down as the object database grows.

**How teams address it:**

- **Git LFS (Large File Storage):** stores binary blobs on a separate server and replaces them in the repo with small pointer files. The full binary is only downloaded when actually needed. _(Source:_ [_git-lfs.com_](http://git-lfs.com)_)_
- **Shallow clones** (`git clone --depth=1`): fetches only the most recent snapshot, skipping history entirely - useful for CI/CD pipelines that just need to build the current code.
- **Repository splits:** keeping large assets in a separate repository and linking them via Git submodules.

Evaluation: Git's distributed model is a poor fit for repositories dominated by large binaries. Teams in game development, video production, or machine learning (large model weights) often bolt on Git Large File Storage (LFS) or reach for specialised tools like Perforce, which was designed with binary-heavy workflows in mind.

---

### O3: Propose a migration strategy for a team moving a 5-year-old SVN project to Git without losing commit history. (K6)

Migrating from SVN to Git while preserving history is well established. The main tool for it is `git svn`, which ships with Git itself.

:::warning
**Phase 1 - Preparation**

- Audit the SVN repository: identify the standard layout (`/trunk`, `/branches`, `/tags`) and check for any non-standard structures.
- Collect a mapping of all SVN committer usernames to their real names and email addresses - Git requires both for commits, SVN only stores usernames. Store this in an `authors.txt` file.
- IMPORTANT! Communicate a **freeze date** to the team: no new SVN commits after a set time. History that arrives during migration will be missed.
:::

:::danger
**Phase 2 - Migration**

```bash
git svn clone https://svn.example.com/project \
  --trunk=trunk \
  --branches=branches \
  --tags=tags \
  --authors-file=authors.txt \
  --no-metadata \
  -A authors.txt \
  ./project-git
```

This command replays every SVN revision as a Git commit, in order, preserving author, timestamp, and commit message. For a 5-year repository this can take hours - run it somewhere stable.
:::

:::note
**Phase 3 - Clean up**

- SVN tags become branches in Git by default - convert them to proper Git tags.
- Remove the `git-svn-id` lines from commit messages if `--no-metadata` was not used.
- Verify commit count and spot-check key historical commits against the SVN log.
:::

:::info
**Phase 4 - Push and switch over**

- Push the migrated repository to the new remote (GitHub, GitLab, etc.).
- Update CI/CD pipelines, webhook URLs, and deployment scripts to point at Git.
- Archive the SVN repository as read-only - keep it accessible for reference but prevent new commits.
:::

:::success
**Phase 5 - Team onboarding**

- Run a short Git workshop for the team, particularly around the staging area and branching model, which differ significantly from SVN's workflow.
- Agree on a branching strategy (feature branches, trunk-based, etc.) before the first commits land.
:::

_Sources:_ `git-svn` _documentation (_[_git-scm.com/docs/git-svn_](http://git-scm.com/docs/git-svn)_); migration guidance from Atlassian (atlassian.com/git/tutorials/migrating-overview)._