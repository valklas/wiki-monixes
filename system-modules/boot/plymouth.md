# Boot Module: Plymouth

Enables the Plymouth graphical boot splash through
`monixes.system.boot.plymouth`.

## Option

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.boot.plymouth.enable` | Boolean | `true` | Enable the Plymouth graphical boot splash. |

## Usage

```nix
monixes.system.boot.plymouth.enable = true;
```

Add this to `configuration.nix`. Disabling Plymouth also prevents Monixes from
automatically adding `splash` to the kernel parameters.

## Navigation

[← Limine](limine.md) · [Boot modules](README.md) · [Hardware →](../hardware/README.md)
