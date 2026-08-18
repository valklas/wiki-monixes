# Getting Started

To use Monixes, add it as a flake input and import its exposed modules in your
system flake. You can then configure NixOS options in `configuration.nix` and
Home Manager options in `home.nix`.

> [!NOTE]
> The `main` branch is the stable release branch. Development takes place on
> `dev`. To test development changes, use `github:valklas/monixes/dev` and the
> matching `dev` branch of the wiki.

## Example flake

```nix
{
    description = "User's System Configuration Flake powered by Monixes";

    inputs = {
        # Core system packages
        nixpkgs.url = "github:nixos/nixpkgs/nixos-unstable";

        # Home Manager for user-space package configuration
        home-manager = {
            url = "github:nix-community/home-manager";
            inputs.nixpkgs.follows = "nixpkgs";
        };

        monixes = {
            url = "github:valklas/monixes";
            inputs.nixpkgs.follows = "nixpkgs";
        }; 
    };

    outputs = { self, nixpkgs, home-manager, monixes, ... }@inputs: {

        # Matches the profile target name used during 'nixos-rebuild switch --flake .#myhost'
        nixosConfigurations.myhost = nixpkgs.lib.nixosSystem {
            system = "x86_64-linux";

            modules = [
                monixes.nixosModules.default

                ./hardware-configuration.nix
                ./configuration.nix

                home-manager.nixosModules.home-manager
                {
                    home-manager.useGlobalPkgs = true;
                    home-manager.useUserPackages = true;

                    home-manager.users.someone = {
                        imports = [
                            monixes.homeManagerModules.default
                            ./home.nix
                        ];
                    };
                }
            ];
        };
    };
}
```

## Navigation

[← Intro](Intro.md) · [Home](Intro.md) · [System Modules →](system-modules/README.md)
