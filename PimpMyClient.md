# How to juice up your Discord Client

***Installation method has been primarily made keeping Windows in mind but if you use any other OS, usually replacing the file path works***

Discord Installation Folders:

**Windows** - /%LOCALAPPDATA%/discord/app-1.0.xx

**Linux** - /usr/share/discord

**Mac** - /Library/Application Support/Discord

<https://savelocation.net/discord> for more info.

## Step 1

A good base client. There is no elaboration. Only one choice, Kernel.

**How install?????**

You will need a recent [**node.js**](https://nodejs.org/) version, with [**pnpm**](https://pnpm.io) installed, regardless of the way you install Kernel.
To do that, after installing [**node.js**](https://nodejs.org/) open a terminal and run:

```sh
npm i -g pnpm
```

### Recommended Method

#### Windows

- Download the latest [Kernel-Windows.exe](https://github.com/strencher-kernel/gui-installer/releases/tag/v1.0.1).

- Make a folder "kernel" and place the downloaded installer in it.

- Close discord completely.

- Run the installer, click [Install](https://i.imgur.com/SJjbt0P.png) and then it should [automatically detect](https://i.imgur.com/hOQFuSu.png) the path to your discord installation.

- If it didn't detect the path to your discord installation, then click on browse and navigate to C:\Users\%username%\Appdata\Local\Discord\app-1.0.xx.

- Click on [Kernel Path](https://i.imgur.com/zH6bBgf.png) and select the folder "kernel" from the second step.

- Then click on Install. Make sure both the toggles are set to "On".

To verify if the installation was successful, open discord, press [ctrl+shift+i](https://pastebin.com/6yyJgwGS) and see if it says "Loading Packages..." anywhere.

#### Arch

You can run this handy script:
- <https://github.com/Scraft161/scripts/blob/master/initcord>. (This also installs OpenAsar).

### The Old Method

> Install [Zig](https://github.com/ziglang/zig/wiki/Install-Zig-from-a-Package-Manager) > 0.90
> and Install [Gyro](https://github.com/mattnite/gyro#installation)

Copy and paste this entire block into your PowerShell terminal.

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
Save this file to the Kernel folder made in the previous step.

Now run:

```ps
installer-cli -i path/to/electron/app -k path/to/kernel/dist/folder
```

or if you wanna be spoonfed, open your PowerShell terminal in the Kernel folder and run:

```ps
./installer.exe -i $env:LOCALAPPDATA\Discord\app-1.0.9004 -k electron\dist
```

### Why Kernel?

Because Kernel offers a major performance boost and can run packages/plugins/themes from almost all client mods.

Here are the major compatibility layers to run:

> Powercord Plugins

<https://github.com/strencher-kernel/pc-compat>

> BetterDiscord Plugins

<https://github.com/strencher-kernel/bd-compat>

> Cumcord Plugins

<https://github.com/kernel-mod/packages/tree/master/CumcordLoader> or [Direct Download](https://download-directory.github.io/?url=https%3A%2F%2Fgithub.com%2Fkernel-mod%2Fpackages%2Ftree%2Fmaster%2FCumcordLoader)

***To install these in Kernel, simply git clone their respective repos to your Kernel packages folder.***

- For Cumcord, you will have to unzip the archive into the packages folder since you can't git clone sub-directories.

## Step 2

I assume you have already installed Kernel, bd-compat, pc-compat and Cumcord. I also assume you have configured them and downloaded your favorite plugins and themes for them. An obvious concern is speed and performance issues due to so many compats. While Kernel manages to hold its own, things can always get better. That's where OpenAsar comes in.

**How Install??**

<https://openasar.dev>

> If using with kernel, do remember to rename the installed `app.asar` in your Discord install's folder to `app-original.asar`.

## Step 3

Join these servers to get support and help.

**Read the FAQ channels and the pinned messages in the support channels before crying for help.**

Kernel - <https://discord.gg/8mPTjTZ4SZ>

OpenAsar - <https://discord.gg/neMncS2>

Note:-
To get support for any of the compat plugins, use the [**#package-support**](https://discord.com/channels/891039687785996328/891053581136982056) channel in the Kernel server.
The servers below are listed to get support from plugins that you may want to run through the compat layers.
Asking for support for the compat plugins in the servers below is not recommended and may get you kicked from those servers.

Cumcord - <https://discord.gg/FhHQQrVs7U>

BetterDiscord - <https://discord.com/invite/0Tmfo5ZbORCRqbAd>

Powercord - <https://discord.gg/powercord>
