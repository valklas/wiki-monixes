# Boot Module: Kernel Parameters

Adds custom kernel parameters through `monixes.system.boot.kernelParams`.
Monixes always adds `quiet`, and adds `splash` when
`monixes.system.boot.plymouth.enable` is enabled. Duplicate values are
removed.

## Option

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.boot.kernelParams` | List of strings | `[ ]` | Additional kernel parameters to pass at boot. |

## Usage

```nix
monixes.system.boot.kernelParams = [ "kvm-intel" "tun" ];
```

Add this to `configuration.nix`.

## Navigation

[← Boot modules](README.md) · [Boot modules](README.md) · [Limine →](limine.md)
