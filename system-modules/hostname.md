# System Module: Hostname

Manages the host machine network identification under the `monixes.system.host` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.host.enable` | Boolean | `false` | Enables machine hostname management. |
| `monixes.system.host.name` | String | `"monixes"` | Sets the operating system hostname. |

## Usage Example

```nix
monixes.system.host = {
    enable = true;
    name = "thinkpad";
};
```

Add the above code block to `configuration.nix`.

## Navigation

[← System Modules](README.md) · [Home](../Intro.md) · [User →](user.md)
