# Triangles - Generated Art

A TRMNL plugin that generates random geometric artwork inspired by traditional Japanese Kumiko patterns. Each refresh creates a unique composition of triangular patterns with varying complexity and density.

## Overview

This plugin creates procedurally generated artwork using triangular geometric patterns. The artwork is generated fresh with each refresh, ensuring your TRMNL display always shows something new and unique. The patterns are inspired by traditional Japanese Kumiko woodworking techniques, featuring intricate geometric designs arranged in a triangular grid.

## Features

- **Procedural Generation**: Each refresh creates a completely unique artwork
- **Customizable Density**: Control the number of columns (4-50)
- **Adjustable Stroke Width**: Fine-tune the line thickness (2-50px)
- **Border Control**: Add or adjust border width (2-50px)
- **Whitespace Control**: Adjust the emptiness/density of patterns (0-10)
- **E-ink Optimized**: Black and white design perfect for e-ink displays
- **Noise-based Distribution**: Uses Perlin-like noise for organic pattern distribution
- **60+ Pattern Variations**: Includes diverse geometric patterns from simple to complex

## Installation

1. Copy all plugin files to your TRMNL plugins directory
2. Configure the plugin settings through the TRMNL interface
3. Add the plugin to your desired layout (supports all sizes)

## Settings

### Columns
- **Range**: 4-50
- **Default**: 8
- **Description**: Controls the number of vertical columns in the artwork. More columns create finer, more detailed patterns.

### Stroke Width
- **Range**: 2-50
- **Default**: 10
- **Description**: Sets the thickness of the lines used to draw the patterns. Thicker strokes create bolder, more visible patterns.

### Border Width
- **Range**: 2-50
- **Default**: 10
- **Description**: Controls the width of the border frame around the artwork.

### Emptyness
- **Range**: 0-10
- **Default**: 5
- **Description**: Adjusts the amount of whitespace in the artwork:
  - **0**: Minimal whitespace, dense patterns
  - **5**: Balanced composition
  - **10**: Maximum whitespace, sparse patterns

## Supported Layouts

This plugin supports all TRMNL layout sizes:
- Full (800x480)
- Half Horizontal
- Half Vertical
- Quadrant

## Technical Details

### Pattern Library

The plugin includes 60+ unique geometric patterns categorized by complexity:
- **Simple patterns**: Basic triangular divisions
- **Medium patterns**: Kumiko-inspired geometric designs
- **Complex patterns**: Intricate multi-layered compositions

### Generation Algorithm

1. **Noise Map Creation**: Uses a seeded Perlin-like noise function for consistent randomness
2. **Darkness Mapping**: Converts noise values to pattern complexity
3. **Pattern Selection**: Chooses patterns based on darkness values
4. **Grid Layout**: Arranges patterns in a triangular tessellation
5. **SVG Rendering**: Generates optimized SVG output

### Performance

- Lightweight SVG-based rendering
- No external dependencies
- Optimized for e-ink refresh rates
- Static strategy (no polling required)

## Customization Tips

### For Dense, Bold Artwork
- Columns: 6-10
- Stroke Width: 15-25
- Emptyness: 0-3

### For Delicate, Detailed Artwork
- Columns: 20-40
- Stroke Width: 2-5
- Emptyness: 5-8

### For Minimalist Compositions
- Columns: 4-8
- Stroke Width: 8-12
- Emptyness: 7-10

## File Structure

```
triangles/
├── settings.yml           # Plugin configuration and metadata
├── shared.liquid          # Core generation logic and pattern library
├── full.liquid           # Full-size layout
├── half_horizontal.liquid # Half horizontal layout
├── half_vertical.liquid   # Half vertical layout
└── quadrant.liquid       # Quadrant layout
```

## Credits

- **Author**: trmnl@achtnegen.nl
- **Inspiration**: Traditional Japanese Kumiko woodworking patterns
- **Category**: Art

## License

This plugin is provided as-is for use with TRMNL devices.

## Support

For issues, questions, or suggestions, please contact: trmnl@achtnegen.nl

---

*Refresh your TRMNL to see a new unique artwork every time!*
