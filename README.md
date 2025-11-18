# Dotfiles

My personal dotfiles for Arch Linux with Hyprland, managed with GNU Stow.

## Included Configs

- **hypr/** - Hyprland window manager config
- **waybar/** - Waybar status bar config
- **nvim/** - Neovim/LazyVim config
- **zsh/** - Zsh shell config (Oh My Zsh)
- **git/** - Git config
- **applications/** - Custom desktop entries (Discord, thinkorswim, etc.)

## Installation

1. Clone this repo to your home directory:
   ```bash
   git clone https://github.com/YOUR_USERNAME/dotfiles.git ~/dotfiles
   ```

2. Install GNU Stow:
   ```bash
   sudo pacman -S stow
   ```

3. Stow the configs you want:
   ```bash
   cd ~/dotfiles
   stow hypr
   stow waybar
   stow nvim
   stow zsh
   stow git
   stow applications
   ```

## Adding New Configs

1. Create the directory structure mirroring where the config lives:
   ```bash
   mkdir -p ~/dotfiles/newconfig/.config/newconfig
   ```

2. Move your config there:
   ```bash
   mv ~/.config/newconfig/* ~/dotfiles/newconfig/.config/newconfig/
   ```

3. Stow it:
   ```bash
   cd ~/dotfiles && stow newconfig
   ```

## System Info

- **OS**: Arch Linux (Omarchy)
- **WM**: Hyprland
- **Shell**: Zsh with Oh My Zsh
- **Editor**: Neovim with LazyVim
