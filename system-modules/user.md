# System Module: User Creation

Automates administrative group assignments and home directory paths under the `monixes.user` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.user.enable` | Boolean | `false` | Enables automated user provisioning. |
| `monixes.user.name` | String | *Required* | The primary account username. |

## Usage Example

```nix
monixes.user = {
  enable = true;
  name = "someone";
};
```

Add the above code block in your **configuration.nix** file.
