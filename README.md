# Omarchy setup

![screenshot](./screenshot.png)

## Ghostty

In omarchy menu install the `ghostty` terminal.

## Get a good neovim config

```bash
git clone https://github.com/krisfur/neovim-config
cp neovim-config/init.lua ~/.config/nvim/
```

## Install more dev tools

```bash
mise use -g odin
mise use -g opencode
mise use -g cmake
mise use -g ninja
mise use -g typst
```

for clang:

```bash
mise settings set experimental true
mise use -g "conda:clang"
```

for swift:

```bash
sudo pacman -S ncurses
sudo ln -sf /usr/lib/libncursesw.so.6 /usr/lib/libncurses.so.6
sudo ldconfig
ls -l /usr/lib/libncurses.so.6
mise settings set experimental true
mise settings set swift.platform ubi9
mise use -g swift@6.3
```

all else can be grabbed from the omarchy menu (`bun`, `go`, `python`, `rust`, `zig`).

## Fix audio on Zephyrus G14

```bash
amixer -c 2 set Master 100%
amixer -c 2 set Speaker 100%
amixer -c 2 set PCM 100%
amixer -c 2 set 'Bass Speaker' on
amixer -c 2 set 'AMP1 Speaker' 0dB
amixer -c 2 set 'AMP2 Speaker' 0dB
sudo alsactl store
```

## Set the Zephyrus G14 slash to static

```bash
asusctl slash --mode Static
```

## Get helium browser

From AUR install `helium-browser-bin`.
