# System Module: Boot

Manages the system bootloader configuration under the `monixes.system.boot` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.boot.enable.limine` | Boolean | `true` | Enable Limine bootloader configuration. |

## Usage Example

```nix
monixes.system.boot.limine = {
    enable = true;
};
```

Add the above code block in your **configuration.nix** file.

## Next Step:

See how hardware graphics acceleration is configured, in the [Graphics Module Guide](hardware/graphics.md).
