# particles.json

`particles.json` is the file used by LHC to control particles. It maps particle events to particle properties.
It is placed under `assets/<owner>` in resource packs. (For example, `assets/minecraft/particles.json` for the vanilla/minecraft particles.)

## File structure

The particles.json file contains particle events, and maps them to their properties based on variants. The way variants are implemented in particles.json is more powerful than 
blockstate variants, allowing arbitrary keys and values. Particle textures go in `assets/<owner>/particles/<texture_name>.png` and animation data go in 
`assets/<owner>/particles/<texture_name>.json`.

The variants are tested from less specific to more specific. By testing the less specific first, the more specific can override the less specific.

Properties are \<insert word here\>, that is, if you have a variant for `"x": 1` setting texture `mytex`, and a variant for `"y": 20` setting color `#FF0000`, and both variants match, 
then the resulting particle uses texture `mytex` and color `#FF0000`.

### Example

```json
{
  "note": {
    "variants": [
      {
        "variant": {
          "instrument": 0,
          "note": 0
        },
        "texture": "minecraft:piano_note",
        "color": "#55dd00"
      }
    ]
  }
}
```

In this example, a `note` particle spawned with `instrument` set to `0` and `note` set to `0` would use texture `minecraft:piano_note` and color `#55dd00`.

### Example 2

```json
{
  "note": {
    "variants": [
      {
        "variant": {"instrument": 0},
        "texture": "minecraft:piano_note"
      },
      {
        "variant": {"instrument": 1},
        "texture": "minecraft:bassdrum_note"
      },
      {
        "variant": {"instrument": 2},
        "texture": "minecraft:snare_note"
      },
      {
        "variant": {"instrument": 3},
        "texture": "minecraft:clicks_note"
      },
      {
        "variant": {"instrument": 4},
        "texture": "minecraft:bassguitar_note"
      },
      {
        "variant": {"note": [0, 24]},
        "color": "#55dd00"
      },
      {
        "variant": {"note": 1},
        "color": "#7ec400"
      },
      {
        "variant": {"note": 2},
        "color": "#a4a400"
      },
      {
        "variant": {"note": 3},
        "color": "#c47e00"
      },
      {
        "variant": {"note": 4},
        "color": "#dd5500"
      },
      {
        "variant": {"note": 5},
        "color": "#ed2c00"
      },
      {
        "variant": {"note": 6},
        "color": "#f30606"
      },
      {
        "variant": {"note": 7},
        "color": "#ed002c"
      },
      {
        "variant": {"note": 8},
        "color": "#dd0055"
      },
      {
        "variant": {"note": 9},
        "color": "#c4007e"
      },
      {
        "variant": {"note": 10},
        "color": "#a400a4"
      },
      {
        "variant": {"note": 11},
        "color": "#7e00c4"
      },
      {
        "variant": {"note": 12},
        "color": "#5500dd"
      },
      {
        "variant": {"note": 13},
        "color": "#2c00ed"
      },
      {
        "variant": {"note": 14},
        "color": "#0606f3"
      },
      {
        "variant": {"note": 15},
        "color": "#002ced"
      },
      {
        "variant": {"note": 16},
        "color": "#0055dd"
      },
      {
        "variant": {"note": 17},
        "color": "#007ec4"
      },
      {
        "variant": {"note": 18},
        "color": "#00a4a4"
      },
      {
        "variant": {"note": 19},
        "color": "#00c47e"
      },
      {
        "variant": {"note": 20},
        "color": "#00dd55"
      },
      {
        "variant": {"note": 21},
        "color": "#00ed2c"
      },
      {
        "variant": {"note": 22},
        "color": "#06f306"
      },
      {
        "variant": {"note": 23},
        "color": "#2ced00"
      }
    ]
  }
}
```

In this example, a `note` particle spawned with `instrument` set to `0` and `note` set to `0` would use texture `minecraft:piano_note` and color `#55dd00`. A `note` particle spawned 
with `instrument` set to `1` and `note` set to `0` would use texture `minecraft:bassdrum_note` and color `#55dd00`. And so on.
