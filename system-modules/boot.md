# System Module: Boot

Configures the Limine bootloader, EFI variable access, Plymouth, and extra
kernel parameters under `monixes.system.boot`.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.boot.limine.enable` | Boolean | `true` | Enable the Limine bootloader. |
| `monixes.system.boot.canTouchEfiVariables` | Boolean | `true` | Allow NixOS to modify EFI variables. |
| `monixes.system.boot.plymouth.enable` | Boolean | `true` | Enable the Plymouth graphical boot splash. |
| `monixes.system.boot.kernelParams` | List of strings | `[ ]` | Additional kernel parameters to pass at boot. |

Monixes always adds `quiet`. It also adds `splash` while
`monixes.system.boot.plymouth.enable` is enabled. Values from `kernelParams`
are merged with those defaults and duplicate values are removed.

## Usage Example

```nix
monixes.system.boot = {
    limine.enable = true;
    canTouchEfiVariables = true;
    plymouth.enable = true;
    kernelParams = [ "kvm-intel" "tun" ];
};
```

Add the above code block in your **configuration.nix** file.

## Next Step:

See how system theming is configured, in the [Theme Module Guide](theme.md).
