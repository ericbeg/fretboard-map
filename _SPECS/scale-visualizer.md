# Scale Visualizer

## Summary

The Scale Visualizer enables users to explore musical scales by selecting a root key and scale type, then displaying all notes of that scale highlighted on the fretboard. It provides an educational tool for understanding scale patterns and positions on the guitar.

## Features

- **Scale Type Selection**: Dropdown menu with comprehensive scale library
- **Root Key Selection**: Choose from all 12 chromatic notes as scale root
- **Visual Highlighting**: Displays all scale notes with boomwhacker color coding
- **Pattern Recognition**: Helps users see scale shapes and positions across strings
- **Educational Value**: Supports music theory learning and fretboard navigation
- **Real-time Updates**: Instant visualization when selections change

## Inputs / Outputs

### Inputs
- **Root Key**: Selected starting note for the scale (C, C#, D, etc.)
- **Scale Type**: Chosen scale pattern (major, minor pentatonic, dorian, etc.)
- **Visualization Trigger**: Request to update the fretboard display

### Outputs
- **Scale Notes Array**: List of all notes contained in the selected scale
- **Position Data**: String/fret coordinates for each scale note
- **Color Mapping**: Boomwhacker colors assigned to each note
- **Fretboard Overlay**: Visual representation of scale notes on the fretboard

## Implementation Details

**Supported Scale Types:**
- **Diatonic Scales**: Major, Natural Minor, Harmonic Minor, Melodic Minor
- **Pentatonic Scales**: Major Pentatonic, Minor Pentatonic, Blues
- **Modal Scales**: Dorian, Phrygian, Lydian, Mixolydian, Locrian
- **Synthetic Scales**: Whole Tone, Diminished (whole/half), Diminished (half/whole), Altered, Chromatic

**Color Coding:**
Uses the boomwhacker color system for note recognition:
- C: Red, C#: Orange, D: Yellow, D#: Yellow-Orange
- E: Green, F: Green-Blue, F#: Blue, G: Blue-Purple
- G#: Purple, A: Purple-Red, A#: Red-Purple, B: Red

**Key Functions:**
- `getScaleNotes(key, scale)`: Calculates all notes in the selected scale
- `updateDisplay()`: Refreshes fretboard with scale visualization
- Dynamic dropdown population from `scaleIntervals` object

**Evolution Notes**: Scale visualization was implemented alongside chord visualization in the initial July 2025 release, providing complementary functionality for music theory exploration.
