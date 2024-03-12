# Linux Gaming

## Glossary
<details>

**Linux** - used as a short version of GNU/Linux. Linux is a kernel, and when combined with the GNU operating system, it forms the GNU/Linux operating system.

**Kernel** - The core of an operating system.

**Distro** - short for a linux distribution.

</details>

## What distro should I use for Linux gaming?

The choice of a Linux distribution depends entirely on your preferences. There isn't a one-size-fits-all recommendation, but here are some widely popular, well-optimized, and community-favored options to consider.

### [Arch](https://archlinux.org/) based

Arch-based distros are the ones with the best support for gaming, but it may be overwhelming for beginners. If you don't know what you are doing, I wouldn't recommend any of those listed here.

Arch-based distros are intended to be used by advanced or semi-advanced users. Those are often referred to as "rolling-release" which means that packages and kernel is always up-to-date

- [Arch Linux](https://archlinux.org/)
- [EndeavourOS](https://endeavouros.com/) - Often referred to as the user-friendly version of Arch Linux, EndeavourOS comes with the calamares installer for an easier setup experience.
- [Garuda Linux](https://garudalinux.org/) - "Gaming" distro
- [Manjaro](https://manjaro.org/) - Relatively easy to use Arch Linux. Comes with installer. Updates for Manjaro may not be always on time, due to their own [release system](https://wiki.manjaro.org/index.php/Manjaro:A_Different_Kind_of_Beast#Dedicated_Repositories).

### [Debian](https://www.debian.org/) and [Ubuntu](https://ubuntu.com/) based

Commonly known as the best linux distributions for beginners, Debian-based distributions are one of the most popular choices amongst them. However, they may come with outdated packages, as they offer stable-release system.

- [Debian](https://www.debian.org/)
- [Ubuntu](https://ubuntu.com/) - One of the most commonly used distributions, based off Debian
- [Linux Mint](https://www.linuxmint.com/) - Best distro for beginners, highest rating on distrowatch.com, based off Ubuntu.
- [Pop_OS!](https://pop.system76.com/) - Made for beginners, based on Ubuntu

### [Fedora](https://fedoraproject.org/) based

- [Fedora](https://fedoraproject.org/)
- [Nobara](https://nobaraproject.org/) - "Gaming" distro, same creator as Proton-GE

### Other/Advanced Distros

- [Gentoo](https://www.gentoo.org/) - For advanced users, you compile everything yourself
- [Funtoo](https://www.funtoo.org/Welcome) - A more optimized version of Gentoo
- [NixOS](https://nixos.org/) - Based on Nix Package Manager

## How does Linux gaming compare to Windows gaming?

While a lot of games are programmed only for Windows, [most of them](https://www.protondb.com/) run perfectly fine on Linux thanks to Proton, which is a collection of software and libraries combined with a patched version of [WINE](https://www.winehq.org/), a compatibility layer that translates Windows system calls to Linux ones.

Games made for Linux or designed to work on Linux usually run smoothly on the platform, occasionally outperforming their Windows counterparts. On the other hand, when running games not originally intended for use on Linux, the outcome may vary, dependant on factors such as your Linux distribution, installed tools, game, compatibility tools, and more.

## Optimizing the system for gaming

### Which kernel should I use?

The standard Linux kernel should sufice; however, if maximum performance is important to you, here are some recommended kernels:

- [linux-zen](https://github.com/zen-kernel/zen-kernel) - Most commonly used out of this bunch
- [XanMod](https://xanmod.org/) - Use real-time version
- [Liquroix](https://liquorix.net/)
- [Clear Linux](https://github.com/clearlinux-pkgs/linux) - Backed by and optimized for Intel ([not being discontinued](https://community.clearlinux.org/t/is-clearlinux-being-discontinued-no/8828), contrary to rumors)

### Proton

#### Installation

If you have already installed Steam, then you already have Proton, as it is also installed by default.

#### Enabling Proton

1. Go to Steam Settings
2. Click on the "Compatibility" tab
3. Turn on "Enable Steam Play for all other titles"

You can also switch your Proton version in this tab.

<details>
  <summary>Pictured Instructions</summary>

![Step 1](/resources/steam-proton-step-1.png)

![Step 2](/resources/steam-proton-step-2.png)

![Step 3](/resources/steam-proton-step-3.png)

</details>

### Proton and Wine related tools

- [ProtonDB](https://www.protondb.com/) - Your go-to for checking compatibility of Steam games with Linux.
- [ProtonUp-Qt](https://github.com/DavidoTek/ProtonUp-Qt/) - GUI for installing and managing custom Proton and Wine versions.
- [Proton-GE](https://github.com/GloriousEggroll/proton-ge-custom) - Custom Proton with additional features.
- [WineTricks](https://github.com/Winetricks/winetricks) - Easy way to work around problems in WINE.
- [Wine-GE](https://github.com/gloriouseggroll/wine-ge-custom) - Custom WINE package, similar to Proton-GE, but made to be used with [Lutris](#game-management).

### Vulkan and DirectX Tools

- [wine-wayland](https://github.com/varmd/wine-wayland) - Allows playing Vulkan and DirectX 9/11 games with pure [Wayland](https://wayland.freedesktop.org/) and WINE.
- [dxvk](https://github.com/doitsujin/dxvk) - A Vulkan-based translation layer for Direct3D 9/10/11 that allows running 3D applications using Wine.
- [vkbasalt](https://github.com/DadSchoorse/vkBasalt) - Post-processing layer for Vulkan applications.

### Optimazation and Performance Tools

- [GameMode](https://github.com/FeralInteractive/gamemode) - Prioritize game over other tasks, similar to Windows counterpart.
- [MangoHud](https://github.com/flightlessmango/MangoHud) - An overlay for monitoring FPS, temperatures, CPU/GPU load and more.
  - [GOverlay](https://github.com/benjamimgois/goverlay) - Easy to use GUI for configuring MangoHUD.
- [Luxtorpeda](https://github.com/luxtorpeda-dev/luxtorpeda) - Steam Play compatibility tool to run games using native Linux libraries.

### Running GameMode

#### Verify whether GameMode is installed and will run correctly

```
$ gamemoded -t
```

#### Running a game

```
$ gamemoderun <game-binary>
```

#### Running a Steam game

Add the following command to the game's launch options:

``gamemoderun %command%``

### Running GameMode With MangoHUD

#### Running a game

```
$ mangohud gamemoderun <game-binary>
```

#### Running a Steam game

Add the following command to the game's launch options:

``mangohud gamemoderun %command%``

### Overclocking

### ⚠ **Warning**

> While overclocking has the potential to enhance system performance, it is strongly advised against unless you have a thorough understanding of the process. Proceeding with overclocking without adequate knowledge may lead to instability, overheating, and permanent damage to your hardware components. Exercise caution and ensure you are well-versed in the intricacies of overclocking before attempting any adjustments. If in doubt, seek guidance from experienced individuals to avoid unintended consequences and potential risks to your system.

#### Overclocking Tools

- [NVBurner](https://github.com/iloveichigo/NVBurner) - A MSI Afterburner alternative for NVIDIA users on Linux.
- [CoreCtrl](https://gitlab.com/corectrl/corectrl) - Profile based overclocking utility

## Other Tools

#### Steam-Related tools

- [SteamTinkerLaunch](https://github.com/sonic2kk/steamtinkerlaunch) - Wrapper for installing various tools, managing game launch options etc.
- [steam-cli](https://github.com/berenm/steam-cli) - Command Line Interface for Steam.
  - [steam-tui](https://github.com/dmadisetti/steam-tui) - Terminal User Interface for [steamcmd](https://developer.valvesoftware.com/wiki/SteamCMD#Linux).

#### GOG and Epic Games tools

- [Minigalaxy](https://sharkwouter.github.io/minigalaxy/) - Simple GOG client for Linux
- [Legendary](https://github.com/derrod/legendary) - CLI replacement for the Epic Games Launcher
- [Heroic Games Launcher](https://heroicgameslauncher.com/) - Epic Games, GOG and Amazon Prime Games launcher

#### Game Management

- [Lutris](https://lutris.net/) - Direct access to games from Humble, Steam, and more, as well as a game manager for all your Linux games.
- [GameHub](https://tkashkin.github.io/projects/gamehub/) - Unified library for all your games

### Game-Specific Tools

#### Minecraft Tools

- [Minecraft Launcher](https://www.minecraft.net/en-us/download/alternative) - Official vanilla Minecraft Launcher
- [Modrinth App](https://modrinth.com/app) - Interface and launcher for mods and modpacks from Modrinth
- [Prism Launcher](https://prismlauncher.org/) - Open Source Minecraft Launcher with the ability to manage multiple instances, accounts and mods. Focused on user freedom and free redistributability.

#### Roblox

- [Grapejuice](https://gitlab.com/brinkervii/grapejuice) - Roblox and Roblox Studio manager
- [Vinegar](https://vinegarhq.org/) - Bootstrapper for Roblox

#### osu!

- [osu!lazer](https://github.com/ppy/osu) - Official osu! version with support for Linux
- [osu!stable](https://github.com/NelloKudo/osu-winello) - Automatic installation script using WINE
