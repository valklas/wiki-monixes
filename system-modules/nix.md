# System Module: User Creation

Optimizes the core Nix package manager engine, manages storage hygiene, and configures licensing terms under the `monixes.system.nix` namespace.

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
