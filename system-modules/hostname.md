# System Module: Hostname

Manages the host machine network identification under the `monixes.system.host` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.host.enable` | Boolean | `false` | Enables machine hostname management. |
| `monixes.system.host.name` | String | `"nixos"` | Sets the operating system hostname. |

## Usage Example

```nix
monixes.system.host = {
  enable = true;
  name = "thinkpad";
};
```

Add the above code block in your **configuration.nix** file.

## Next Step

See how user is set, in the [User Module Guide](user.md).
