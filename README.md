# Rethement
Customize apps as you want

```json
{
  "manifest": {
    "version": "0.0.1",
    "transparency_mode": 3,
    "author": "Some author",
    "name": "Test theme"
  },
  "background": {
    //for portain device rotation
    "portain": {
      "front": {
        "size": "contain",
        "position": "center center",
        "color": "#000000FF",
        "repeat": "no-repeat",
        "mine": "jpeg"
      }
    },
    //for landscape device rotation
    "landscape": {
      "front": {
        "size": "contain",
        "position": "center center",
        "color": "#00000000",
        "repeat": "no-repeat",
        "mine": "jpeg"
      },
      "back": {
        "size": "contain",
        "position": "center center",
        "color": "#00000000",
        "repeat": "repeat-x",
        "mine": "jpeg"
      }
    },
    //black overlay opacity
    "overlay_alpha": 70,
    "blur_radius": 0
  },
  "simple_colors": {},
  "colors": {},
  "drawable_tints": {}
}
```
