# Welcome to Monixes

Monixes is a lightweight configuration wrapper for NixOS and Home Manager. It
groups low-level settings behind a consistent option schema:

- `monixes.system.*` for NixOS configuration.
- `monixes.home.*` for Home Manager configuration.

## Wiki Navigation

- [Getting Started](Getting-Started.md): Add the flake inputs and register the modules to your system.
- [System Modules](system-modules/README.md) — NixOS configuration.
  - [Core System](system-modules/README.md#core-system)
    - [Hostname](system-modules/hostname.md) — Configure hostname.
    - [User](system-modules/user.md) — Create the primary user account.
    - [Nix](system-modules/nix.md) — Configure the Nix package manager.
  - [Networking](system-modules/networking/README.md)
    - [NetworkManager](system-modules/networking/networkmanager.md) — Enable NetworkManager.
    - [Firewall](system-modules/networking/firewall.md) — Configure firewall rules.
  - [Boot](system-modules/boot/README.md)
    - [Kernel Parameters](system-modules/boot/kernel-params.md) — Configure kernel parameters.
    - [Limine](system-modules/boot/limine.md) — Configure the bootloader.
    - [Plymouth](system-modules/boot/plymouth.md) — Configure the boot splash.
  - [Theme](system-modules/theme.md) — Configure the system Catppuccin theme.
  - [Hardware](system-modules/hardware/README.md)
    - [Graphics](system-modules/hardware/graphics.md) — Enable graphics acceleration.
    - [Bluetooth](system-modules/hardware/bluetooth.md) — Enable Bluetooth support.
    - [Audio](system-modules/hardware/audio.md) — Configure PipeWire audio.
  - [Desktop](system-modules/desktop/README.md)
    - [Display Manager](system-modules/desktop/DM/README.md)
      - [greetd-tuigreet](system-modules/desktop/DM/greetd-tuigreet.md) — Configure greetd.
- [Home Manager Modules](home-modules/README.md) — User-session configuration.
  - [Theme](home-modules/theme.md) — Configure the user Catppuccin theme.

## Navigation

[← README](README.md) · [Home](Intro.md) · [Getting Started →](Getting-Started.md)
