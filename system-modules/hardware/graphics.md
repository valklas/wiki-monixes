# System Module: Graphics

Enables hardware graphics acceleration (OpenGL / Vulkan drivers) under the `monixes.system.hardware.graphics` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.hardware.graphics.enable` | Boolean | `true` | Enable hardware graphics acceleration. |

## Usage Example

```nix
monixes.system.hardware.graphics = {
    enable = true;
};
```

Add the above code block to `configuration.nix`.

## Navigation

[← Hardware](README.md) · [Home](../../Intro.md) · [Bluetooth →](bluetooth.md)
