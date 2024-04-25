# My dotfiles

## Requirements

Ensure you have the following installed on your system

### Requirements

- [Git](https://git-scm.com/downloads)
- [GH](https://cli.github.com/)
- [Stow](https://www.gnu.org/software/stow/)
- [wayland](https://wayland.freedesktop.org/)
- [hypr](https://hyprland.org/)
- [Neovim](https://neovim.io/)
- [Alacritty](https://alacritty.org)
- [Kitty](https://sw.kovidgoyal.net/kitty/)
- [tmux](https://github.com/tmux/tmux)
- [LibreOffice](https://www.libreoffice.org/)

I will be using pacman. I use arch btw,
#### Pacman install
```
$ pacman -S git stow flameshot i3 nvim tmux brave libreoffice
```

## Installation dotfiles

First, check out the dotfiles repo in your $HOME directory using git

```
$ git clone git@github.com/theIbraDev/dotfiles.git
$ cd dotfiles
```

If you also want my nvim config, you need to populate git submodules:
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
- Set download path for flameshot at dotfiles/config/flameshot/flameshot.ini. Canno't use ~ or $ path.
- i3 Workspaces and screen outputs needs to be configured to your screen setup.
- Nvim run packer to install packages

## Optional installation

### yay

The initial installation of Yay can be done by cloning the PKGBUILD and
building with makepkg:

Before you begin, make sure you have the `base-devel` package group installed.


```sh
pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

If you want to do all of this at once, we can chain the commands like so:

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

#### Usage of yay

Use 'yay steam' to search for steam packages. From there you can install from the menu the packages you want.

### Brave browser
- [Brave Browser](https://brave.com/)

```
yay brave-bin
```

### Open Broadcaster Software

If the browser plugin is required, we have to use the AUR package obs-studio-git

- Yay is required for this.
```
yay obs-studio-git
```
If not, just use the official stable one:

```
sudo pacman -S obs-studio
```
