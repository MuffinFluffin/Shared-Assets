
## Structure

```
music/          — Background music tracks (MP3/WAV)
sfx/            — UI sound effects (WAV)
catalog.json    — Live music catalog manifest
```
### Current tracks

| Track | Artist | Source | License |
|-------|--------|--------|---------|
| Butterflow Menu Music Theme | Nomagician | Freesound.org | CC BY 4.0 |
| Video Game Menu Music | magmadiverrr | Freesound.org | CC0 1.0 |
| Piano Loops 188 Octave Down | josefpres | Freesound.org | CC0 1.0 |
| Piano Loops 198 Octave Down | josefpres | Freesound.org | CC0 1.0 |
| Piano Loops 201 Octave Short | josefpres | Freesound.org | CC0 1.0 |
| Piano Loops 207 Efect 2 Octave | josefpres | Freesound.org | CC0 1.0 |
| Sergio's Magic Dustbin | Kevin MacLeod | incompetech.com | CC BY 4.0 |
| Mesmerizing Galaxy | Kevin MacLeod | incompetech.com | CC BY 4.0 |
| Adventures in Adventureland | Kevin MacLeod | incompetech.com | CC BY 4.0 |
| Hot Start | MuffinFluffin | Original | CC0 1.0 |
| Matsuri | MuffinFluffin | Original | CC0 1.0 |
| Funk Of Liberation - UP B! | MuffinFluffin | Original | CC0 1.0 |
| Blue Bell - Tempo | MuffinFluffin | Original | CC0 1.0 |
| Matsuri - Core | MuffinFluffin | Original | CC0 1.0 |
| Blue Bell - Chill | MuffinFluffin | Original | CC0 1.0 |
| Blue Bell - Bitz | MuffinFluffin | Original | CC0 1.0 |
| GEAR-UP! - Clear | MuffinFluffin | Original | CC0 1.0 |
| GEAR-UP - Core | MuffinFluffin | Original | CC0 1.0 |

## SFX

UI click/navigation sounds. Auto-downloaded silently on first app launch.

| File | Source | License |
|------|--------|---------|
| sfx_confirm.wav | Christopherderp — Freesound | CC0 1.0 |
| sfx_navigate.wav | Foxfire- — Freesound | CC0 1.0 |
| sfx_back.wav | sfx_navigate reversed | CC0 1.0 |
| sfx_toggle.wav | mellau — Freesound | CC0 1.0 |
| sfx_error.wav | (placeholder) | — |

## catalog.json

The app fetches this file on every launch to discover new tracks without requiring an app update.

```json
{
  "tracks": [
    {
      "slug": "butterflow-menu-music-theme",
      "title": "Butterflow Menu Music Theme",
      "artist": "Nomagician",
      "filename": "butterflow-menu-music-theme.mp3"
    }
  ]
}
```

## License

Audio files retain their original licenses (CC BY 4.0, CC0 1.0, etc.) as noted above. This repository structure and tooling is GPL-3.0+.

## Neural (Core ML texture upscalers)

Optional `.mlpackage` bundles for on-device download in Surume Settings.

| Package | Scale | Notes |
|---------|-------|-------|
| `Sakura-Fast.mlpackage` | 2x | Lite tile128 |
| `Sakura-x2-tile128.mlpackage` | 2x | |
| `Sakura-x2-tile256.mlpackage` | 2x | HQ tiles |
| `Sakura-x4-tile128.mlpackage` | 4x | |
| `Nomos2-realplksr-x4-tile64.mlpackage` | 4x | Faster |
| `Nomos2-realplksr-x4-tile192.mlpackage` | 4x | Balanced tiles |
| `Nomos2-realplksr-x4-tile256.mlpackage` | 4x | HQ tiles (legacy) |
| `PBRify-UpscalerV4-x4-tile128.mlpackage` | 4x | Game textures |
| `PBRify-RPLKSRd-V3-x4-tile64.mlpackage` | 4x | Game textures, faster |
| `PBRify-RPLKSRd-V3-x4-tile128.mlpackage` | 4x | Game textures, HQ |
| `PBRify-RPLKSRd-V3-x4-tile192.mlpackage` | 4x | Game textures, balanced |
| `PBRify-RPLKSRd-V3-x4-tile256.mlpackage` | 4x | Game textures (legacy) |
| `PBRify-RPLKSRd-V3-x4-tile512.mlpackage` | 4x | Game textures, max tiles |
| `UltraSharpV2-Lite-x4-tile128.mlpackage` | 4x | Sharp detail |

GitHub Contents API (used by the app):

`https://api.github.com/repos/MuffinFluffin/Shared-Assets/contents/neural/<folder>.mlpackage?ref=main`

Weights lineage: OpenModelDB / Real-ESRGAN family (see Surume `scripts/convert_texture_neural_coreml.py`).

