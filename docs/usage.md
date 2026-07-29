---
sidebar_position: 4
---

# Usage

Simply run the `bimagic` command or the `wz` shortcut in your terminal:

```bash
wz
# OR
bimagic
```

:::tip Quick Access
- Press **Ctrl + B** in your terminal to quickly summon the wizard from anywhere!
- You can use the short alias **`wz`** (Wizard) for even faster access!
:::

### Command Line Flags (Power User Direct Keymaps)

Power users can bypass the interactive menu by using direct keymap flags:

| Keymap Flag | Operation Description |
| :--- | :--- |
| `wz -d [url] [-i]` | **Clone Repository** (optional `-i` for interactive sparse checkout) |
| `wz -I` / `wz --init` | **Init New Repo** (guaranteed `main` branch default) |
| `wz -A` / `wz --add` | **Add / Stage Files** interactively |
| `wz -U` / `wz --unstage` | **Unstage Files** (`git restore --staged`) |
| `wz -X` / `wz --discard` | **Discard Local Modifications** (`git checkout --`) |
| `wz -c` / `wz --commit` | **Magic Commit Builder** (Conventional Commits specification) |
| `wz -P` / `wz --push` | **Push to Remote** (auto-configures upstream tracking) |
| `wz -p` / `wz --pull` | **Pull Latest Changes** from remote |
| `wz -b` / `wz --branch` | **Branch Operations** (switch, create, rename `-m`, delete `-d`/`-D`) |
| `wz -t` / `wz --tag` | **Tag Operations** (create, list, push, delete local & remote tags) |
| `wz -D` / `wz --diff` | **Diff & Inspection Wizard** (unstaged, staged, file, branch diffs) |
| `wz -C` / `wz --cherry` | **Cherry-Pick Wizard** (pluck commits onto current branch) |
| `wz -r` / `wz --remote` | **Set Remote** (configure HTTPS token or SSH remotes) |
| `wz -s` / `wz --status` | **Status Dashboard** (sub-5ms single-pass execution) |
| `wz -S` / `wz --stats` | **Contributor Statistics** (activity highlights & numstat analysis) |
| `wz -g` / `wz --graph` | **Git Graph** (pretty git log tree view) |
| `wz -a` / `wz --architect` | **Summon the Architect** (.gitignore generator with 70+ blueprints) |
| `wz -R` / `wz --remove` | **Remove Files/Folders** (safe `git rm` integration) |
| `wz -m` / `wz --merge` | **Merge Branches** (with conflict detection) |
| `wz --uninit` | **Uninitialize Repo** (remove `.git` tracking) |
| `wz -k` / `wz --resurrect` | **Resurrection Stone** (recover lost commits from reflog) |
| `wz -v` / `wz --revert` | **Revert Commit(s)** (multi-select revert) |
| `wz -w` / `wz --stash` | **Stash Operations** (push, pop, list, apply, drop, clear) |
| `wz -q` / `wz --quickview` | **The Scrying Glass** (instant file browser with `fzf` & `bat`) |
| `wz -u` / `wz --undo` | **Time Turner** (undo last commit: soft, mixed, hard) |
| `wz -z "message"` | **The Lazy Wizard** (Add + Commit + Push fast track) |
| `wz -h` / `wz --help` | **Show Direct Keymaps Help Menu** |

### Status Dashboard

At the top of the interface, a prominent rounded status box summarizes:

- Current `GITHUB_USER` and active branch
- Ahead/behind counts relative to upstream (`AHEAD: X | BEHIND: Y`)
- Working tree state: `🟢 clean`, `🟡 uncommitted`, or `🔴 conflicts`

*In Bimagic Go Edition, this dashboard renders in **sub-5ms** via single-pass porcelain v2 execution.*
