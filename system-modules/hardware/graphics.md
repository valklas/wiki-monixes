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

Add the above code block in your **configuration.nix** file.

## Next Step:

See how to set bluetooth options, in the [Bluetooth Module Guide](bluetooth.md).
