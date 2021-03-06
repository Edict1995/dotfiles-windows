# My Dotfiles for Windows

See also: `github.com/ReeceRGGIL/dotfiles`

## Installation using git-bash

1. `alias config='git --git-dir=$HOME/.cfg/ --work-tree=$HOME'`
2. `git clone --bare git@github.com:ReeceRGGIL/dotfiles-windows.git $HOME/.cfg`
3. `config checkout`
4. `config config --local status.showUntrackedFiles no`

### Neovim Setup

1. Run the `install-vim-plug.ps1` powershell script.
2. Install nodejs: `choco install nodejs.install`
3. Install fzf: `choco install fzf`
4. Install ripgrep: `choco install ripgrep`
5. Set the fzf default command: `setx FZF_DEFAULT_COMMAND "rg --files --ignore-case --color auto --hidden --follow --glob \"!.git/*\""
6. Run `PlugInstall` in neovim
7. Create a shortcut that starts in the home directory.

## Dotfiles

- .bash_aliases: Commands aliases are listed in this file. This file is sourced by .bashrc
- .bash_logout: Executed by bash when login shell exits
- .bash_profile: Executed for login shells (at login)
- .bashrc: Executed for interactive non-login shells (running a terminal emulator)
- .gitconfig: Git configuration
- .gitignore: Global git ignore
- .inputrc: GNU Readline configuration file
- Appdata\Local\nvim\init.vim: Neovim configuration

## Requirements Expectations Considerations Side-effects

- .bash_aliases: None
- .bash_logout: None
- .bash_profile: None
- .bashrc: None
- .gitconfig: None
- .gitignore: None
- .inputrc: None
- AppDat\Local\nvim\init.vim
    - Setup for 24-bit color support from the terminal. Colors will be wrong and/or broken without that support

## Sources

- [ReeceRGGIL/dotfiles](github.com/ReeceRGGIL/dotfiles)
