# Game Background Style Guide

## Visual Style: Graphic Novel

Inspired by late 90s/early 2000s Mortal Kombat/Tekken fighting game backgrounds, executed in a bold comic book aesthetic.

---

## Technical Requirements

- **Pure HTML + CSS** (minimal JS only for quiz interaction)
- **Performance priority** - fast loading on slow school networks
- **No external images** - all CSS shapes and gradients
- **Responsive** - works on desktop and mobile
- **Hardware-accelerated animations** only (transform, opacity)

## Core Design Principles

### 1. Bold Outlines
- All elements have **4-5px solid black borders**
- Creates that hand-drawn comic book feel
- No soft edges or gradients on shapes

### 2. Color Palette
```css
--ink-black: #0a0a0a;        /* Outlines, silhouettes */
--shadow-dark: #1a1a2e;      /* Dark building fills */
--shadow-mid: #2d2d44;       /* Mid-tone fills */
--highlight: #fff1c1;        /* Cream/beige highlights, clouds */
--accent-red: #c0392b;       /* Action accents */
--accent-yellow: #f1c40f;    /* Highlights, windows, taxis */
```
*Colors will vary per environment but maintain similar contrast ratios*

### 3. Halftone Overlay
- Subtle dot pattern over entire background
- 4px spacing, ~8% opacity
- Adds print/comic texture

### 4. Layered Depth
- **Far silhouettes**: Pure black, simple shapes
- **Mid-ground**: Dark fills with black outlines, window patterns
- **Foreground**: More detail, interactive elements

---

## Animation Guidelines

### Speed
- **Slow and subtle** - not distracting from gameplay
- Clouds: ~50 second loop
- Flying elements (planes, birds): ~60 second loop
- Different speeds create parallax effect

### Direction
- Movement goes **left to right**
- Elements start visible on screen

### Types of Animation
- Drifting clouds
- Flying objects (planes, birds - environment appropriate)
- Blinking lights (antenna, signals)
- No sudden or jarring movements

---

## Environment-Specific Elements

### Urban Rooftop Sunset (Complete)
- NYC/Chicago inspired skyline with iconic building shapes
- Art deco spires, setbacks, distinctive silhouettes
- Water tower, antenna with blinking light, AC units, pipes, vents
- Traffic lights, taxis (yellow), cars
- Sun with rays, comic-style clouds, airplane
- Warm sunset orange/purple palette

### Aztec Temple Jungle (Complete)
- Stone temple pyramid structure with stepped layers
- Dense jungle vegetation in foreground and background
- Tropical birds flying across (animation)
- Ancient stone carvings and idol statues
- Torches with flickering flame animation
- Layered palm trees (larger at edges, smaller in middle)
- Warm humid green/gold palette

### Egyptian Pyramids Desert (Complete)
- Three pyramids with CSS triangle technique
- Gold capstones (pyramidions) on pyramid tops
- Shadows on correct side (left, with sun on right)
- Pyramids sitting on horizon line
- Small scattered cacti
- Hot golden/orange sunset palette
- Minimal, clean composition

### Underwater Atlantis (Complete)
- Submarine moving across top (60s animation)
- 7 colorful fish with forked tails swimming at varying speeds (45-62s)
- Atlantis ruins: temple with columns, broken arch, fallen pillar
- Swaying seaweed animation
- Coral in pink and orange
- Rising bubble animations
- Ocean floor with shells
- Vivid blue/teal/cyan underwater palette
- Light rays from surface

### Outer Space Cosmos (Complete)
- Space station with solar panels moving across top (70s animation)
- Two comets with detailed tails:
  - Multi-layer tail (core, glow, wisp)
  - Dust particle effects
  - Blue ion tail accent
- 25 scattered stars (white, yellow, blue) with twinkle animation
- Large orange planet with rings
- Small teal moon and distant red planet
- Nebula clouds (pink, purple, blue glow)
- Asteroid belt
- Small rocket with flickering flame
- Distant spiral galaxy
- Deep space purple/blue palette

---

## Quiz Modal Design

### Container
- Background: `var(--highlight)` (cream/beige)
- Border: 5px solid black
- Box shadow: 10px 10px 0 black (comic offset shadow)
- Slight rotation: -0.5deg
- Red inner border accent (3px)

### Typography
- **Question**: Nunito, 800 weight, 1.3rem, centered
- **Options**: Nunito, 700 weight, 1rem, centered
- High legibility is priority

### Option Buttons
- White background, 4px black border
- Comic box shadow (4px 4px 0 black)
- **Hover**: Yellow background, slight lift (-2px, -2px), anticipation pulse animation
- **Correct**: Green (#27ae60), pop animation, other options disabled (grey/translucent)
- **Incorrect**: Red, shake animation, "INCORRECT!" text, resets after 1 second

### Action Text
- Font: Bangers (comic style)
- Large, rotated, with heavy text-shadow
- Shows "CORRECT!" (yellow) or "INCORRECT!" (red)
- Hidden by default, appears on interaction

---

## File Naming
- `urban-rooftop-sunset.html`
- `aztec-temple-jungle.html`
- `egyptian-pyramids-desert.html`
- `underwater-atlantis.html`
- `outer-space-cosmos.html`

---

## Live Demos
All backgrounds are hosted on GitHub Pages:
- https://fryerd.github.io/playtests/urban-rooftop-sunset.html
- https://fryerd.github.io/playtests/aztec-temple-jungle.html
- https://fryerd.github.io/playtests/egyptian-pyramids-desert.html
- https://fryerd.github.io/playtests/underwater-atlantis.html
- https://fryerd.github.io/playtests/outer-space-cosmos.html
