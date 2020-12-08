### :warning: Warning
This project is currently in an hiatus, until some design issues are fixed. Please refer to [issues](https://github.com/MCPI-Devs/MCPIL/issues) for most common bugs. All of them are produced by the lack of a good internal design, and practically broke the Launcher.

If you want stability, please consider using MCPI-Docker directly, or an old version of this Launcher ([v0.6.2](https://github.com/MCPI-Devs/MCPIL/releases/tag/v0.6.2) would be a good choice).

This does **not** mean that the project will not be maintained anymore, so feel free to send reports, code, or other contributions.


# MCPIL
A **Broken** Minecraft Pi Launcher

[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/4335/badge)](https://bestpractices.coreinfrastructure.org/projects/4335)

![screenshot](https://raw.githubusercontent.com/Alvarito050506/MCPIL/master/screenshot.png)

A simple launcher for Minecraft: Pi Edition.


## Getting started
### Prerequisites
To use MCPIL you must have `Python >= 3.7.x` installed on your device prior to using MCPIL.

### Installation
Download and install MCPIL from the Packagecloud Debian repository:
```shell
# If you didn't add the repository yet
curl -s https://packagecloud.io/install/repositories/Alvarito050506/mcpi-devs/script.deb.sh | sudo bash

# Now the actual installation
sudo apt-get install mcpil
```

## Features
 + Switch between Minecraft Pi and Minecraft Pocket Edition
 + Username changing
 + Skin changing
 + Mod loading
 + Mod API
 + Mod compilation
 + World settings (gamemode and name) changing
 + Join non-local servers
 + Coming soon: More stuff 

## Usage
Launch the MCPIL desktop file or run the `mcpil` command folder as following to see the magic! :wink:
```shell
mcpil # Yes, simple as this
```

## API
The API documentation was moved to the [ModPi repo](https://github.com/MCPI-Devs/modpi).

The support for the old API was **dropped** in the **v0.5.0 release**! It is recommended to use the new ModPi API. However, the old API documentation is still avaiable [here](https://github.com/MCPI-Devs/MCPIL/tree/3470fb73b81510f5e819a34c04cca6f86457c2b2#api).

## Mod compilation
To compile (compress) a Python mod, run the `mcpim` command passing the filename of the mod as the first argument. For example:
```shell
mcpim ./example.py
```
This will produce an `example.mcpi` mod file.

## Troubleshooting
If you get the `module not found: _tkinter` error, or something of the sort, you can use Homebrew to install a custom tap made by @gamer4life1.
```shell
# First, install brew (If you don't have it already, also make sure to install in /home/linuxbrew/.linuxbrew)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
# Then, apply the custom tap
brew tap gamer4life1/mcpi-tap
# Install gcc (a needed dependency)
brew install gcc
# Follow caveats for gcc (something like example)
export LDFLAGS="-L/home/linuxbrew/.linuxbrew/opt/isl@0.18/lib"
export CPPFLAGS="-I/home/linuxbrew/.linuxbrew/opt/isl@0.18/include"
# Install the custom formula of python (Ignore errors if they say that the system cannot find the bottle, it will compile from source)
brew install custompython
# Finally, add it to your PATH so it is first in your PATH
export PATH="/usr/local/opt/custompython/bin:$PATH"
# Add above to bashrc to load automatically
```

## Thanks
To [@Phirel](https://www.minecraftforum.net/members/Phirel) for his Pi2PE (a.k.a. "survival") patch, and to [@TheBrokenRail](https://thebrokenrail.com) for MCPI-Docker. These two projects were/are highly used & abused by MCPIL :wink:.

To everyone who has or had interest on the project, including MCPI Revival members.

## Licensing
All the code of this project is licensed under the [GNU General Public License version 2.0](https://github.com/Alvarito050506/MCPIL/blob/master/LICENSE) (GPL-2.0).

All the documentation of this project is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0) license.

![CC BY-SA 4.0](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)
