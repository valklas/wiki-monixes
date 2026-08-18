# Monixes Wiki

Documentation for [Monixes](https://github.com/valklas/monixes), a lightweight
configuration wrapper for NixOS and Home Manager.

Start with the [introduction](Intro.md).

> [!NOTE]
> This wiki is up to date through Monixes commit
> [`106d4f6`](https://github.com/valklas/monixes/commit/106d4f662a397596fe7adfb1055e522034b6bed0),
> `Configure Catppuccin auto-enable`. Changes introduced after this commit
> may not be documented yet; pages for subsequent commits will be added soon.

## Wiki Architecture

```
wiki-monixes/
├── AGENTS.md
├── Getting-Started.md
├── Intro.md
├── LICENSE
├── README.md
├── home-modules
│   ├── README.md
│   └── theme.md
└── system-modules
    ├── README.md
    ├── boot
    │   ├── README.md
    │   ├── kernel-params.md
    │   ├── limine.md
    │   └── plymouth.md
    ├── desktop
    │   ├── README.md
    │   └── DM
    │       ├── README.md
    │       └── greetd-tuigreet.md
    ├── hardware
    │   ├── README.md
    │   ├── audio.md
    │   ├── bluetooth.md
    │   └── graphics.md
    ├── hostname.md
    ├── networking
    │   ├── README.md
    │   ├── firewall.md
    │   └── networkmanager.md
    ├── nix.md
    ├── theme.md
    └── user.md

8 directories, 26 files
```

## License

This Repo is under [MIT](LICENSE).
