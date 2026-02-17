# Dice Game (大話骰 / Liar's Dice)

Premium 3D mobile web version.

## Features

- Pure CSS 3D dice (no images, true transparency)
- Mobile portrait layout (responsive)
- Smooth roll animation with physics easing
- Touch-friendly controls
- Sound effects (Web Audio API)
- Casino-style dark green felt table
- Glass-morphism UI panels

## Files

- `index.html` - Complete game (HTML + CSS + JS in one file)

## How to Run

Open `index.html` in any modern mobile browser. Or serve locally:

```bash
cd dice-game
python3 -m http.server 8000
# Then open http://localhost:8000 on your phone (same network)
```

## Technical Details

### Dice Implementation
- CSS `transform-style: preserve-3d`
- Each die has 6 faces positioned in 3D space
- Pips are grid-positioned on each face
- Rotation achieved by setting `--final-rot` CSS variable
- Animation uses `cubic-bezier(0.2, 0.8, 0.2, 1)` for natural bounce

### Responsive Sizing
- Root variables use `clamp()` for fluid scaling
- Die size: `clamp(50px, 18vw, 80px)`
- Works on any screen width (portrait mode)

### Sound
- Web Audio API with triangle oscillators
- Toggle button to enable/disable

## Design Notes

- Color scheme: Dark green (#0d2818) felt table, bright green accents (#4caf50)
- Typography: System fonts (SF Pro, PingFang TC) for native feel
- All shadows and gradients are CSS-only

## Future Improvements

- [ ] Add scoring categories (Yahtzee/Liar's Dice rules)
- [ ] Multiplayer support (WebRTC)
- [ ] Sound customization
- [ ] Theme switcher

---

**Last updated:** 2026-02-18
**Status:** Working, basic roll functionality complete
