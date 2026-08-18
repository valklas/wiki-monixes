# Boot Modules

Boot modules use the `monixes.system.boot.*` namespace.

## Available modules

- [Kernel parameters](kernel-params.md) — Add extra kernel parameters while preserving Monixes defaults.
- [Limine](limine.md) — Enable and configure the Limine bootloader.
- [Plymouth](plymouth.md) — Enable the graphical boot splash.

## Defaults

Monixes always adds `quiet` to the kernel command line. It also adds `splash`
while Plymouth is enabled. Custom values from `kernelParams` are merged with
those defaults and duplicate values are removed.

## Navigation

[← System modules](../README.md) · [Kernel parameters](kernel-params.md) · [Limine](limine.md) · [Plymouth →](plymouth.md)
