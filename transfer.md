### 1. Upload changes to remote

Push your local branch to the remote repository:

```bash
git push -u origin <branch-name>
```

---

### 2. Download a repository

Clone a repository (no need to `git init` before this):

```bash
git clone <repo-url>
```

Clone only the **latest commit** (shallow clone):

```bash
git clone --depth 1 <repo-url>
```

Clone **only a specific branch**:

```bash
git clone --branch <branch-name> --single-branch <repo-url>
```

---

### 3. Get updates from the remote

Fetch all changes and update your remote-tracking branches:

```bash
git fetch --all
```

> **Note:** `git fetch --all` only updates your **knowledge of remote branches**; it does **not** create local branches automatically.

Pull changes and merge them into your current branch:

```bash
git pull --all
```

> **Note:** This updates your local files to match the remote.

---

### 4. Working with remote branches

#### a) See all remote branches

```bash
git fetch origin
git branch -r
```

#### b) Create a local branch tracking a remote branch

```bash
git checkout -b <branch-name> origin/<branch-name>
```

> This creates a new local branch that tracks the remote branch.

#### c) Shortcut (modern Git ≥ 2.23)

```bash
git switch <branch-name>
```

> If the branch exists on the remote but not locally, Git automatically creates a tracking branch for you.

---
