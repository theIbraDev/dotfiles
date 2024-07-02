#### Pacman install
Does not include wm, or gpu drivers.
```
$ pacman -S git zsh wireplumber waybar stow grim slurp nvim tmux firefox libreoffice steam obs-studio
```

Programming stuff
```
$ pacman -S rustup luarocks luajit go npm pnpm alacritty
```

## Installation dotfiles

First, check out the dotfiles repo in your $HOME directory using git

```
$ git clone git@github.com/theIbraDev/dotfiles.git
$ cd dotfiles
```

For submodules. Tmux and nvim
```
$ cd dotfiles
$ git submodule update --init --recursive
```

#### First time setup

We use GNU Stow to populate symlinks where needed in your machine, run:
```
$ ~/dotfiles
$ stow .
```

## Optional installation

### yay


```sh
pacman -S --needed git base-devel && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si
```

#### First use of yay

##### Development packages upgrade

- Use `yay -Y --gendb` to generate a development package database for `*-git`
  packages that were installed without yay.
  This command should only be run once.

- `yay -Syu --devel` will then check for development package updates

- Use `yay -Y --devel --save` to make development package updates permanently
  enabled (`yay` and `yay -Syu` will then always check dev packages)
