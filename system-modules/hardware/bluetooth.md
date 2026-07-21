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

Add the above code block in your **configuration.nix** file.

## Next Step:

See how to set audio options, in the [Audio Module Guide](audio.md).
