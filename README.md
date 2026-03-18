# dotfiles

Personal dotfiles for macOS.

## What's included

- **nvim** - Neovim configuration
- **opencode** - OpenCode configuration
- **.agents** - Agent skills for OpenCode

## Prerequisites

- [GNU Stow](https://www.gnu.org/software/stow/)

## Installation

```bash
git clone https://github.com/billyhawkes/dotfiles.git
cd dotfiles
stow .
```

## Structure

```
.agents/
└── skills/       # Agent skills for OpenCode
.config/
├── nvim/         # Neovim config
└── opencode/     #OpenCode config
```