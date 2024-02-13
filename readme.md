# My dotfiles

This directory contains the dotfiles for my system

## Requirements

Ensure you have the following installed on your system

### Requirements

Install using your package manager

#### Pacman install
```
pacman -S git stow flameshot i3 nvim tmux kitty
```

## Installation

First, check out the dotfiles repo in your $HOME directory using git

```
$ git clone git@github.com/rossvold/dotfiles.git
$ cd dotfiles
```

then use GNU stow to create symlinks

```
$ stow .
```
