# Dotfiles

My dotfiles

# Install

I use [chezmoi](https://www.chezmoi.io/) to handle my dotfiles.


## Setup

sudo apt-get install libfuse2

## Fonts

```
mkdir -p .fonts
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/JetBrainsMono.zip
```

## Terminal: Alcratty

```
cargo install alacritty

sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator /home/ph/.cargo/bin/alacritty 50
sudo update-alternatives --config x-terminal-emulator
```

## Shell Prompt: Starship

```
sudo curl -sS https://starship.rs/install.sh | sh
```

## Text Editor: Neovim

```
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim.appimage
chmod u+x nvim.appimage
./nvim.appimage
./nvim.appimage --appimage-extract
./squashfs-root/AppRun --version
sudo mv squashfs-root /
sudo ln -s /squashfs-root/AppRun /usr/bin/nvim
nvim
```