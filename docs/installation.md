---
sidebar_position: 2
---

# Installation

:::tip Recommended: Bimagic Go Edition (v2.0.0)
For sub-5ms rendering speed, multi-core CPU performance, native Windows support (`bimagic.exe`), and the `wz` shortcut alias, install **Bimagic Go Edition**. The classic Bash script version remains fully supported.
:::

## 🚀 Installing Bimagic Go Edition (Recommended)

### Automated One-Liner (Linux & macOS)

Run this one-line command to install Bimagic Go:

```bash
curl -fsSL https://raw.githubusercontent.com/bimagic/bimagic-go/main/install.sh | bash
```

*(Use `--system` flag to install into `/usr/local/bin` for all users, or default to `~/.local/bin` without root).*

### Via Go (`go install`)

If you have Go installed:

```bash
go install github.com/bimagic/bimagic-go@latest
```

### Windows Installation Guide 🪟

Bimagic runs natively on Windows 10/11 inside **Windows Terminal**, **PowerShell**, **Command Prompt**, or **Git Bash** without requiring WSL.

1. **Install `gum`** in PowerShell:
   ```powershell
   winget install charmbracelet.gum
   ```
2. **Download `bimagic.exe`** from [GitHub Releases](https://github.com/bimagic/bimagic-go/releases) or build via Go (`go build -ldflags="-s -w" -o bimagic.exe main.go`).
3. **Add to PATH & Configure PowerShell Alias (`wz`)**:
   Place `bimagic.exe` in `%USERPROFILE%\bin` and append to your `$PROFILE`:
   ```powershell
   Set-Alias wz bimagic.exe
   Set-PSReadLineKeyHandler -Key "Ctrl+b" -ScriptBlock {
       [Microsoft.PowerShell.PSConsoleReadLine]::Insert("wz")
       [Microsoft.PowerShell.PSConsoleReadLine]::AcceptLine()
   }
   ```

### Manual Build from Source (Go)

```bash
git clone https://github.com/bimagic/bimagic-go.git
cd bimagic-go
go build -ldflags="-s -w" -o bimagic main.go

# Install to ~/.local/bin and create shortcut symlink:
mkdir -p ~/.local/bin
mv bimagic ~/.local/bin/
ln -sf ~/.local/bin/bimagic ~/.local/bin/wz
```

---

## 🐚 Installing Bimagic Shell Edition (Classic Bash)

### Automated Installation (Shell)

Run this one-line command to install the classic Bash edition of Bimagic:

```bash
curl -sSL https://raw.githubusercontent.com/orion-kernel/bimagic/main/install.sh | bash
```

### Installation using npm

You can also install the classic **bimagic** shell tool using npm:

```bash
npm i -g bimagic
```

### Manual Installation (Shell)

1. Clone the repository:
```bash
git clone https://github.com/orion-kernel/bimagic.git
```

2. Make the script executable:
```bash
chmod +x bimagic/bimagic
```

3. Move it to your bin directory:
```bash
# Option 1: For user-local installation (no sudo required)
mkdir -p ~/bin
mv bimagic/bimagic ~/bin/

# Option 2: For system-wide installation (requires sudo)
sudo mv bimagic/bimagic /usr/local/bin/
```

4. Ensure the bin directory is in your PATH:
```bash
export PATH="$HOME/bin:$PATH"  # For user-local installation
```

---

## 🎹 Integrations & Shortcuts

### Quick Access (Keybinding)

The installer automatically configures a **Ctrl + B** keybinding for **Zsh**, **Bash**, and **Fish** shells. This allows you to summon the Git Wizard (`wz` / `bimagic`) from anywhere in your terminal instantly!

- **Zsh**: Uses a custom ZLE widget to ensure a clean UI transition.
- **Bash**: Uses `bind -x` for direct execution.
- **Fish**: Uses `bind \cb` with a repaint command.

:::tip Terminal Restart Required
You may need to restart your terminal or source your config file (e.g., `source ~/.zshrc`) after installation for the keybinding to take effect.
:::

### Neovim Integration

You can use Bimagic directly inside Neovim! This integration wraps the CLI tool in a floating terminal window using `toggleterm.nvim` for a seamless workflow.

#### LazyVim / Toggleterm Setup

Create a new plugin file (e.g., `~/.config/nvim/lua/plugins/bimagic.lua`) with the following configuration. This sets up a `<leader>gm` keybinding to launch the wizard in a floating popup.

```lua
return {
  {
    "akinsho/toggleterm.nvim",
    opts = function(_, opts)
      opts.size = 20
      opts.open_mapping = [[<c-\>]]
    end,
    keys = {
      {
        "<leader>gm",
        function()
          local Terminal = require("toggleterm.terminal").Terminal
          local bimagic = Terminal:new({
            cmd = "wz", -- Uses 'wz' or 'bimagic' in global PATH
            hidden = true,
            direction = "float",
            float_opts = {
              border = "curved", -- 'single', 'double', 'shadow', 'curved'
              width = 100,
              height = 25,
              title = "  Bimagic Git Wizard ",
            },
            close_on_exit = true,

            on_open = function(term)
              vim.cmd("startinsert!")
              vim.api.nvim_buf_set_keymap(term.bufnr, "n", "q", "<cmd>close<CR>", { noremap = true, silent = true })
            end,
          })
          bimagic:toggle()
        end,
        desc = "Bimagic (Git Wizard)",
      },
    },
  },
}
```

### Dependencies

- **gum** (required for modern UI and interactive selection)
  - Automatically installed by `install.sh` on supported Linux/macOS package managers or via `winget install charmbracelet.gum` on Windows.
- **Git** (required)
- **Node.js** v16+ & **npm** v8+ (only if installing shell edition via npm)
