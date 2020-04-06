NixOS configuration

## Setup

Add and update `nixos-config` channel:

```
$ sudo nix-channel --add https://github.com/HellSt0rm/nixos-config/archive/master.tar.gz nixos-config
$ sudo nix-channel --update nixos-config
```

Then import an appropriate setting profile path from the table below. For example, to
enable host specific settings for Algiz, modify your `imports` in `/etc/nixos/configuration.nix`
should look like:

```
imports = [
  <nixos-config/host/algiz>
  ./hardware-configuration.nix
];
```

## Incomplete list of Profiles

See code for all available configurations.

| Model                             | Path                                               |
| --------------------------------- | -------------------------------------------------- |
| [Algiz][]                         | `<nixos-config/host/algiz>`                        |

[Algiz]: host/algiz
