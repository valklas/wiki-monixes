# System Module: Display Manager

Manages greetd display manager configuration under the `monixes.system.desktop.displayManager.greetd` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.desktop.displayManager.greetd.enable` | Boolean | `true` | Enable greetd display manager with tuigreet. |
| `monixes.system.desktop.displayManager.greetd.environment` | String | `"bash"` | The target user environment name or custom startup command (e.g. start-hyprland). |

## Usage Example

```nix
monixes.system.desktop.displayManager.greetd = {
    enable = true;
    environment = "start-hyprland";
};
```

Add the above code block in your **configuration.nix** file.
