# System Modules

Monixes NixOS modules use the `monixes.system.*` namespace. Import
`monixes.nixosModules.default` in your system flake before configuring these
options.

## Wiki Navigation

### Core System

- [Hostname](hostname.md) — Set the machine hostname.
- [User](user.md) — Create the primary user account and assign standard groups.
- [Nix](nix.md) — Configure flakes, store optimization, garbage collection, and unfree packages.

### Networking

- [Networking Modules](networking/README.md)
  - [NetworkManager](networking/networkmanager.md) — Enable NetworkManager.
  - [Firewall](networking/firewall.md) — Configure firewall rules.

### Boot

- [Boot Modules](boot/README.md)
  - [Kernel Parameters](boot/kernel-params.md) — Configure kernel parameters.
  - [Limine](boot/limine.md) — Configure the bootloader.
  - [Plymouth](boot/plymouth.md) — Configure the boot splash.

### Theme

- [Theme](theme.md) — Configure the system Catppuccin theme.

### Hardware

- [Hardware Modules](hardware/README.md)
  - [Graphics](hardware/graphics.md) — Enable graphics acceleration.
  - [Bluetooth](hardware/bluetooth.md) — Enable Bluetooth support.
  - [Audio](hardware/audio.md) — Configure PipeWire audio.

### Desktop

- [Desktop Modules](desktop/README.md)
  - [Display Manager Modules](desktop/DM/README.md)
    - [greetd-tuigreet](desktop/DM/greetd-tuigreet.md) — Configure greetd.

## Navigation

[← Intro](../Intro.md) · [Home](../Intro.md) · [Hostname →](hostname.md)
