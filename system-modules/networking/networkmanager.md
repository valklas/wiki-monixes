# System Module: Network Manager

Manages the core network connectivity engine under the `monixes.system.networking.networkmanager` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.networking.networkmanager.enable` | Boolean | `true` | Toggles networkmanager |

## Usage Example

```nix
monixes.system.networking = {
    networkmanager.enable = true;
};
```

Add the above code block in your **configuration.nix** file.

## Next Step:

See how to set firewall, in the [firewall Guide](firewall.md).
