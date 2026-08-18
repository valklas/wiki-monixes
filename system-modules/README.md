# System Modules

Monixes NixOS modules use the `monixes.system.*` namespace. Import
`monixes.nixosModules.default` in your system flake before configuring these
options.

## Module groups

### Core system

- [Hostname](hostname.md) — Set the machine hostname.
- [User](user.md) — Create the primary user account and assign standard groups.
- [Nix](nix.md) — Configure flakes, store optimization, garbage collection, and unfree packages.

### Boot and desktop

- [Boot modules](boot/README.md) — Configure Limine, Plymouth, and kernel parameters.
- [Theme](theme.md) — Configure the system Catppuccin theme.
- [Desktop](desktop/README.md) — Configure the display manager.

### Hardware

- [Hardware modules](hardware/README.md) — Configure graphics, Bluetooth, and audio.

### Networking

- [Networking modules](networking/README.md) — Configure NetworkManager and the firewall.

## Navigation

[← Home](../Intro.md) · [System modules](README.md) · [Hostname →](hostname.md)
