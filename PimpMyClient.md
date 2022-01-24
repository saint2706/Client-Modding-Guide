# How to juice up your discord client

## Step 1

A good base client. There is no elaboration. Only one choice, Kernel.

**How install?????**

> Install [Zig](https://github.com/ziglang/zig/wiki/Install-Zig-from-a-Package-Manager) > 0.90
> and Install [Gyro](https://github.com/mattnite/gyro#installation)

Then copy paste this entire block into your powershell terminal.

```ps
iwr https://get.pnpm.io/install.ps1 -useb | iex
pnpm env use --global latest
mkdir kernel
cd kernel
git clone https://github.com/kernel-mod/browser
cd browser
pnpm i
cd ..
git clone https://github.com/kernel-mod/electron
cd electron
pnpm i
pnpm run build
cd ..
```

Now head to <https://github.com/kernel-mod/installer-cli/releases> and get the one suited for your system.
Save this file to the kernel folder made in the previous step.

Now run,

```ps
installer-cli -i path/to/electron/app -k path/to/kernel/dist/folder
```

or, if you wanna be spoonfed, open your powershell terminal in the kernel folder and run

```ps
./installer.exe -i $env:LOCALAPPDATA\Discord\app-1.0.9003 -k electron\dist
```

To verify if the installation was successful, open discord, press ctrl+shift+i and see if it says "Loading Packages..." anywhere.

### Why kernel?

Because kernel offers a major performance boost and it can run packages/plugins/themes from almost all client mods.

> Powercord Plugins

<https://github.com/strencher-kernel/pc-compat>

> BetterDiscord Plugins

<https://github.com/strencher-kernel/bd-compat>

> Cumcord Plugins

<https://github.com/kernel-mod/packages/tree/master/CumcordLoader> or [Direct Download](https://download-directory.github.io/?url=https%3A%2F%2Fgithub.com%2Fkernel-mod%2Fpackages%2Ftree%2Fmaster%2FCumcordLoader)

> HolyMod Plugins

<https://github.com/HolyMod/HolyMod>

**_To install these plugins in kernel, simply clone their respective repos to the kernel\electron\dist\packages folder._**

- For cumcord you will have to unzip the archive into the packages folder since you can't clone sub-directories.

## Step 2

I assume you have installed kernel, bd-compat, pC-compat, cumcord and holymod. I also assume you have configured them and downloaded your favorite plugins and themes for them. An obvious concern is speed and performance issues due to so many compats. While kernel manages to hold its own, things can always get better. That's where openasar comes in.

**How Install??**

<https://github.com/GooseMod/OpenAsar#readme>

## Step 3

Join the servers to get support and help.

**Read the faq channels and the pinned messages in support before crying for help.**

Kernel - <https://discord.gg/8mPTjTZ4SZ>

OpenAsar - <https://discord.gg/neMncS2>

Note:-
To get support for any of the compat plugins, use the package-support channel in the kernel server.
The servers below are listed to get support from plugins that you may want to run through the compat layers.
Asking for support for the compat plugins in the servers below is not recommended and may very well get you kicked from those servers.

Cumcord - <https://discord.gg/FhHQQrVs7U>

BetterDiscord - <https://discord.com/invite/0Tmfo5ZbORCRqbAd>

powerCord - <https://discord.gg/powercord>