# particles.json

`particles.json` is the file used by LHC to control particles. It maps particle events to particle properties.
It is placed under `assets/<owner>` in resource packs. (For example, `assets/minecraft/particles.json` for the vanilla/minecraft particles.)

## File structure

```json
{
  "note": {
    "variants": {
      "instrument=0,note=0": {
        "texture": "minecraft:piano_note",
        "color": "#55dd00"
      }
    }
  }
}
```

Going line by line:

```
{                                          Main JSON object
  "note": {                                Particle event
    "variants": {                          Set of variants
      "instrument=0,note=0": {             Variant
        "texture": "minecraft:piano_note", Texture property
        "color": "#55dd00"                 Color property
      }
    }
  }
}
```

TODO expand
