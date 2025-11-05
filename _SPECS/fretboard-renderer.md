# Fretboard Renderer

## Summary

The Fretboard Renderer is responsible for creating and maintaining the visual SVG representation of a guitar fretboard. It handles the drawing of strings, frets, fret markers, and note positions, providing the canvas upon which chord, scale, and free mode visualizations are overlaid.

## Features

- **Responsive SVG Rendering**: Creates a scalable vector graphics fretboard that adapts to different screen sizes
- **Standard Guitar Layout**: Renders 6 strings (E-A-D-G-B-E) with 15 frets
- **Fret Markers**: Displays traditional fretboard markers at frets 3, 5, 7, 9, 12, and 15 (double dots at 12)
- **Visual Styling**: Applies dark theme with gradient background and proper contrast
- **Interactive Elements**: Provides clickable note positions for MIDI playback
- **Performance Optimized**: Efficient SVG creation with minimal DOM manipulation

## Inputs / Outputs

### Inputs
- **Container Element**: DOM element where the SVG fretboard will be rendered
- **Display Mode**: Current visualization mode (chords, scales, free) affecting what notes are highlighted
- **Note Data**: Array of notes to highlight with their positions and styling information

### Outputs
- **SVG Element**: Complete fretboard visualization with strings, frets, and markers
- **Interactive Circles**: Clickable note positions that trigger MIDI playback
- **Visual Feedback**: Color-coded note highlighting based on musical function

## Implementation Details

The renderer uses a coordinate system based on:
- **String Spacing**: Calculated dynamically based on fretboard height
- **Fret Width**: Fixed width per fret with margin for proper positioning
- **Note Positioning**: Mathematical calculation of note positions on each string

**Evolution Notes**: Initial implementation included basic fretboard drawing. Fret 15 marker was added in July 2025 to extend playable range.
