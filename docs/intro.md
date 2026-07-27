---
sidebar_position: 1
---

# Introduction

<p align="center">
  <img width="400" style={{borderRadius: '12px'}} alt="Bimagic Logo" src="/img/logo_1.png" />
</p>

<p align="center">By Bimbok and adityapaul26</p>

A powerful interactive Git automation wizard that simplifies your GitHub workflow with an interactive menu system.

:::tip Recommended Edition: Bimagic Go (v2.0.0)
We strongly recommend using **Bimagic Go Edition (`bimagic-go`)**! Rebuilt from the ground up in Go, it features **sub-5ms multi-threaded performance**, native **Windows (`bimagic.exe`)** support, shortcut symlink (`wz`), Nerd Font icons, and new spells (Unstage, Discard, Tag Operations, Diff Wizard, Cherry-Pick). 

*The classic Bash script version remains supported for Unix environments.*
:::

## Overview

Bimagic is an interactive command-line tool that streamlines common Git operations, making version control more accessible through a user-friendly menu interface. It handles repository initialization, committing, branching, tag management, diff inspection, cherry-picking, stash operations, reflog recovery, and interactive sparse checkouts with GitHub integration using personal access tokens or SSH.

## Sample

<img width="800" style={{borderRadius: '12px'}} alt="Interactive Menu" src="/img/1.png" />
<p align="center">Interactive magic spell menu with custom theme styling</p>

<img width="800" style={{borderRadius: '12px'}} alt="Confirmation Dialog" src="/img/2.png" />
<p align="center">Interactive confirmation dialog with dynamic button themes</p>

## Features

### ⚡ Go Engine Highlights (Recommended Edition)

- **Multi-Threaded Speed Engine**: 5ms execution latency using Go parallelism (`runtime.GOMAXPROCS` & single-pass `git status --porcelain=v2 --branch`).
- **Native Windows Support**: Runs natively on Windows (`bimagic.exe`), macOS, and Linux without needing WSL.
- **Shortcut Symlink (`wz`)**: Automatically provisions `wz -> bimagic` shortcut symlinks during installation.
- **Nerd Font Icons**: Clean modern terminal UI aesthetics.

### Core Operations

- **Interactive Interface**: Intuitive menu-driven command-line experience with Charm's `gum`.
- **Commit Management**: Streamlined staging, committing, and undoing ("Time Turner") with multi-select revert support.
- **Unstage Files**: Interactive multi-select unstaging (`git restore --staged`).
- **Discard Local Modifications**: Safe interactive discard of unstaged edits (`git checkout --`).
- **Tag Mastery**: Complete tag lifecycle (create annotated/lightweight, list, push, delete local & remote tags).
- **Diff & Inspection Wizard**: Interactive viewer for unstaged diffs, staged diffs, file diffs, and branch comparisons.
- **Cherry-Pick Wizard**: Select and apply commits onto current branch with conflict resolution.
- **Branching & Merging**: Simplified branch management (switch, create, rename `-m`, delete `-d`/`-D`) and merging with automated conflict detection.
- **Stash Management**: Full support for stash operations including push, pop, list, apply, drop, and clear.
- **Shallow Clone Support**: Use `--depth` for lightweight clones.
- **Resurrection Stone**: Recover lost commits/branches from reflog.

### Repository Management

- **Secure Integration**: GitHub authentication via personal access tokens or SSH.
- **Automated Initialization**: Rapid setup and repository initialization with guaranteed `main` branch default.
- **Smart Cloning**: Support for both standard and interactive sparse checkout selection (`--filter=blob:none`).
- **The Architect**: Integrated `.gitignore` generator for professional project setup with 70+ blueprints.
- **Safety**: Automated `master`-to-`main` branch renaming and safe file removal with Git integration.

### Analysis & Visualization

- **Status Dashboard**: Real-time overview of branch status, ahead/behind counts, and uncommitted changes in a high-contrast rounded box.
- **Visual Commit Graph**: High-quality "pretty git log" for clear history visualization.
- **Contributor Stats**: Detailed project contribution insights with custom time-range filtering.
- **The Scrying Glass**: Scrollable file browser with `fzf` side-by-side preview and `bat` syntax highlighting.
- **Theming**: Dynamic themed progress bar for cloning.

### Customization

- **Theming Engine**: Full UI customization with support for ANSI and Hex color codes via `~/.config/bimagic/theme.wz`.
- **Matugen Integration**: Automatic Material You wallpaper color syncing.
