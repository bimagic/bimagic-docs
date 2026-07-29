---
sidebar_position: 15
---

# Conflict Resolution Assistant

The **Conflict Resolution Assistant** provides a streamlined 1-click interface to resolve merge or rebase conflicts when status shows `󰅖 conflicts`.

### Features

1. **Auto Detection**: Scans and lists all conflicted files in the working tree.
2. **1-Click Resolution**:
   - **Accept Ours (`--ours`)**: Keep current branch version and auto-stage.
   - **Accept Theirs (`--theirs`)**: Keep incoming branch version and auto-stage.
   - **Manual Edit**: Launch `$EDITOR` (Neovim / Vim / Nano) to resolve `<<<<<<<` markers manually.
3. **Auto Complete**: Detects when all conflicts are resolved and prompts to finalize the merge commit.

**CLI Keymap**: `wz -x` / `wz --conflicts`
