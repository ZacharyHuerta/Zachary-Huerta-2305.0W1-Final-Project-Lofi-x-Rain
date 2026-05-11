# Lofi X Rain

## Demo
Demo Video: https://youtu.be/NNChPL0rcwk

## GitHub Repository
https://github.com/ZacharyHuerta/Zachary-Huerta-2305.0W1-Final-Project-Lofi-x-Rain.git

## Description
Inspired by the long-lasting YouTube trend of lofi music streams with relaxing animations, 
Lofi X Rain is my own take on the aesthetic. It is an animated and interactive program built 
with Python and Pygame that showcases a hand-drawn study room with digital rain cascading 
outside the window. Users can cycle through rain styles, room color themes, and music tracks 
to create their own personalized virtual study space.

## Features

- **Rain Animation & Cycling**
  - A custom particle system renders digital rain using Katakana, ASCII characters, and 
    geometric shapes with glow effects. Seven unique rain styles can be cycled through 
    including Classic, Chars Only, Shapes Only, Dense, Sparse, Glitch, and Diagonal.
    Rain color themes can be cycled manually or set to auto cycle.

- **Music Cycling**
  - Using Pygame's mixer module the program plays lo-fi audio tracks loaded from a local 
    audio folder. Tracks play sequentially and can be cycled manually or set to auto cycle.

- **Room Color Cycling**
  - Six room color themes (Neutral, Lofi, Night, Sunset, Forest, Neon) are applied as 
    smooth fading overlays using transparency layers and blitting. Themes can be cycled 
    manually or set to auto cycle. The overlay excludes the window and monitor screen areas.

- **Monitor Display**
  - The in-room computer monitor displays a scrolling marquee of the currently playing 
    track name rendered in a VT323 retro terminal font, color synced to the current rain 
    theme with a subtle glow effect.

- **HUD**
  - An on screen overlay displays all current feature states and keybindings for rain theme,
    rain style, room color, and now playing track.

## Controls
| Key | Action |
|-----|---------|
| T | Cycle rain color theme |
| C | Toggle rain color auto cycle |
| S | Cycle rain style |
| R | Cycle room color theme |
| B | Toggle room auto cycle |
| M | Cycle music track |
| N | Toggle music auto cycle |
| H | Toggle HUD |
| +/- | Adjust rain speed |
| Click | Burst rain at mouse position |
| ESC | Quit |

## Challenges
- Planning the layer order of background, room image, rain surface, color overlay, 
  monitor display, and HUD while maintaining clean performance in the game loop.
- Implementing a color overlay system that smoothly fades between themes while punching 
  transparent holes over the window and monitor screen areas so rain and monitor display 
  show through correctly.
- Learning Pygame's mixer module for audio playback, sequential track progression using 
  USEREVENT, and syncing the monitor display to track changes from both manual and auto cycle.
- Coordinating multiple independent cycling systems (rain theme, rain style, room color, 
  music) each with their own manual and auto cycle states running simultaneously.
- Organizing a Python project with multiple asset types (images, audio, fonts) and keeping 
  a single project.py codebase readable and debuggable as features were added.

## Design Considerations
- The room was hand drawn in Adobe Illustrator and exported as a PNG with black used as a 
  colorkey for transparency, allowing rain and monitor content to show through the window 
  and screen areas.
- The particle system was designed to support multiple shapes and character sets with 
  per-particle glow, fade, and glitch animations.
- All cycling systems share a consistent pattern of manual key press and auto cycle toggle 
  for a unified user experience.

## Future Improvements
- Interactive animated buttons for mouse driven control instead of keyboard only.
- Additional rain styles and room color themes.
- Visualizer on the monitor screen that reacts to the music being played.
- Volume control and track shuffle mode.
- Custom user loaded audio support.

## Files
- `src/project.py` — Main program source code
- `assets/images/room.png` — Hand drawn study room illustration
- `assets/audio/` — Music tracks
- `assets/fonts/VT323-Regular.ttf` — Retro terminal font for monitor display
- `requirements.txt` — Python dependencies
