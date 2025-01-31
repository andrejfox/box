**Modules** are chunks of nix code that extend your nix code configuration by setting options od providing new ones. Basically functions that take some arguments and return dictionaries with options.
```nix
{ pkgs, lib, ... }:

{
	option1.enable = true;
	systemPackages = with pkgs; {
		neovim
	}
}
```
This is equivalent to this peace of pseudo code:
```
export function({pkgs, lib, ...}) {
	return {
		"option1.enable" = true,
		"systemPackages" = [
			pkgs.neovim
		],
	}
}
```
```
[andrej@nixos:/etc/nixos]$ nixos-rebuild dry-build --flake /etc/nixos#default
building the system configuration...

[andrej@nixos:/etc/nixos]$ 
```