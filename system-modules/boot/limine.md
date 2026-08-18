# Boot Module: Limine

Configures the Limine bootloader through `monixes.system.boot.limine`.
Limine is enabled by default when the Monixes NixOS module is imported.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.boot.limine.enable` | Boolean | `true` | Enable the Limine bootloader. |
| `monixes.system.boot.canTouchEfiVariables` | Boolean | `true` | Allow NixOS to modify EFI variables. |

## Usage

```nix
monixes.system.boot = {
    limine.enable = true;
    canTouchEfiVariables = true;
};
```

Add this to `configuration.nix`.

## Navigation

[← Kernel Parameters](kernel-params.md) · [Home](../../Intro.md) · [Plymouth →](plymouth.md)
