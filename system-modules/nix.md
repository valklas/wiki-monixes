# System Module: Nix

Optimizes the core Nix package manager engine, manages storage hygiene, and configures licensing terms under the `monixes.system.nix` namespace.

> [!WARNING]
> By default, `monixes` automatically handles experimental `flakes` and `nix-command` provisioning for your system behind the scenes. 
> 
> However, if you explicitly opt out by setting `monixes.system.nix.enable = false;`, you **must** manually add the following:
> 
> ```nix
> nix.settings.experimental-features = [ "nix-command" "flakes" ];
> ```
> 
> in your **configuration.nix** to avoid build failures.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.nix.enable` | Boolean | `true` | Provision background maintenance optimizations. |
| `monixes.system.nix.allowUnfree` | Boolean | `true` | Controls the evaluation engine block for proprietary licenses. |

## Usage Example

```nix
monixes.system.nix = {
    enable = true;
    allowUnfree = false;
};
```

Add the above code block in your **configuration.nix** file.

## Next Step:

See how system boot is set, in the [Boot Module Guide](boot.md).
