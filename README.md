# Git Workflow Guidelines

## 1. Update Your Branch After Every PR Merge
After a Pull Request is merged into the main development branch (`develop` for LMS), update your local branch with the latest code.

```bash
git fetch
```

```bash
git pull origin develop
```

---

## 2. If You Have Uncommitted Changes Before Pulling

If you have local changes that are **not committed**, stash them before pulling the latest code.

```bash
git stash
git pull origin develop
git stash apply
```

This will:

1. Temporarily save your local changes
2. Pull the latest updates from the `develop` branch
3. Re-apply your saved changes

---

## 3. Save Uncommitted Changes (Stash)

If you need to temporarily save your changes without committing:

**Save changes**

```bash
git stash
```

**Apply saved changes**

```bash
git stash apply
```

---

## 4. Create and Move to a New Branch

```bash
git checkout -b <branch-name>
```

Example:

```bash
git checkout -b feature-login-page
```

---

## 5. Switch to an Existing Branch

```bash
git checkout <branch-name>
```

---

## 6. Push Your Code

**Stage changes**

```bash
git add .
```

**Commit changes**

```bash
git commit -m "commit message"
```

**Push code and set upstream branch**

```bash
git push -u origin <branch-name>
```

---

## Example Full Flow

```bash
git checkout -b feature-dashboard
git add .
git commit -m "Add dashboard UI"
git push -u origin feature-dashboard
```

---

## Branch Naming Convention system :

```

feature/<feature-name>
fix/<bug-name>
refactor/<component>

```

Example:

```

feature/dashboard-ui
fix/login-validation

```
