# Product Requirements Document

Use this PRD to build a similar color palette generator with Claude Code CLI.

## Overview

Build a real-time color palette generator that extracts colors from images and displays them applied to live UI components.

## Core Features

### 1. Image Loading
- **Upload**: Drag-and-drop or click to upload images
- **Random Photos**: Button to load random photos from a free API (Picsum Photos)
- **Thumbnail Gallery**: Display all loaded images as clickable thumbnails below the main viewer
- **Image Switching**: Click any thumbnail to make it the active selection surface

### 2. Color Picking Interface
- **Hover Preview**: As user hovers over the image, display the current pixel color in real-time
- **Click to Generate**: Clicking on the image generates a complete color palette (not just a single color)
- **Color Info Tooltip**: Show HSL values that follow the cursor while hovering

### 3. Color Harmony Modes
Generate palettes using three harmony algorithms:
- **Analogous**: Colors adjacent on the color wheel (±30°, ±60°)
- **Complementary**: Base color + opposite color + light/dark variations
- **Triadic**: Three evenly spaced colors (120° apart) + muted variations

**Behavior**: Switching harmony modes regenerates the palette from the last selected color and saves it to history.

### 4. Three-Panel Layout

**Left Panel: Palette History**
- Display previously generated palettes as thumbnail strips
- Show harmony mode label for each palette
- Click any palette to reapply it
- Store up to 20 palettes

**Center Panel: Image Selection Surface**
- Main image viewer with crosshair cursor
- Current color display with HSL values
- Generated palette display (5 colors with hue values)
- Thumbnail gallery below

**Right Panel: Live Component Preview**
- Display shadcn/ui components that update in real-time:
  - Primary, Secondary, Accent buttons
  - Card component
  - Input field
  - Badges
  - CSS variable values

### 5. Toolbar Controls
- **Harmony Mode Buttons**: Analogous, Complementary, Triadic
- **Random Photo**: Load new random image
- **Upload Image**: Add more images
- **Reset**: Clear history and reset to default theme

## Design Requirements

### Visual Style
- Inspired by paper.design aesthetic
- Cream/off-white background (#edebe1)
- Minimal, clean layout
- Subtle borders and shadows
- System font stack

### Component Library
- Use shadcn/ui design system principles
- CSS custom properties for theming
- Tailwind CSS for utility styling

### Responsive Behavior
- Three-column layout on desktop (lg breakpoint)
- Stack vertically on mobile
- All controls accessible on small screens

## Technical Requirements

### Implementation
- Single HTML file with embedded CSS and JavaScript
- No build process required
- Tailwind CSS via CDN
- Canvas API for pixel color extraction
- CORS-enabled image loading

### Color Processing
- RGB to HSL conversion
- Dynamic palette generation based on harmony rules
- Real-time CSS custom property updates
- Proper foreground color calculation (light/dark contrast)

### Image Handling
- Support drag-and-drop upload
- Load external images with CORS support
- Canvas-based pixel sampling
- Thumbnail generation and gallery management

## User Flow

1. **Initial State**: Upload zone with "load random photo" option
2. **Image Loaded**: Main interface appears with three panels
3. **Color Exploration**: Hover over image to preview colors
4. **Palette Generation**: Click to generate and save palette
5. **Mode Switching**: Change harmony modes to see variations
6. **History Management**: View and reapply saved palettes
7. **Multi-Image**: Load more images via random or upload buttons

## Footer

- Credit shadcn/ui with link to https://ui.shadcn.com
- Minimal styling to match overall aesthetic

## API Integration

Use **Picsum Photos** (https://picsum.photos):
- Free, no API key required
- Random high-quality images
- Reliable CORS support
- URL format: `https://picsum.photos/id/{random}/1200/800`

---

## How to Use This PRD

Copy this entire document and paste it into Claude Code CLI with:

```
Build this application following the PRD in a single HTML file.
```

Then iterate on specific features or styling as needed.
