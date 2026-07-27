---
sidebar_position: 14
---

# 󱖫 Show Status (Crystal Ball)

The **Status Dashboard** presents a high-contrast overview of repository state (`bimagic -s`).

### Features

- **Single-Pass Engine**: Renders in **sub-5ms** using a single `git status --porcelain=v2 --branch` execution.
- **Repository Highlights**: Summarizes `GITHUB_USER`, active branch, ahead/behind commit counts (`AHEAD: X | BEHIND: Y`), and repository cleanliness (`🟢 clean`, `🟡 uncommitted`, `🔴 conflicts`).
- **High-Contrast Border**: Displays inside a rounded Unicode box inheriting primary theme colors.
