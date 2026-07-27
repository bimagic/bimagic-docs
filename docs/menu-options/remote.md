---
sidebar_position: 13
---

#  Set Remote

Configure remote repository URLs (`origin` or custom remotes) with built-in authentication guidance.

### Features

- **Protocol Chooser**: Switch between **HTTPS (Token)** and **SSH** (`git@github.com:user/repo.git`).
- **Token Integration**: Automatically constructs authenticated HTTPS URLs using your `GITHUB_USER` and `GITHUB_TOKEN` environment variables.
- **Safety Confirmation**: Shows the full formatted remote URL before applying changes.
