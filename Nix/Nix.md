**Configs:**
Main config: `/etc/nixos/configuration.nix`
Hardware config: `/etc/nixos/hardware-configuration.nix`
Flakes: ``

> [!NOTE] Help
>  `man /etc/nixos/configuration.nix`
>  `/bluetooth`

**Rebuilding:**
Creates a system version:  
Rebuilds system but no addition to boot loader : `sudo nixos-rebuild test`
Cleaning up system versions: `sudo nix-collect-garbage --delete-older-than 15d`

**bins:**
All in `/nix/store`

[[Modules]]
[[Flakes]]