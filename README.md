# Bimagic Documentation 🔮✨

Welcome to the official documentation repository for **Bimagic**, the interactive Git companion. This website provides comprehensive guides, installation tutorials, and spell references for both **Bimagic Go Edition (`bimagic-go` v2.0.0)** (Recommended) and the classic **Bimagic Shell Edition**.

Built with [Docusaurus 3](https://docusaurus.io/), this site is optimized for ultra-fast performance, accessibility, and an intuitive developer experience.

## 🌐 Live Site

Check out the live documentation at: **[https://bimagic.vercel.app](https://bimagic.vercel.app)**

---

## 🔮 What's Documented

This site covers full documentation for Bimagic v2.0.0:

- **🚀 Installation Guides**: Automated one-liner (`curl`), Go `go install`, native **Windows Installation (`bimagic.exe`)**, npm, and manual build workflows.
- **🎹 Shell & Editor Integrations**: Zsh, Bash, and Fish keybindings (**Ctrl + B**), Neovim `toggleterm` floating popups, and the `wz` shortcut symlink.
- **🎨 Theme Customization**: Custom color palettes via `~/.config/bimagic/theme.wz` and automatic wallpaper color syncing via **Matugen**.
- **📜 Complete Spellbook (24 Interactive Operations)**:
  - `clone` - Standard & Interactive Sparse Checkouts
  - `init` - Rapid setup with guaranteed `main` default
  - `unstage` - Interactive file unstaging (`git restore --staged`) *(Go Edition)*
  - `discard` - Safe local modification discarding (`git checkout --`) *(Go Edition)*
  - `commit` - Magic Commit Builder (Conventional) & Quick Commit
  - `push` & `pull` - Remote synchronization & upstream auto-tracking
  - `branch` - Switch, create, rename (`-m`), and delete (`-d`/`-D`) branches
  - `tag` - Complete tag lifecycle (create, list, push, delete local & remote tags) *(Go Edition)*
  - `diff` - Unstaged, staged, file, and branch comparison diffs *(Go Edition)*
  - `cherry` - Search and pluck specific commits onto current branch *(Go Edition)*
  - `remote` - Set HTTPS token or SSH remotes
  - `status` - Single-pass porcelain v2 status dashboard (<5ms latency)
  - `contributor-stats` - Per-author contribution activity (lines, commits, highlights)
  - `git-graph` - Pretty git log tree visualization
  - `architect` - Interactive `.gitignore` generator with 70+ blueprints
  - `file-removal` - Safe `git rm` file/folder deletion
  - `merge` & `uninitialize` - Branch merging & Git untracking
  - `resurrection` - Reflog recovery for lost commits/branches
  - `revert` & `undo` - Multi-select commit revert & Time Turner undo
  - `stash` - Stash push, pop, list, apply, drop, clear
  - `scrying` - Quick file browser with `fzf` side-by-side preview & `bat` syntax highlighting

---

## 🚀 Local Development

### Prerequisites
- [Node.js](https://nodejs.org/) (version 18 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Installation
Clone the repository and install dependencies:

```bash
git clone https://github.com/bimagic/bimagic-docs.git
cd bimagic-docs
npm install
```

### Start Development Server

```bash
npm run start
```
This starts a local development server at `http://localhost:3000` with live hot-reloading.

---

## 🛠️ Build & Deployment

### Production Build
Generate a static production build:

```bash
npm run build
```
The static HTML/CSS/JS assets will be generated in the `build/` directory.

### Preview Build Locally
```bash
npm run serve
```

---

## 📂 Repository Structure

```text
.
├── blog/                 # Announcements & release notes
├── docs/                 # Documentation MDX source files
│   ├── menu-options/     # Detailed guides for all 24 spell operations
│   ├── configuration.md  # PAT, Theme, & Matugen configuration
│   ├── installation.md   # Linux, macOS, Windows & Go setup
│   ├── intro.md          # Overview & feature matrix
│   ├── usage.md          # CLI flags & status dashboard
│   ├── troubleshooting.md
│   └── uninstallation.md
├── src/                  # Custom React components & pages
├── static/               # Assets (logos, images, screenshots)
├── docusaurus.config.js  # Main site configuration
└── sidebars.js           # Navigation sidebar configuration
```

---

## 🤝 Contributing

We welcome contributions to improve the documentation!

1. **Fork** the repository: `github.com/bimagic/bimagic-docs`.
2. **Create** a feature branch: `git checkout -b docs/my-new-guide`.
3. **Commit** your changes cleanly.
4. **Push** and submit a **Pull Request**.

---

## 📄 License

This project is open-source under the **MIT License**. Built with ❤️ by [Bimbok](https://github.com/bimbok) and [adityapaul26](https://github.com/adityapaul26).
