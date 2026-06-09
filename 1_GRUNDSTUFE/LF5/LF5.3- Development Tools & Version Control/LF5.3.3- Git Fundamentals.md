# LF5.3.3: Git Fundamentals

<details>
<summary>Briefing</summary>

## 👤 User Story

> As a Developer,  
> I want to master the fundamental Git commands,  
> so that I can track my local changes, save snapshots of my work, and push them securely to a remote repository.

## 🎉 Celebration Criteria (Learning Objectives)

- I can **define** the three states of a file in Git (modified, staged, committed). (K1)
- I **know how to execute** the core commands to save changes (`add`, `commit`). (K3)
- I can **synchronize** local code with a remote server (`push`, `pull`). (K3)

## 🧠 Knowledge Briefing

Git operates locally using three "trees" or states. Understanding this flow is crucial.

### The Git Flow

1. **Working Directory (Modified):** You change a file in VSCode. Git notices it's changed, but hasn't saved it yet.
2. **Staging Area (Staged):** You use `git add <file>`. You are preparing the file to be saved in the next snapshot. It's like putting items in a shipping box.
3. **Local Repository (Committed):** You use `git commit -m "Message"`. The box is sealed and stored permanently in your local `.git` folder with a unique ID (hash).

### Syncing with the Cloud (GitHub)

- `git push`: Uploads your local commits to the remote server.
- `git pull`: Downloads new commits from the remote server and merges them into your local files.

## ⚠️ Common Pitfalls

- Forgetting to `git add` before `git commit`. Git will only commit what is in the Staging Area.
- Writing terrible commit messages like "fixed stuff". A commit message should explain _why_ the change was made.

## 🛠️ Mandatory Tasks (K1 - K3)

1. List the three states a file can reside in within local Git (Working Directory, Staging Area, Repository). (K1)
2. Explain the purpose of the "Staging Area" (Index) in Git. (K2)
3. Write down the exact terminal command used to move a file named `index.html` into the Staging Area. (K3)
4. Write down the exact terminal command used to save the staged changes permanently with the message "Add login button". (K3)
5. Describe the functional difference between `git push` and `git pull`. (K2)

## 🔥 Optional Tasks (K4 - K6)

1. Analyze what happens to the local file system if you execute a `git reset --hard` command. (K4)
2. Evaluate the security implications of accidentally committing an API key to a public GitHub repository, even if you delete it in the very next commit. (K5)
3. Design a set of "Commit Message Guidelines" for a new developer team to enforce consistency and readability. (K6)

## 🕸️ Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Git Basics | YouTube | "Git tutorial for beginners" |
| Git Staging Area | Google | "Understanding the Git Staging Area" |

</details>

## Answers

### M1: List the three states a file can reside in within local Git (Working Directory, Staging Area, Repository). (K1)

A file in a local Git setup moves through three distinct states:

1. **Working Directory (modified)** - the file exists on your machine and has been changed, but Git has not been told to do anything with it yet.
2. **Staging Area (staged)** - the file has been registered for the next commit via `git add`. The file is queued up and ready.
3. **Local Repository (committed)** - the staged changes have been confirmed via `git commit` and are now permanently stored in the `.git` folder with a unique identifier (SHA-1 hash).

---

### M2: Explain the purpose of the "Staging Area" (Index) in Git. (K2)

**The Staging Area** - also called the Index - is a deliberate middle step between changing a file and saving it permanently. It lets you decide **exactly which changes go into the next commit**, even if you have modified several files at once.

**Example:** A bug in `login.py` was fixed. But refactoring `database.py` has started, but isn't finished yet. Without the Staging Area, you'd have to commit everything or nothing. With it, you `git add login.py` only, commit that clean fix on its own, and leave the unfinished refactor out of the commit until it's ready.

---

### M3: Write down the exact terminal command used to move a file named `index.html` into the Staging Area. (K3)

`git add index.html`

---

### M4: Write down the exact terminal command used to save the staged changes permanently with the message "Add login button". (K3)

`git commit -m "Add login button"`

---

### M5: Describe the functional difference between `git push` and `git pull`. (K2)

Both commands sync the local repository with a remote server (like GitHub), but in opposite directions:

| Command | Direction | What it does |
| --- | --- | --- |
| `git push` | Local → Remote | Uploads your local commits to the remote repository. |
| `git pull` | Remote → Local | Downloads new commits from the remote and merges them into your local files. |

`git push origin main` (soon outdated and formerly: “master”, now “main”) transfers all commits from the local working copy into the main remote directory, and `git pull` downloads content from the main directory to update the local repository.

---

### O1: Analyze what happens to the local file system if you execute a `git reset --hard` command. (K4)

`git reset --hard` is one of the more destructive commands in Git's toolkit.

A command that **completely deletes** the registered work - as opposed to `--soft`, which merely un-stages changes while keeping the files intact.

In concrete terms, `git reset --hard` does three things simultaneously:

1. **Moves the branch pointer** back to the specified commit (e.g. `HEAD~1` means "one commit ago").
2. **Resets the Staging Area** - anything queued up with `git add` is wiped out.
3. **Overwrites the Working Directory** - your actual files on disk are reverted to match the target commit. Any unsaved changes, any new lines you wrote since that commit, are gone.

:::danger
Critical: unlike most Git operations, this one is **not safely reversible through normal means**. Git's regular safety net - the fact that committed data lives in the object store and can be recovered via `git reflog` - only helps if you had already committed. **Uncommitted work that gets wiped by** `--hard` **has no such safety net.**
:::

**When it is legitimate to use:**

- Discarding a failed experiment you never committed.
- Resetting a CI environment to a clean known state.
- Undoing a bad merge before it gets pushed anywhere.

**When it is dangerous:**

- Any time someone runs it on a shared branch, or when they have uncommitted work they haven't backed up. A common horror story is a developer running `git reset --hard` thinking it only affects the last commit, not realising they had hours of uncommitted work sitting in the Working Directory.

**The rule of thumb:** `git stash` first - it tucks the working directory changes away safely before you do anything drastic.

---

### O2: Evaluate the security implications of accidentally committing an API key to a public GitHub repository, even if you delete it in the very next commit. (K5)

This is a scenario that plays out regularly in real development - and the consequences are more severe and longer-lasting than most people initially assume.

**Why "I deleted it in the next commit" is not enough:**

Git is fundamentally a history-preservation tool. When you add a new commit, the previous commit is not erased - it remains fully intact in the repository's object store. Anyone who clones the repository, or even just browses it on GitHub, can navigate to the previous commit and read the API key in plain text. The deletion commit only affects the _current_ state of the file, not the history.

**How fast attackers move:**

Automated bots continuously scan GitHub for freshly pushed API keys - tokens from AWS, Stripe, Twilio, and dozens of other services. Studies have shown that exposed keys can be discovered and exploited **within minutes** of being pushed. By the time a developer notices the mistake, creates a new commit, and pushes the fix, the window of exposure may already have been sufficient.

**What "deleting" from history actually requires:**

Removing a secret from Git history is not a simple operation. It requires rewriting history using tools like `git filter-repo` or the older `BFG Repo Cleaner`. This produces a new set of commit hashes for every affected commit, which breaks the history for everyone who has cloned the repository and forces a force-push - a disruptive operation on any shared repository.

**The only safe response:**

1. **Revoke the key immediately** - before anything else, log into the service (AWS, GitHub, Stripe, etc.) and invalidate the exposed credential. Assume it has already been seen (_assume breach_).
2. Generate a fresh replacement key.
3. Clean the history with `git filter-repo` and force-push.
4. Notify the team that they need to re-clone.
5. Investigate whether the key was used during the exposure window via the service's access logs.

**The prevention layer:**

This is exactly the scenario that pre-commit secrets-scanning hooks (like `gitleaks` or `git-secrets`) are designed to catch - blocking the commit before the key ever reaches the remote. The fix after the fact is painful; the prevention is a one-time setup.

_Sources: gitguardian.com; docs.github.com._

---

### O3: Design a set of "Commit Message Guidelines" for a new developer team to enforce consistency and readability. (K6)

A commit history is only useful if you can actually read it six months later. These guidelines give a new team a concrete, enforceable baseline.

**The golden rule: explain the** **_why_****, not the _what_.** The diff already shows what changed. The commit message should explain why that change was necessary.

---

**Structure: the 50/72 rule**

```
<type>(<scope>): <short summary>          ← max 50 characters
                                           ← blank line
<optional body, wrapped at 72 characters>
<optional footer: references, breaking changes>
```

---

**Allowed types (Conventional Commits standard):**

| Type | When to use |
| --- | --- |
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only |
| `refactor` | Code restructuring, no behaviour change |
| `test` | Adding or fixing tests |
| `chore` | Tooling, dependencies, CI config |

---

**Concrete examples:**

==Bad:==

```
fixed stuff
```

```
WIP
```

```
asdfgh
```

==Good:==

```
fix(auth): prevent login bypass on empty password input

The bcrypt check was short-circuiting when the password field
was an empty string, returning a false positive match.
Fixes #142.
```

```
feat(dashboard): add export to CSV button

Requested by the sales team for weekly reporting.
Closes #98.
```

---

**Rules to enforce as a team:**

1. **Imperative mood in the summary line** - "Add feature", not "Added feature" or "Adding feature". Read it as: "If applied, this commit will... _add feature_."
2. **No period at the end of the summary line.**
3. **Reference issue numbers** in the footer where relevant (`Fixes #142`, `Closes #98`).
4. **No committing directly to** `main` - commit messages on feature branches, squash or rebase before merging.
5. **No "WIP" commits on shared branches** - use `git stash` or a draft Pull Request instead.

---

**Tooling to back it up:**

- **commitlint** - a pre-commit hook that automatically rejects messages that don't match the Conventional Commits format.
- **CHANGELOG generation** - tools like `standard-version` or `release-please` can auto-generate changelogs directly from well-formed commit messages, making the guidelines pay dividends at release time.

A team that writes good commit messages rarely needs to ask "who broke this and why?" - `git log` or `git blame` gives them the answer in plain English.

_Sources: conventionalcommits.org; cbea.ms/git-commit._