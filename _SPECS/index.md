# Fretboard Map Specifications Index

This index provides an overview of all specification files for the Fretboard Map project, an interactive guitar fretboard visualizer web application.

## Project Overview

Fretboard Map is a browser-based application that helps musicians visualize guitar chords, scales, and notes on a fretboard. Built with vanilla HTML, CSS, and JavaScript, it provides real-time visualization with optional MIDI output support.

**Evolution Timeline (from git history):**
- July 2025: Initial fretboard implementation with basic chord/scale visualization
- July 2025: Added README documentation and UI refinements
- September 2025: Added free mode for manual note selection

## Specification Files

### Core Components

- **[fretboard-renderer.md](fretboard-renderer.md)** - SVG-based fretboard drawing and visual rendering system
- **[note-calculator.md](note-calculator.md)** - Music theory utilities for note calculations, intervals, and MIDI conversions
- **[ui-controller.md](ui-controller.md)** - User interface management and event handling for mode switching

### Visualization Modes

- **[chord-parser.md](chord-parser.md)** - Chord input parsing and chord note visualization
- **[scale-visualizer.md](scale-visualizer.md)** - Scale selection and scale note highlighting
- **[free-mode.md](free-mode.md)** - Manual note selection and free-form playing mode

### External Integration

- **[midi-controller.md](midi-controller.md)** - Web MIDI API integration for audio output

## Architecture Notes

The application follows a modular design with clear separation of concerns:
- **Rendering**: Pure SVG-based visualization with responsive design
- **Logic**: Music theory calculations and mode-specific functionality
- **Interaction**: Event-driven UI with optional MIDI integration
- **Data**: Static music theory data (intervals, note mappings) with dynamic state management

All specifications reflect the current implementation state and incorporate evolutionary changes from the project's git history.
