# System Module: User Creation

Automates administrative group assignments and home directory paths under the `monixes.system.user` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.user.enable` | Boolean | `false` | Enables automated user provisioning. |
| `monixes.system.user.name` | String | *Required* | The primary account username. |

## Usage Example

```nix
monixes.system.user = {
    enable = true;
    name = "someone";
};
```

Add the above code block in your **configuration.nix** file.

## Next Step

See how networkmanager is set, in the [Network Manager Guide](networking/networkmanager.md).
