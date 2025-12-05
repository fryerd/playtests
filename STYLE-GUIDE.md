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

### Urban Rooftop (Complete)
- NYC/Chicago inspired skyline with iconic building shapes
- Art deco spires, setbacks, distinctive silhouettes
- Water tower, antenna with blinking light, AC units, pipes, vents
- Traffic lights, taxis (yellow), cars
- Sun with rays, comic-style clouds, airplane

### Aztec Temple/Jungle (Next)
- Stone temple pyramid structure
- Dense jungle vegetation layers
- Tropical birds or insects
- Ancient stone carvings/statues
- Vines, ferns, exotic plants
- Warm humid color palette

### Egyptian Pyramids/Desert
- Pyramid silhouettes
- Desert sand dunes
- Pharaoh statues/sphinx elements
- Palm trees, oasis hints
- Hot golden/orange palette
- Maybe a camel or desert bird

### Pirate Caribbean Island
- Tropical island with palm trees
- Pirate ship or dock elements
- Beach/ocean waves
- Treasure chest, barrels, ropes
- Seagulls or parrots
- Teal/turquoise water colors

### Neon City Street (Japanese/Chinese)
- Dense urban buildings
- Neon signs (stylized characters)
- Lanterns, paper decorations
- Street food stalls, vending machines
- Cherry blossoms or rain
- Pink/purple/cyan neon palette

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
- `pirate-caribbean-island.html`
- `neon-city-street.html`
