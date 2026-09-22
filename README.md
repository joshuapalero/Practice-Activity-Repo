# Practice Activity Repository.

Interactive practice modules, cheat sheets, and command documentation.

## 01 - Master Git by Reading Manuals
### Configure Global User Identity
Establishes your author identity recorded permanently into every commit object SHA you create.
```bash
git config --global user.name "Joshua Maddie"
git config --global user.email "joshuamaddie@gmail.com"
```

### Check Out Hotfix Branch in Parallel Directory (Git Worktree)
Allows working on an urgent bug on a different branch simultaneously without stashing or disrupting your current build.
```bash
git worktree add ../hotfix-folder hotfix/login-crash
git worktree list
git worktree remove ../hotfix-folder
```

### Binary Search to Find the Exact Commit that Introduced a Bug
Automates binary search through commit history to identify the exact regression commit in O(log n) steps.
```bash
git bisect start
git bisect bad
git bisect good v1.0.0
git bisect good
git bisect reset
```

### Transplant a Single Specific Commit onto Current Branch
Applies the exact changes introduced by a specific commit from another branch onto your active branch.
```bash
git cherry-pick <commit-hash>
