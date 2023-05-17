# Introduction

## MagmaWM Info

**MagmaWM** is a versatile and customizable [Wayland compositor](https://wayland.freedesktop.org/) for Linux systems, made with the [Smithay](https://github.com/Smithay/smithay) library and programmed in [Rust](https://www.rust-lang.org/).

it is currently in heavy development, so bugs and drastic changes are to be expected as MagmaWM develops.

## Wayland Info
Unlike X, which has a display server which communicates with a WM, Wayland itself is a protocol, instead having the WM (if you want to be pedantic, it's technically called a Wayland compositor) handle the duties that would be handled by a display server on X.

## Support Info
If you are having issues, consider joining our [Discord server](https://discord.gg/VM8DkxaHfa).

## Building MagmaWM

### 0. Disclaimer
MagmaWM is under heavy development and is alpha-quality, so it is not recommended for daily use just yet.
If you do wish to use it, make sure you have another WM installed so you have something to fall back on in case MagmaWM breaks.

### 1. Dependencies
You will need to install MagmaWM's dependencies with your package manager of choice.

#### Debian and derivatives (Ubuntu, Linux Mint, MX Linux, etc.)
```bash
# apt install libudev-dev libgbm-dev libxkbcommon-dev libegl1-mesa-dev libwayland-dev libinput-dev libdbus-1-dev libsystemd-dev libseat-dev
```
#### Arch and derivatives (EndeavourOS, Garuda, etc.)
Manjaro is **not** supported.
```bash
# pacman -Syu udev wayland wayland-protocols libinput libxkbcommon libglvnd seatd dbus-glib mesa
```
#### openSUSE Tumbleweed
```bash
# zypper in systemd-devel libgbm-devel libxkbcommon-devel Mesa-libEGL1 wayland-devel libinput-devel libdbus-glib-1-3 seatd-devel
```

### 2. Compilation
Clone the git repo and build MagmaWM by running the following command:
```bash
$ cargo build --release
```
The binary will be created in `./target/release/magmawm`.
You can also use `cargo run --release` to run the project.
## Install
**MagmaWM** is still under heavy development and installation is not recommended.
If you really want to, run the following command to install MagmaWM: 
```bash
cargo install --path .
```

