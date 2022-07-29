# Rethement
Customize apps as you want

Theme files structure:
```
theme.zip ┐
          ├ drawables ┐
          │           ├ ic_call_24dp.svg
          │           ├ ic_notification_24dp.svg
          │           ├ ic_play_arrow.svg
          │           └ and etc...
          │
          ├ background ┐
          │            ├ pFront.png
          │            ├ pBack.png
          │            ├ lFront.png
          │            └ lBack.png
          │
          ├ fonts ┐
          │       ├ w100.ttf
          │       ├ w200.ttf
          │       ├ w300.ttf
          │       ├ ...
          │       ├ w700.ttf
          │       ├ w800.ttf
          │       └ w900.ttf
          │
          └ manifest.json
```

Example for `manifest.json`
```json
{
  "manifest": {
    "author": "username#1000",
    "version": "0.0.1",
    "name": "My theme",
    "transparency_mode": 3,
    "license": "GNU",
    "updater": "-",
    "tags": ["anime", "blue", "vanilla", "animated", "night", "stars"],
    "rating": 0
  },
  "background": {
    "overlay_alpha": 112,
    "blur_radius": 4,
    "portain": {
      "front": {
        "size": "contain",
        "position": "center center",
        "color": "#000000FF",
        "repeat": "no-repeat",
        "mine": "jpeg"
      }
    },
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
    }
  },
  "colors": {
    "simple_colors": {},
    "colors": {},
    "drawable": {}
  },
  "fonts":{
    "all": "w400",
    "w100": false,
    "w200": false,
    "w300": false,
    "w400": true,
    "w500": false,
    "w600": false,
    "w700": false,
    "w800": false,
    "w900": false
  }
}
```

### Manifest
```
manifest ┐
         ├ author (since we can't use ID to get information, we just use username (for example username#1000))
         ├ version (0.0.1 - major minor patch)
         ├ transparency_mode (0 - none, 1 - chat, 2 - chat & settings, 3 - full, 4 - display homescreen wallpaper (including live wallpaper))
         ├ name (theme name)
         ├ licence (license for theme (MIT, GNU and etc.))
         ├ updater (raw url to .json file (only github and gitlab))
         ├ tags (tags that describe your theme)
         └ rating (from 0 to 5.
                        5 - Adults Only 18+ (Content suitable only for adults ages 18 and up. May include prolonged scenes of intense violence, graphic sexual content and/or gambling with real currency),
                        4 - Mature 17+ (Content is generally suitable for ages 17 and up. May contain intense violence, blood and gore, sexual content and/or strong language)
                        3 - Teen (Content is generally suitable for ages 13 and up. May contain violence, suggestive themes, crude humor, minimal blood, simulated gambling and/or infrequent use of strong language)
                        2 - Everyone 10+ (Content is generally suitable for ages 10 and up. May contain more cartoon, fantasy or mild violence, mild language and/or minimal suggestive themes)
                        1 - Everyone (Content is generally suitable for all ages. May contain minimal cartoon, fantasy or mild violence and/or infrequent use of mild language)
                        0 - not specified
                   )

background ┐
           ├ portain ┐
           │         ├ front ┐
           │         │       ├ size (cover, contain or auto)
           │         │       ├ position (may be just left,right,bottom,top or in % (50% 50%))
           │         │       ├ color (int32 argb (alpha, red, green, blue))
           │         │       ├ repeat (no-repeat, repeat (x,y), repeat-x, repeat-y)
           │         │       └ mine (file format (jpeg, png, webp, gif, mp4))
           │         │
           │         └ back ┐
           │                ├ size (cover, contain or auto)
           │                ├ position (may be just left,right,bottom,top or in % (50% 50%))
           │                ├ color (int32 argb (alpha, red, green, blue))
           │                ├ repeat (no-repeat, repeat (x,y), repeat-x, repeat-y)
           │                └ mine (file format (jpeg, png, webp, gif, mp4))
           │
           ├ overlay_alpha (opacity of black overlay layer from 0 to 255)
           └ blur_radius (blur image from 0 to 100)

colors ┐
       ├ simple_colors (int32 argb) ┐
       │                            ├ link
       │                            ├ background (front image -> back image -> background)
       │                            ├ statusbar
       │                            ├ active_channel
       │                            └ and etc...
       │
       ├ colors (int32 argb) ┐
       │                     ├ chat_media_view_stroke
       │                     ├ design_icon_tint
       │                     ├ focus_primary_160
       │                     ├ link_360
       │                     └ and etc...
       │
       └ drawable (int32 argb) ┐
                               ├ abc_item_background_holo_light
                               ├ design_snackbar_background
                               ├ exo_notification_fastforward
                               ├ ic_clock_black_24dp
                               └ and etc...

fonts (.ttf format) ┐
                    ├ default (string (can be w100 to w900))
                    ├ w100 (boolean (if has .ttf file for font weight 100)
                    ├ w200
                    ├ w300
                    ├ ...
                    ├ w700
                    ├ w800
                    └ w900
                    
dwawables (string array list) - [
                                    "images_native_icons_ic_1password_24px",
                                    "images_native_icons_ic_arrow_forward_24px",
                                    "images_native_icons_ic_group_dm"
                                    ...
                                ]
``` 
