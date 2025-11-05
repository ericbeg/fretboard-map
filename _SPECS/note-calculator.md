# Note Calculator

## Summary

The Note Calculator provides core music theory utilities for calculating note positions, intervals, and MIDI values. It serves as the mathematical foundation for all musical calculations in the fretboard visualizer, handling note name conversions, interval arithmetic, and MIDI note number calculations.

## Features

- **Note Name Mapping**: Bidirectional conversion between note names (C, C#, D, etc.) and numerical indices
- **Interval Arithmetic**: Calculates note positions based on semitone intervals from a root note
- **MIDI Note Calculation**: Converts string/fret positions to MIDI note numbers for playback
- **Enharmonic Equivalents**: Handles sharp/flat note name variations (C#/Db, D#/Eb, etc.)
- **String Tuning Support**: Configurable for standard guitar tuning (E-A-D-G-B-E)
- **12-Tone Equal Temperament**: All calculations based on standard Western music theory

## Inputs / Outputs

### Inputs
- **Root Note**: Starting note name (string) for interval calculations
- **Interval Array**: Array of semitone intervals from root (e.g., [0, 4, 7] for major triad)
- **String Index**: Guitar string number (0-5, low to high E)
- **Fret Number**: Fret position on the string (0-15)

### Outputs
- **Note Names**: Calculated note names at specific positions
- **MIDI Numbers**: Standard MIDI note numbers (0-127) for audio playback
- **Note Arrays**: Lists of notes for chords, scales, or custom selections

## Implementation Details

**Core Data Structures:**
- `notes[]`: Array of 12 note names in chromatic order
- `noteToIndex{}`: Lookup table for note name to index conversion
- `stringNotes[]`: Current string tunings (configurable)
- `chordIntervals{}`: Predefined chord type intervals
- `scaleIntervals{}`: Predefined scale type intervals

**Key Functions:**
- `getNoteAtFret(stringIndex, fret)`: Returns note name at position
- `getMidiNote(stringIndex, fret)`: Returns MIDI note number
- `getChordNotes(root, quality)`: Returns array of notes in chord
- `getScaleNotes(key, scale)`: Returns array of notes in scale

**Evolution Notes**: Core music theory calculations were part of the initial implementation. The system supports both chord and scale visualization modes added progressively.
