# Desktop Module: greetd-tuigreet

Configures greetd with the tuigreet interface. The module is selected through
`monixes.system.desktop.DM`.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.desktop.DM.displayManager` | Enum: `none`, `greetd-tuigreet` | `"none"` | Select the display manager. |
| `monixes.system.desktop.DM.environment` | String | `"bash"` | Startup command passed to tuigreet, such as `start-hyprland`. |

The `displayManager` option defaults to `none`, so greetd is not enabled until
`greetd-tuigreet` is selected.

## Usage Example

```nix
monixes.system.desktop.DM = {
    displayManager = "greetd-tuigreet";
    environment = "start-hyprland";
};
```

Add the above code block to `configuration.nix`.

## Navigation

[← Display Manager modules](README.md) · [Desktop modules](../README.md) · [Theme →](../../theme.md)
