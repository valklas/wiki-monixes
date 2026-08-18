# System Module: Theme

Configures the system-wide Catppuccin theme through the unified
`monixes.system.theme` interface. The Monixes flake imports the Catppuccin
NixOS module automatically. When enabled, Catppuccin's `autoEnable` behavior
is also enabled so supported integrations can adopt the selected theme
automatically.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.theme.enable` | Boolean | `true` | Enable the system theme. |
| `monixes.system.theme.flavor` | Enum: `latte`, `frappe`, `macchiato`, `mocha` | `"mocha"` | Catppuccin flavor. |
| `monixes.system.theme.accent` | Enum: `rosewater`, `flamingo`, `pink`, `mauve`, `red`, `maroon`, `peach`, `yellow`, `green`, `teal`, `sky`, `sapphire`, `blue`, `lavender` | `"blue"` | Catppuccin accent color. |

## Usage Example

```nix
monixes.system.theme = {
    enable = true;
    flavor = "mocha";
    accent = "mauve";
};
```

Set these options in `configuration.nix`.

For user-session theming, see the [Home Manager Theme Guide](../home-modules/theme.md).
