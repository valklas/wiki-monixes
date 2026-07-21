# System Module: Audio

Enables PipeWire audio stack configuration under the `monixes.system.hardware.audio` namespace.

## Options

| Option | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `monixes.system.hardware.audio.enable` | Boolean | `true` | Enable modern PipeWire audio stack with ALSA and PulseAudio emulation. |
| `monixes.system.hardware.audio.supportJack` | Boolean | `false` | Enable JACK audio emulation layer for pro-audio and production software. |

## Usage Example

```nix
monixes.system.hardware.audio = {
    enable = true;
    supportJack = true;
};
```

Add the above code block in your **configuration.nix** file.

## Next Step:

See how to set display-manager options, in the [Display Manager Guide](../desktop/display-manager.md).
