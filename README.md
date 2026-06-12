# Golden Hour Waves 2 🌅🌊

**Golden Hour Waves 2** is an interactive canvas ocean experiment built for CodePen and GitHub Pages. It creates a full-screen animated sea scene with wind interaction, splash particles and a cinematic day/night atmosphere.

Live demo:

**https://laurandreea10.github.io/Golden-hour-waves-2/**

## Overview

This project uses a minimal HTML structure, a full-screen `<canvas>` and vanilla JavaScript to draw an animated ocean in real time. The scene responds to pointer movement and click/tap interactions.

The interaction model is simple:

- move the mouse or pointer to stir the wind;
- click or tap to create a splash;
- watch the ocean shift through a day → sunset → night → dawn cycle.

## CodePen Panels

### HTML

```html
<canvas id="c"></canvas>
<div class="hint">move to stir the wind · click for a splash 🌊</div>
```

### CSS

```css
* { margin: 0; }

html, body {
  height: 100%;
  overflow: hidden;
  background: #04101e;
}

#c {
  position: fixed;
  inset: 0;
  display: block;
  cursor: crosshair;
  touch-action: manipulation;
}

.hint {
  position: fixed;
  left: 50%;
  bottom: 22px;
  transform: translateX(-50%);
  font: 500 13px/1 system-ui, sans-serif;
  letter-spacing: .06em;
  color: rgba(255, 255, 255, .85);
  background: rgba(4, 16, 30, .35);
  backdrop-filter: blur(6px);
  padding: 9px 16px;
  border-radius: 999px;
  pointer-events: none;
  animation: hintFade 9s ease forwards;
}

@keyframes hintFade {
  0%, 70% { opacity: 1; }
  100% { opacity: 0; }
}

@media (prefers-reduced-motion: reduce) {
  .hint { animation: none; }
}
```

## JavaScript Features

The JavaScript layer powers the interactive visual system:

- five procedural wave layers;
- full day/night color cycle;
- sun, moon, clouds, stars and birds;
- animated surfer emoji on the middle wave;
- foam particles;
- bioluminescent night sparks;
- ambient swell impulses;
- pointer-driven wind;
- click/tap splash impulses;
- high-DPI canvas support;
- `prefers-reduced-motion` support.

## Tech Stack

- HTML5
- CSS3
- Canvas API
- Vanilla JavaScript
- GitHub Pages

## Project Structure

```txt
Golden-hour-waves-2/
├── index.html
└── README.md
```

## How to Run Locally

Clone the repository:

```bash
git clone https://github.com/LaurAndreea10/Golden-hour-waves-2.git
cd Golden-hour-waves-2
```

Open `index.html` in your browser.

No install step is required.

## Accessibility Notes

The project respects `prefers-reduced-motion` for the hint animation. Because the main experience is a visual canvas animation, consider adding an off-screen text description if you extend it for a more complete accessibility layer.

## Portfolio Use

This project works well as a creative coding / CodePen challenge piece because it demonstrates:

- canvas drawing;
- animation timing;
- procedural motion;
- interaction handling;
- responsive full-screen rendering;
- visual storytelling through code.

## Author

Created by **Laura Andreea**  
GitHub: [@LaurAndreea10](https://github.com/LaurAndreea10)

## License

This project is open for portfolio/demo use. Add a license file if you want to define formal reuse permissions.
