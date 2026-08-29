# Games

Original homebrew titles by **MuffinFluffin**, one folder per console. Every title
here is written from scratch and carries no third-party trademarks, so it can ship
with the apps and be handed to App Review as something to press play on.

The in-app metadata lists an in-fiction developer and publisher per title. The real
author of every title in this folder is MuffinFluffin.

Apps read `games.json` to list what is available for the console they run, then
download a title's files from its folder.

```
games/games.json                        manifest, one entry per console
games/<console>/README.md               console, app, core, accepted files
games/<console>/<Title>/game.json       metadata for one title
games/<console>/<Title>/cover.png       cover art
games/<console>/<Title>/<Title>.cue     boot file
```

## Consoles

| Console | Folder | App | Core | Titles |
|---|---|---|---|---|
| PlayStation | [`playstation`](playstation/) | Sakura | Beetle PSX | 5 |
| PlayStation 2 | [`playstation-2`](playstation-2/) | Surume, Surume Lite | PCSX2 | — |
| PlayStation 3 | [`playstation-3`](playstation-3/) | Surume, Surume3 | RPCS3 | — |
| PlayStation 4 | [`playstation-4`](playstation-4/) | Surume, Magnus | shadPS4 | — |
| PlayStation 5 | [`playstation-5`](playstation-5/) | Magnus | Silva | — |
| PlayStation Portable | [`psp`](psp/) | Sakura | PPSSPP | 3 |
| PlayStation Vita | [`ps-vita`](ps-vita/) | Suno, Surume | Vita3K | — |
| GameCube | [`gamecube`](gamecube/) | Fin | Dolphin | — |
| Wii | [`wii`](wii/) | Fin | Dolphin | — |
| Triforce | [`triforce`](triforce/) | Fin | Dolphin | — |
| Wii U | [`wii-u`](wii-u/) | TailFin | Cemu | — |
| Nintendo 3DS | [`nintendo-3ds`](nintendo-3ds/) | Chronic | azahar | — |
| Game Boy | [`game-boy`](game-boy/) | Fin, MicroFin | mGBA | — |
| Game Boy Color | [`game-boy-color`](game-boy-color/) | Fin, MicroFin | mGBA | — |
| Game Boy Advance | [`game-boy-advance`](game-boy-advance/) | Fin, MicroFin | mGBA | — |
| Dreamcast | [`dreamcast`](dreamcast/) | Plume | flycast | — |
| Xbox | [`xbox`](xbox/) | Monolith | xemu | — |
| Xbox 360 | [`xbox-360`](xbox-360/) | Astra | Xenia | — |

## Raw download

`https://raw.githubusercontent.com/MuffinFluffin/Shared-Assets/main/games/<console>/<Title>/<file>`

## License

Titles and cover art are original work by MuffinFluffin, released CC0 1.0.
Tooling is GPL-3.0+.
