# System Module: Display Manager

Manages the greetd-tuigreet display manager under the
`monixes.system.desktop.DM` namespace. The default display-manager selection is
`none`, so greetd is not enabled unless selected.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.desktop.DM.displayManager` | Enum: `none`, `greetd-tuigreet` | `"none"` | Select the display manager. |
| `monixes.system.desktop.DM.environment` | String | `"bash"` | Startup command passed to tuigreet, such as `start-hyprland`. |

## Usage Example

```nix
monixes.system.desktop.DM = {
    displayManager = "greetd-tuigreet";
    environment = "start-hyprland";
};
```

Add the above code block in your **configuration.nix** file.
