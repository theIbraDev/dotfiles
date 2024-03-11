# My dotfiles

This directory contains the dotfiles for my system

## Requirements

Ensure you have the following installed on your system

### Requirements

Install using your package manager

#### Pacman install
```
pacman -S git stow flameshot i3 nvim tmux kitty brave libreoffice
```

## Installation dotfiles

First, check out the dotfiles repo in your $HOME directory using git

```
$ git clone git@github.com/rossvold/dotfiles.git
$ cd dotfiles
```

To create the symlinks open your HOME/dotfiles repository, use GNU stow to create symlinks

```
HOME/dotfiles
$ stow .
```

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

#### Usage

Use 'yay steam' to search for steam packages. From there you can install from the menu the packages you want.

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
