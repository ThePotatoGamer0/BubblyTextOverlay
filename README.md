# BubblyTextOverlay

A highly customizable, bubbly text overlay for use as a Browser Source in OBS, Streamlabs, or any other streaming software. The text, styling, and animation can be controlled entirely through URL parameters.

Hosted at: [https://potatogamer.uk/BubblyTextOverlay/](https://potatogamer.uk/BubblyTextOverlay/)

## URL Format

The base URL is followed by a `?` and a series of `key=value` pairs, separated by an ampersand `&`.

### Example
```
https://potatogamer.uk/BubblyTextOverlay/?text=Fully Customizable!&fontFamily='Montserrat',sans-serif&fontSize=70&fontWeight=900&color=%23FFD700&duration=2&stagger=0.07&bounce=-50
```
---

## All Parameters

### Text & Style Parameters

| Parameter | Description | Default Value | Example |
| :--- | :--- | :--- | :--- |
| `text` | The text you want to display. URL encoding handles spaces automatically. | `Hello World` | `text=Stream Starting Soon` |
| `fontFamily`| Sets the font. Available fonts: `Inter`, `Montserrat`, `Roboto`, `Lato`, `Oswald`, `Source Code Pro`. | `'Inter', sans-serif`| `fontFamily='Roboto',sans-serif`|
| `fontSize` | The size of the font in pixels. Do not include "px". | `80` | `fontSize=120` |
| `fontWeight`| Sets the thickness/weight of the font. | `bold` | `fontWeight=900` |
| `color` | The color of the text. Can be a name or a hex code. | `white` | `color=red` or `color=%23FFD700` |
| `customFontUrl` | URL to a custom font file (`.woff2`, `.ttf`). Overrides `fontFamily`. | `none` | `customFontUrl=https://your.cdn/font.woff2` |

**Note on Colors:** For hex color codes, you **must** replace the `#` symbol with `%23` in the URL for it to work correctly.

**Note on Custom Fonts:** Simply provide a direct link to a font file. For best performance and compatibility, the `.woff2` format is recommended. This will automatically override the `fontFamily` parameter.

### Animation Parameters

| Parameter | Description | Default Value | Example |
| :--- | :--- | :--- | :--- |
| `duration` | The time in seconds for one complete bounce animation cycle. | `1.5` | `duration=3` (slower) |
| `stagger` | The delay in seconds between each letter starting its animation. | `0.05` | `stagger=0.1` (more spread out) |
| `bounce` | How high the letters bounce as a percentage of their height. Use negative values to go up. | `-40` | `bounce=-60` (higher bounce) |
