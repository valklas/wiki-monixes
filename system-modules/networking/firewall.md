# System Module: Firewall

Secures the system against unauthorized network traffic by wrapping NixOS infrastructure routing filters under the `monixes.system.networking.firewall` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.networking.firewall.enable` | Boolean | `true` | Provision background firewall routing tables. |
| `monixes.system.networking.firewall.allowSSH` | Boolean | `false` | Expose standard incoming secure shell infrastructure (Port 22 and 443). |
| `monixes.system.networking.firewall.allowedTCPPorts` | List of Ports | `[ ]` | Custom TCP ports to open globally. |
| `monixes.system.networking.firewall.allowedUDPPorts` | List of Ports | `[ ]` | Custom UDP ports to open globally. |

## Usage Example

```nix
monixes.system.networking.firewall = {
	enable = true;
	allowSSH = true;
	allowedTCPPorts = [ 100 200 ];
	allowedUDPPorts = [ 100 200 ];
};
```

Add the above code block in your **configuration.nix** file.

## Next Step:

See some extra nix modules and how to set them, in the [Nix Module Guide](../nix.md).
