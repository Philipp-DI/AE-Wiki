# LF5.3.4: Branching & Workflows

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a DevOps Engineer,  
> I want to establish a branching strategy,  
> so that I can isolate new features, prevent unfinished code from breaking the main application, and manage team collaboration effectively.

## 🎉 Celebration Criteria (Learning Objectives)

- **I can define** the concept of a branch in Git. (K1)
- **I know how to contrast** different workflow models (Feature Branching vs. Trunk-based). (K2)
- **I can explain** the purpose of a Pull Request (PR) in a team setting. (K2)

## 🧠 Knowledge Briefing

Working directly on the `main` branch with multiple people leads to chaos. We use branches to isolate work.

### What is a Branch?

A parallel version of your repository. You branch off `main`, write your code safely without affecting anyone else, and later merge it back.

### Branching Workflows

- **Feature Branching (e.g., Git Flow):** Every new feature gets its own branch (e.g., `feature/login`). Once done, it is reviewed and merged into `main`. Safer, but merges can be large and complex.
- **Trunk-based Development:** Everyone pushes small, frequent updates directly to `main` (the trunk) multiple times a day. Requires heavy automated testing (CI/CD) to prevent breaking things.

**3\. Pull Requests (PR) / Merge Requests:** A mechanism on GitHub/GitLab to say: "I finished my feature branch. Please review my code before we merge it into the main project."

## ⚠️ Common Pitfalls

- Merge Conflicts. This happens when two people edit the exact same line in a file on two different branches, and Git doesn't know which version to keep during a merge. Humans must resolve this manually.

## 🛠️ Mandatory Tasks (K1 - K3)

1. Define what a "Branch" is in the context of Git. (K1)
2. Describe the basic concept of the "Feature Branch Workflow". (K2)
3. Explain the core philosophy of "Trunk-based Development" regarding commit frequency and branches. (K2)
4. Define what a "Merge Conflict" is and explain why it occurs. (K2)
5. Describe the purpose of a "Pull Request" on platforms like GitHub. (K2)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze why a strict Git Flow model might be too heavy and bureaucratic for a 3-person startup building an MVP. (K4)
2. Evaluate how Trunk-based Development relies on the concept of "Feature Flags" to hide unfinished code deployed to production. (K5)
3. Formulate a step-by-step resolution strategy for a developer facing a complex merge conflict in VSCode. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Git Branching | YouTube | "Git Branching simply explained" |
| Git Workflows | Google | "Feature Branch Workflow vs Trunk Based Development" |
| Merge Conflicts | YouTube | "How to resolve Git Merge Conflicts" |

</details>

## Answers

### M1: Define what a "Branch" is in the context of Git. (K1)

A branch is a **parallel, independent line of development** within a repository. It serves as a separate working environment - you can create a new branch, make changes there, and the `main` branch remains completely untouched until you deliberately merge the two back together.

The HEAD pointer - an index pointing to the last active commit in the current working environment, moves along with whichever branch you are currently on.

**Analogy:**  
The main branch is the published edition of a book. A branch is your personal draft copy where you can rewrite a chapter freely. The published edition stays on the shelf unchanged until an editor reviews your draft and decides to incorporate it.

---

### M2: Describe the basic concept of the "Feature Branch Workflow". (K2)

In the Feature Branch Workflow, **every new feature gets its own dedicated branch**, forked off from `main`. The developer works on that branch in isolation - committing freely, experimenting, breaking things and fixing them - without any of that affecting the stable codebase.

A typical lifecycle looks like this:

1. **Branch off** `main`: `git branch feature/login`
2. **Switch to it:** `git checkout feature/login`
3. **Develop and commit** on the feature branch.
4. Once complete, open a **Pull Request** for review.
5. After approval, **merge back** into `main`: `git checkout main` → `git merge feature/login`
6. **Delete** the now-redundant branch: `git branch -d feature/login`

The key principle is that `main` only ever receives finished, reviewed work.

---

### M3: Explain the core philosophy of "Trunk-based Development" regarding commit frequency and branches. (K2)

Trunk-based Development flips the Feature Branch model on its head. Instead of long-lived feature branches, **every developer commits small, frequent changes directly to** `main` - the "trunk" - multiple times a day.

The philosophy is built on two convictions:

- **Long-lived branches are the enemy.** The longer a branch drifts from `main`, the more painful the eventual merge becomes. Small, frequent integrations keep the divergence minimal.
- **The test suite is the safety net.** Because everyone is pushing to `main` constantly, a strong automated CI/CD pipeline is non-negotiable. If a commit breaks something, the pipeline catches it within minutes.

For features that are not yet ready to be visible to users, Trunk-based Development relies on **Feature Flags** - see **O2** below.

---

### M4: Define what a "Merge Conflict" is and explain why it occurs. (K2)

A Merge Conflict is a situation where Git **cannot automatically reconcile differences** between two branches and requires a human to decide what the final version should look like.

It occurs specifically when two developers have edited **the exact same line or region of the same file** on different branches. When those branches are merged, Git finds two competing versions of that section and has no logical way to choose between them - so it flags the conflict, marks the affected sections in the file, and halts until a developer resolves it manually.

This is a natural consequence of parallel development - the more developers work on the same files over longer periods, the more likely conflicts become.

**What a conflict looks like in the file:**

```
<<<<<<< HEAD
button.color = "blue"
=======
button.color = "green"
>>>>>>> feature/new-design
```

Everything between `<<<<<<<` and `=======` is your version; everything between `=======` and `>>>>>>>` is the incoming branch's version. You pick one, delete the markers, and commit.

---

### M5: Describe the purpose of a "Pull Request" on platforms like GitHub. (K2)

A **Pull Request (PR)** is a formal mechanism for saying: **"I have finished work on my feature branch - please review it before it is merged into main."**

It is not a Git feature itself, but a collaboration layer added by platforms like GitHub or GitLab on top of Git. A PR typically shows:

- A diff of every change the branch introduces.
- A space for reviewers to leave comments on specific lines.
- A status check showing whether the automated tests passed.
- A merge button that only becomes available once the required reviewers have approved.

The PR process enforces a **four-eyes principle** - no code reaches `main` without at least one other person having seen it. This catches bugs, enforces coding standards, and spreads knowledge about changes across the team.

---

### O1: Analyze why a strict Git Flow model might be too heavy and bureaucratic for a 3-person startup building an MVP. (K4)

Git Flow, popularised by Vincent Driessen in 2010, defines a rigid set of long-lived branches: `main`, `develop`, `feature/*`, `release/*`, and `hotfix/*`. Each has a defined purpose and a prescribed merge path. For a large team managing a versioned, installed product it makes a lot of sense. For a 3-person startup it is frequently overkill.

**Where the friction comes from:**

- **Cognitive overhead.** With 3 people, half the daily conversation becomes "wait, should this go into `develop` or directly into `release/1.2`?" The branching rules consume mental energy that a tiny team needs for building.
- **Slow feedback loops.** In Git Flow, features land on `develop` first, then get bundled into a `release` branch, then finally hit `main`. For an MVP where the product changes dramatically every week, that pipeline introduces unnecessary delay between writing code and seeing it in production.
- **Merge ceremony for every change.** A hotfix in Git Flow requires branching off `main`, fixing, merging back into _both_ `main` and `develop`, and tagging the release. Three people can just talk to each other instead.
- **Implicit assumption of multiple parallel versions.** Git Flow shines when you need to maintain version 1.x while developing version 2.x simultaneously. A startup building its first product has exactly one version - the next one.

**What works better:**

For a small team moving fast, a lightweight Feature Branch model or even Trunk-based Development with feature flags is typically a much better fit. The principle should be: adopt the minimum process that prevents stepping on each other's work, and no more. Bureaucracy has a real cost in a startup context.

_Sources: nvie.com; atlassian.com/git/tutorials/comparing-workflows_

---

### O2: Evaluate how Trunk-based Development relies on the concept of "Feature Flags" to hide unfinished code deployed to production. (K5)

This is one of the more elegant ideas in modern software delivery, and it resolves an apparent contradiction: how can you commit half-finished code to `main` multiple times a day without breaking what users see?

**The contradiction:**

Trunk-based Development requires constant integration into `main`. But features take days or weeks to build. If you commit an unfinished checkout flow on Monday, users on Tuesday see a broken half-built page.

**What Feature Flags do:**

A Feature Flag (also called a Feature Toggle) is simply an `if` statement wrapped around new code, controlled by a configuration value rather than hardcoded in the source:

```python
if feature_flags.is_enabled("new_checkout_flow", user):
    show_new_checkout()
else:
    show_old_checkout()
```

The flag value is stored in a config file, environment variable, or a dedicated feature flag service (LaunchDarkly, Unleash, etc.). In production, the flag is `off` by default. The unfinished code is deployed - it exists in the binary - but users never hit it.

**Why this is powerful:**

- Developers can merge freely to `main` without gating on feature completion.
- The flag can be turned on for internal testers or a specific percentage of users before full rollout - a technique called **canary releasing**.
- If a newly released feature causes problems, flipping the flag off is a **rollback that takes seconds**, with no redeployment needed.
- Long-lived feature branches and their painful merges are avoided entirely.

**The trade-offs:**

Feature Flags introduce their own complexity. Flags accumulate over time - a codebase with dozens of stale flags becomes harder to reason about. Teams need a discipline of **removing flags** once a feature is fully released, or the code becomes riddled with conditional branches that nobody dares to touch. At its worst, a poorly managed flag system is just a different kind of technical debt.

**The honest evaluation:** Feature Flags are a genuine enabler of Trunk-based Development at scale, but they work best when treated as temporary scaffolding - put up deliberately, taken down promptly.

_Sources: martinfowler.com/articles/feature-toggles.html; launchdarkly.com/blog/what-are-feature-flags_

---

### O3: Formulate a step-by-step resolution strategy for a developer facing a complex merge conflict in VSCode. (K6)

Merge conflicts feel alarming the first time, but they follow a predictable pattern and VSCode provides solid tooling to work through them without touching the raw conflict markers directly.

---

**Step 1 - Don't panic, understand the situation first**

Before touching anything, run:

```bash
git status
```

This lists every file with a conflict. Read the list fully before editing anything - understanding the scope prevents making things worse.

---

**Step 2 - Open the Merge Editor in VSCode**

VSCode detects conflict markers automatically and offers an **"Open in Merge Editor"** button when you open a conflicted file. This splits the view into three panes:

- **Incoming** (the branch being merged in) - left pane.
- **Current** (your branch, HEAD) - right pane.
- **Result** (what the file will look like after resolution) - bottom pane.

This is much safer than editing raw `<<<<<<<` markers by hand, where one misplaced deletion breaks the file silently.

---

**Step 3 - Resolve conflict by conflict, not file by file**

VSCode highlights each conflict block individually. For each one, choose one of the available actions:

- **"Accept Current"** - keep your version.
- **"Accept Incoming"** - take the other branch's version.
- **"Accept Both"** - keep both, one after the other.
- **Edit the Result pane directly** - for complex cases where neither version is fully correct and you need to write a third, combined solution.

Work through every conflict in the file before moving to the next one.

---

**Step 4 - Verify the result makes logical sense**

Once all markers are resolved, read the **Result pane** as a whole. A file with no conflict markers can still be logically broken - two developers may have added different functions that both call the same variable name, for example. The merge editor resolves syntax conflicts; the developer must verify logical correctness.

---

**Step 5 - Stage the resolved file**

```bash
git add <filename>
```

Staging the file tells Git the conflict in that file has been resolved. Do this for every conflicted file.

---

**Step 6 - Complete the merge**

Once all conflicts are staged:

```bash
git commit
```

Git will pre-populate the commit message with a standard merge message. Add context if the resolution was non-trivial - a future colleague will thank you.

---

**Step 7 - Run the test suite**

Before pushing, run the full test suite. A clean merge with no conflict markers is not the same as a correct merge. Tests are the final verification that the combined result actually works.

---

**General principles for avoiding the situation next time:**

- Merge or rebase from `main` into your feature branch **frequently** - small, regular syncs produce small, manageable conflicts.
- Keep Pull Requests short-lived and focused. A branch that touches 40 files over 3 weeks will always produce worse conflicts than one that touches 5 files over 2 days.
- Communicate with teammates when working on the same module - a quick message prevents the conflict entirely.

_Sources: code.visualstudio.com/docs/sourcecontrol/overview; git-scm.com/docs/git-merge._