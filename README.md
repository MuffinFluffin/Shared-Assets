# Surume-Assets

Remote assets for the [Surume](https://github.com/MuffinFluffin/Surume) PlayStation 2 emulator for iOS.

## Structure

```
music/          — Background music tracks (MP3/WAV)
sfx/            — UI sound effects (WAV)
catalog.json    — Live music catalog manifest
```

## Music

Menu music files downloaded on-demand by the app. Tracks listed in `catalog.json` are discovered automatically on app launch.

### Adding new tracks

1. Drop the audio file into `music/`.
2. Add an entry to `catalog.json`:
   ```json
   {
     "slug": "unique-slug",
     "title": "Track Title",
     "artist": "Artist Name",
     "filename": "filename.mp3"
   }
   ```
3. Commit and push. The app will pick up the new track on next launch.

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
| `Nomos2-realplksr-x4-tile256.mlpackage` | 4x | HQ tiles |
| `PBRify-UpscalerV4-x4-tile128.mlpackage` | 4x | Game textures |
| `PBRify-RPLKSRd-V3-x4-tile64.mlpackage` | 4x | Game textures, faster |
| `PBRify-RPLKSRd-V3-x4-tile128.mlpackage` | 4x | Game textures, HQ |
| `PBRify-RPLKSRd-V3-x4-tile256.mlpackage` | 4x | Game textures, slowest |
| `PBRify-RPLKSRd-V3-x4-tile512.mlpackage` | 4x | Game textures, max tiles |

GitHub Contents API (used by the app):

`https://api.github.com/repos/MuffinFluffin/Shared-Assets/contents/neural/<folder>.mlpackage?ref=main`

Weights lineage: OpenModelDB / Real-ESRGAN family (see Surume `scripts/convert_texture_neural_coreml.py`).

