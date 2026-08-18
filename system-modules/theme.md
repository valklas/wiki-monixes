# System Module: Theme

Configures the NixOS-wide Catppuccin theme through `monixes.system.theme`.
This is a system option set and is separate from the Home Manager
[`monixes.home.theme`](../home-modules/theme.md) option set.

The Monixes flake imports the Catppuccin NixOS module automatically. When
enabled, the wrapper enables Catppuccin and its supported automatic
integrations.

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

## Navigation

[← greetd-tuigreet](desktop/DM/greetd-tuigreet.md) · [Home](../Intro.md) · [Home Theme →](../home-modules/theme.md)
