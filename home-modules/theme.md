# Home Manager Module: Theme

Configures the user-session Catppuccin theme through
`monixes.home.theme`. Import `monixes.homeManagerModules.default` inside the
relevant `home-manager.users.<name>` module before using these options.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.home.theme.enable` | Boolean | `true` | Enable the user theme. |
| `monixes.home.theme.flavor` | Enum: `latte`, `frappe`, `macchiato`, `mocha` | `"mocha"` | Catppuccin flavor. |
| `monixes.home.theme.accent` | Enum: `rosewater`, `flamingo`, `pink`, `mauve`, `red`, `maroon`, `peach`, `yellow`, `green`, `teal`, `sky`, `sapphire`, `blue`, `lavender` | `"blue"` | Catppuccin accent color. |

## Usage Example

```nix
monixes.home.theme = {
    enable = true;
    flavor = "mocha";
    accent = "blue";
};
```

Set these options in the user's `home.nix`.

For NixOS-wide theming, see the [System Theme Guide](../system-modules/theme.md).
