# Color Palette Generator

A real-time color palette generator that lets you extract colors from images and see them applied instantly to shadcn/ui components.

## Features

- **Interactive Color Picker** - Hover over any image to preview colors in real-time
- **Click to Generate Palettes** - Generate complete color palettes with a single click
- **3 Color Harmony Modes**:
  - Analogous - Colors adjacent on the color wheel
  - Complementary - Opposite colors for high contrast
  - Triadic - Three evenly spaced colors
- **Live Component Preview** - See shadcn/ui components (buttons, cards, inputs, badges) update instantly
- **Palette History** - Save and reapply your favorite palettes
- **Image Gallery** - Load multiple images and switch between them
- **Random Photos** - Instantly load random high-quality photos to explore

## How to Use

1. **Load an Image**:
   - Upload your own image, or
   - Click "or load random photo" to fetch a random photo

2. **Pick Colors**:
   - Hover over the image to preview colors
   - Click anywhere to generate a complete palette

3. **Switch Harmony Modes**:
   - Try Analogous, Complementary, or Triadic modes
   - Each generates a new palette variation

4. **Build Your Collection**:
   - Generated palettes are saved to history
   - Click any palette to reapply it
   - Use "Random Photo" to load more images

## Tech Stack

- Pure HTML/CSS/JavaScript
- [Tailwind CSS](https://tailwindcss.com) for styling
- [shadcn/ui](https://ui.shadcn.com) design system
- [Picsum Photos](https://picsum.photos) for random images
- Canvas API for pixel color extraction

## License

MIT
