# System Module: Boot

Configures the Limine bootloader, EFI variable access, Plymouth, and extra
kernel parameters under `monixes.system.boot`.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.boot.limine.enable` | Boolean | `true` | Enable the Limine bootloader. |
| `monixes.system.boot.canTouchEfiVariables` | Boolean | `true` | Allow NixOS to modify EFI variables. |
| `monixes.system.boot.plymouth.enable` | Boolean | `true` | Enable the Plymouth graphical boot splash. |
| `monixes.system.boot.kernelParams` | List of strings | `[ "quiet" "splash" ]` | Additional kernel parameters appended to the system configuration. |

## Usage Example

```nix
monixes.system.boot = {
    limine.enable = true;
    canTouchEfiVariables = true;
    plymouth.enable = true;
    kernelParams = [ "quiet" "splash" ];
};
```

Add the above code block in your **configuration.nix** file.

## Next Step:

See how system theming is configured, in the [Theme Module Guide](theme.md).
