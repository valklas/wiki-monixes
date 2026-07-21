# Welcome to monixes

`monixes` is a lightweight, unified configuration wrapper for NixOS and Home Manager. It simplifies how you deploy machines by grouping low-level settings under a clean, unified schema (`monixes.*`).

## Wiki Navigation

*   **[Getting Started](Getting-Started.md)**: Add the flake inputs and register the modules to your system.
*   **System Modules**:
    *   [Host Config](system-modules/hostname.md) — Handle machine identification.
    *   [User Config](system-modules/user.md) — Automate system user setup.
    *   **Networking**:
        *   [Network Manager Config](system-modules/networking/networkmanager.md) — Network Manager setup.
        *   [Firewall Config](system-modules/networking/firewall.md) — Firewall setup.
    *   [Nix Config](system-modules/nix.md) — Automate weekly garbage collection, enable or disable installation of packages with proprietary licenses, enable flake by default.
    *   [Boot Config](system-modules/boot.md) — Configure the system bootloader.
    *   **Hardware**:
        *   [Graphics Config](system-modules/hardware/graphics.md) — Enable hardware graphics acceleration.
        *   [Bluetooth Config](system-modules/hardware/bluetooth.md) — Enable Bluetooth support.
        *   [Audio Config](system-modules/hardware/audio.md) — Configure modern PipeWire audio stack.
    *   **Desktop**:
        *   [Display Manager Config](system-modules/desktop/display-manager.md) — Configure greetd display manager.
*   **Home Manager Modules**: (Coming Soon).

Source Code: [monixes Repository](https://github.com/valklas/monixes.git)
