# Dotfiles

My dotfiles

# Install

I use [chezmoi](https://www.chezmoi.io/) to handle my dotfiles.


## Setup

```bash
# Deps
sudo apt-get install -y gcc cmake g++ libfuse2 libfontconfig1-dev

#Rustup
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source .bashrc

# chezmoi
sh -c "$(curl -fsLS get.chezmoi.io)"
sudo mv ~/bin/chezmoi /usr/local/bin && sudo chmod +x /usr/local/bin/chezmoi
chezmoi init git@github.com:$GITHUB_USERNAME/dotfiles.git

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

:TSInstall bash python cmake dockerfile elixir gitignore go graphql hcl html http javascript json make markdown rust sql terraform toml xml yaml zig


