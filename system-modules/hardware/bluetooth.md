# System Module: Bluetooth

Enables Bluetooth support under the `monixes.system.hardware.bluetooth` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.hardware.bluetooth.enable` | Boolean | `false` | Enable Bluetooth support. |

## Usage Example

```nix
monixes.system.hardware.bluetooth = {
    enable = true;
};
```

Add the above code block to `configuration.nix`.

## Navigation

[← Graphics](graphics.md) · [Home](../../Intro.md) · [Audio →](audio.md)
