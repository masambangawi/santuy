# Maintainer Release & Identity Isolation Guide

This internal playbook outlines the strict identity isolation practices enforced for maintainers of the `skill-santuy` project.

---

## Clean-Room Identity Invariant

The project maintainer and repository owner is **`masambangawi`**. Under no circumstances should any primary or private maintainer identity leak into public commits, issue comments, or release artifacts.

### 1. Isolated GitHub CLI Environment

Never rely on global `gh auth switch`. Always isolate the GitHub CLI configuration:

```bash
export GH_CONFIG_DIR=/tmp/gh_isolated_masamba
gh auth status
# Verify that gh api user returns strictly masambangawi:
gh api user --jq .login  # Must output: masambangawi
```

---

## 2. Git Author & Committer Isolation

Before committing to this repository, configure git locally with the dedicated GitHub noreply email address:

```bash
git config --local user.name "masambangawi"
git config --local user.email "178961665+masambangawi@users.noreply.github.com"
git config --local commit.gpgsign false
git config --local user.useConfigOnly true
```

Verify the active committer identity prior to each commit:

```bash
git var GIT_AUTHOR_IDENT
git var GIT_COMMITTER_IDENT
```

Both must show `masambangawi <178961665+masambangawi@users.noreply.github.com>`.

---

## 3. Pre-Push Verification Checklist

Run these checks before pushing changes to GitHub:

1. **Commit History Audit**:
   ```bash
   git log -n 5 --format=fuller
   ```
   Confirm that author and committer emails match the noreply address.

2. **Absence of Personal Path Leaks**:
   ```bash
   git grep -i -E "developer_identity|/home/user"
   ```
   Must return zero occurrences across all tracked files.

3. **Remote Target Verification**:
   ```bash
   git remote -v
   ```
   Must point strictly to `https://github.com/masambangawi/santuy.git`.
