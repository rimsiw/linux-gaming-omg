# linux-gaming-omg



## Getting started

It is a list of tools for linux gaming, as well as a guide for setting up your basic gaming enviroment.

### Explaining Terms

_**Linux**_ - Shortened term for GNU/Linux, sorry Stallman

_**Kernel**_ - Core of an operating system

_**Distro**_ - Distribution of linux, commonly reffered as distro.

### What Distribution should I pick for linux gaming?

Honestly? It is entirely your choice and what you prefer. It is not possible to recommend a single distro for everyone, however I'll list here most popular, most optimized and community favourites.

#### [Arch](https://archlinux.org/) based

Arch-based distros are the ones with one of the best support for gaming, but it may be overwhelming for beginners. If you don't know what you are doing, I wouldn't recommend any of those listed here.

Arch-based distros are intended to be used by advanced or semi-advanced users. Those are often reffered to as "rolling-release" which means that packages and kernel is always up-to-date

* [Arch Linux (duh)](https://archlinux.org/)
* [EndeavourOS](https://endeavouros.com/) - Commonly known as user-friendly Arch Linux. It is packaged with an installer.
* [Manjaro](https://manjaro.org/) - Relatively easy to use Arch Linux. Comes with installer. Updates for Manjaro may not be always on time, due to their own [release system](https://wiki.manjaro.org/index.php/Manjaro:A_Different_Kind_of_Beast#Dedicated_Repositories).
* [Garuda Linux](https://garudalinux.org/) - Gaming linux distro.

#### [Debian](https://www.debian.org/) and [Ubuntu](https://ubuntu.com/) based.

Commonly known as the best linux distributions for beginners, Debian-based distributions are one of the most popular choices amongst them. However, they may come with outdated packages, as they offer stable-release system.

* [Debian](https://www.debian.org/)
* [Ubuntu](https://ubuntu.com/) - Most popular linux distribution amongst beginners.
* [LinuxMint](https://www.linuxmint.com/) - Easy to use and friendly distribution based on Ubuntu.
* [Pop_OS!](https://pop.system76.com/) - Made for beginners. Based on Ubuntu.

#### Other linux distributions.

* [Gentoo](https://www.gentoo.org/) - For advanced users. Flexible and source-based distro.
* [Funtoo](https://www.funtoo.org/Welcome) - For advanced users. Evolution of Gentoo. Optimized for the best performance.
* [NixOS](https://nixos.org/) - For advanced users. Linux distribution based on Nix Package Manager
* [OpenSUSE](https://www.opensuse.org/) - Fast and stabilized rolling-release distribution.

### How good is gaming on Linux? How does it compare to Windows gaming?

While a lot of games are programmed only for Windows PC, most of them run perfectly fine on linux. That is thanks to awesome [WINE](https://www.winehq.org/), which translates Windows code to a Linux one. And no, it is not in fact an emulator.

Answer however may get a little bit tricky when it comes to performance, cause as everything in life, it depends. Native Linux games or those which were programmed for linux should run without any performance issues on Linux, even in some cases surpassing Windows version. However when running games not intended for Linux, answer may vary and it depends on your distro, installed tools, game, compatibility tool and many more. However we can tweak that to make sure your game runs at best possible performance.

## Tools and Applications

That being said, we can now make our way to enhancing your experience.

### Which kernel should i use?

Most of the time you don't need to change your kernel. However if performance is important to you, I recommend [linux-zen](https://github.com/zen-kernel/zen-kernel).

### Proton

Proton is a compatibility tool developed by Valve Software. It is based on previously mentioned, WINE.

#### How to install Proton?

If you use Steam (and you probably do), after installing it on your OS, Proton would be installed as well.

#### How to enable Proton for Steam games?

Go to Steam Settings, click on "Compatibility" tab, and check the box stating "Enable SteamPlay for all other titles". Here you can change your version of Proton as well.

![Step 1](/resources/2023-12-26_22-09.png)
![Step 2](/resources/2023-12-26_22-09_1.png)
![Step 3](/resources/2023-12-26_22-10.png)

From this point you can also change your Proton version.

#### Proton related tools.

* [ProtonDB](https://www.protondb.com/) - Your go-to for checking compatibility of Steam games with Linux.
* [ProtonUp-Qt](https://github.com/DavidoTek/ProtonUp-Qt/) - GUI for installing and managing custom Proton and Wine versions.
* [Proton-GE](https://github.com/GloriousEggroll/proton-ge-custom) - Custom Proton with additional features.

### Vulkan & DirectX

#### Vulkan and DirectX tools

* [wine-wayland](https://github.com/varmd/wine-wayland) - Allows running Vulkan and DirectX games with pure wine.
* [dxvk](https://github.com/doitsujin/dxvk) - Allows DirectX games to use 3D.
* [vkbasalt](https://github.com/DadSchoorse/vkBasalt) - Post-processing layer for Vulkan games.

### Optimazation and Performance

#### Tools

* [GameMode](https://github.com/FeralInteractive/gamemode) - System optimizer. Highly recommended.
* [MangoHUD](https://github.com/flightlessmango/MangoHud) - Game usage and FPS monitor.
    * [GOverlay](https://github.com/benjamimgois/goverlay) - Easy to use GUI for configuring MangoHUD
* [Luxtorpeda](https://github.com/luxtorpeda-dev/luxtorpeda) - Steam Play compatibility tool which runs games using native Linux libralies.

##### Gamemode Usage

Mentioned in previous section, gamemode is a great way to improve your performance in games.

* *Verify if the configuration files are working*
```
$ gamemoded -t
```

* *Run a single game*
```
$ gamemoderun ./GAME
```

* *Run with a single Steam game*

Add to launch parameters of your game the following:
```
gamemoderun %command%
```

###### With MangoHUD

* *Run a single game*
```
$ mangohud gamemoderun [GAME]
```

* *Run a single Steam game*
```
mangohud gamemoderun %command%
```

### Other Tools

#### Steam-Related tools

* [SteamTinkerLaunch](https://github.com/sonic2kk/steamtinkerlaunch) - Easy to use GUI which may be used to to configure GameScope, MangoHUD, Vortex Mod Manager and more.
* [steam-cli](https://github.com/berenm/steam-cli) - Command Line Interface for Steam.
    * [steam-tui](https://github.com/dmadisetti/steam-tui) - Terminal User Interface for Steam, based on ``steam-cli``

#### GOG and Epic Games tools

* [Minigalaxy](https://sharkwouter.github.io/minigalaxy/) - Simple GOG client for Linux
* [HeroicGamesLauncher](https://heroicgameslauncher.com/) - Epic Games, GOG and Amazon Prime Gaming client

#### Game Management
* [Lutris](https://lutris.net/) - Direct access to games from Humble, Steam and more, as well as game manager for all your Linux games.
* [GameHub](https://tkashkin.github.io/projects/gamehub/) - Unified library for your games.
* [Playnite](https://playnite.link/) - Library manager
    * [Playnite Plugins](https://playnite.link/addons.html)