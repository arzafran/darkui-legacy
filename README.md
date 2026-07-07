# darkUI

darkUI is a Darkroom-themed fork of [MinUI](https://github.com/shauninman/MinUI-Legacy-RG35XX), Shaun Inman's focused custom launcher for the original Anbernic RG35XX (2022, Actions ATM7039S — not the Plus/H/H700 variants).

All launcher and frontend design and engineering is [Shaun Inman](https://github.com/shauninman)'s work; this fork rebrands the boot logo, install screens, and launcher chrome. Upstream is archived, so this fork also serves as a pinned, buildable snapshot.

<img src="github/minui-main.png" width=320 /> <img src="github/minui-menu-gbc.png" width=320 />

## Features

- Simple launcher, simple SD card
- No settings or configuration
- No boxart, themes, or distractions
- Consistent in-emulator menu with quick access to save states, disc changing, and emulator options
- Automatic sleep, power-off, and resume
- Streamlined emulator frontend (minarch + libretro cores)
- Darkroom boot logo and branding

## Building

Requires the [union-rg35xx-toolchain](https://github.com/darkroomengineering/union-rg35xx-toolchain) Docker image (x86_64 buildroot — on Apple Silicon build and run with `--platform linux/amd64`).

Clone this repo into the toolchain's `./workspace`, then inside the container shell:

```sh
cd ~/workspace/darkui
PLATFORM=rg35xx make
```

Release zips land in `./releases`. The payload zip keeps the internal name `MinUI.zip` so existing MinUI chainloaders pick it up as an update.

## Installing

See `skeleton/BASE/README.txt` (shipped as `README.txt` in the base release zip).
