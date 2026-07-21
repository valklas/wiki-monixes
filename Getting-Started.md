# Getting Started

To use `monixes`, you need to declare it as a flake input and import its exposed modules inside your **flake.nix**. Once imported, you can configure system-level options directly in your **configuration.nix** and user-level options in your **home.nix**.

> [!NOTE]
> **Branch Configurations & Stability:**
> * The `main` branch is stable and all the development is done on the `dev` branch.
> * If you want to test the `monixes` dev branch, add `https://github.com/valklas/monixes/dev` (or `github:valklas/monixes/dev`) as the input URL in the flake.
> * If you want to use the main branch of `monixes`, refer to the stable wiki at [https://github.com/valklas/wiki-monixes](https://github.com/valklas/wiki-monixes). For the dev branch, refer to the dev wiki branch at [https://github.com/valklas/wiki-monixes/tree/dev](https://github.com/valklas/wiki-monixes/tree/dev).

Check out the **flake.nix** example below:

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

        # 1. Import your custom monixes flake configuration framework
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
                # 2. Inject the monixes wrapper layer into the system build environment
                monixes.nixosModules.default

                # 3. Import standard core system layout configs
                ./hardware-configuration.nix
                ./configuration.nix

                # 4. Include home-manager setup directly within the NixOS configuration context
                home-manager.nixosModules.home-manager
                {
                    home-manager.useGlobalPkgs = true;
                    home-manager.useUserPackages = true;

                    # Inject the monixes Home Manager bundle into user-space setups
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

## Next Step

See how hostname is set, in the [Hostname Module Guide](system-modules/hostname.md).
