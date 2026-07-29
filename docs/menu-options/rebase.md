---
sidebar_position: 14
---

# Interactive Rebase & Squash

The **Rebase & Squash Wizard** allows power users to clean up commit histories, squash draft commits, or rebase branches.

### Quick Squash (Combine last N commits into 1)

Combines the last `N` commits into a single clean commit with a custom commit message:
1. Prompts for the number of commits to combine (`N`).
2. Performs a soft reset (`git reset --soft HEAD~N`).
3. Prompts for the new squashed commit message and commits.

**CLI Keymap**: `wz -K` / `wz --rebase`

### Interactive Rebase

Launches standard interactive rebase (`git rebase -i HEAD~N`) in your terminal editor.

### Rebase onto Target Branch

Rebases the current branch onto any target branch (e.g. `main` / `dev`).
