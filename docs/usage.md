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

### Command Line Flags

You can use flags to perform specific actions immediately:

- **Clone Repository**:
  ```bash
  bimagic -d "repo-url"
  ```
- **Shallow Clone**:
  ```bash
  bimagic -d "repo-url" --depth 1
  ```
- **Interactive Clone** (Select specific files/folders to download):
  ```bash
  bimagic -d -i "repo-url"
  ```
- **The Lazy Wizard** (Add + Commit + Push; auto-amends if clean):
  ```bash
  bimagic -z "commit message"
  ```
- **The Crystal Ball** (Show Status Dashboard):
  ```bash
  bimagic -s
  ```
- **The Time Scroll** (Show Git Graph):
  ```bash
  bimagic -g
  ```
- **The Time Turner** (Undo last commit):
  ```bash
  bimagic -u
  ```
- **The Architect** (Summon .gitignore):
  ```bash
  bimagic -a
  ```
- **Pull Latest Changes**:
  ```bash
  bimagic -p
  ```
- **Tag Operations** *(Go Edition)*:
  ```bash
  bimagic -t
  ```
- **Diff & Inspection Wizard** *(Go Edition)*:
  ```bash
  bimagic --diff
  ```

### Status Dashboard

At the top of the interface, a prominent rounded status box summarizes:

- Current `GITHUB_USER` and active branch
- Ahead/behind counts relative to upstream (`AHEAD: X | BEHIND: Y`)
- Working tree state: `🟢 clean`, `🟡 uncommitted`, or `🔴 conflicts`

*In Bimagic Go Edition, this dashboard renders in **<5ms** via single-pass porcelain v2 execution.*
