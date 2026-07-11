# Getting Started

To use `monixes`, you need to declare it as a flake input and import its exposed modules inside your **flake.nix**. Once imported, you can configure system-level options directly in your **configuration.nix** and user-level options in your **home.nix**.

> [!WARNING]
> If this is your first time using Flakes on your machine, make sure you have enabled experimental features inside your **configuration.nix**:
> ```nix
> nix.settings.experimental-features = [ "nix-command" "flakes" ];
> ```

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
