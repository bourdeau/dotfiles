# Dotfiles

My dotfiles

## Install

I use [tow](https://www.gnu.org/software/stow/) to manage my dotfiles.


## Rust

```bash
# Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source .bashrc
```

## Terminal: Alacritty

```
cargo install alacritty

# Set it as default terminal
sudo update-alternatives --install /usr/bin/x-terminal-emulator x-terminal-emulator /home/ph/.cargo/bin/alacritty 50
sudo update-alternatives --config x-terminal-emulator
```

## Shell Prompt: Starship

```
cargo install starship
```

## Terminal workspace: zellij

```
cargo install --locked zellij
```

## Shell: Nushell

```
sudo apt install pkg-config libssl-dev
cargo install nu
```

## Carapace: Shell Completion

```
wget https://github.com/carapace-sh/carapace-bin/releases/download/v1.0.1/carapace-bin_1.0.1_linux_amd64.deb && \
sudo dpkg -i carapace-bin_1.0.1_linux_amd64.deb
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

## Neovim: Treesitter

:TSInstall bash python cmake dockerfile elixir gitignore go graphql hcl html http javascript json make markdown rust sql terraform toml xml yaml zig
