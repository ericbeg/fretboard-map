# Chord Parser

## Summary

The Chord Parser handles user input for chord names and converts them into visualizable note data. It parses chord symbols (like "C", "Am", "G7sus4") and determines the appropriate notes to highlight on the fretboard based on music theory rules.

## Features

- **Chord Symbol Parsing**: Recognizes root notes and chord qualities from text input
- **Quality Detection**: Supports major, minor, 7th, suspended, diminished, and augmented chords
- **Real-time Input**: Updates visualization as user types chord names
- **Error Handling**: Gracefully handles invalid or unrecognized chord inputs
- **Color Coding**: Assigns specific colors to chord tones (root, third, fifth, seventh)
- **Comprehensive Coverage**: Supports common chord types used in guitar playing

## Inputs / Outputs

### Inputs
- **Chord String**: User-entered chord name (e.g., "Cmaj7", "Bbmin", "F#sus2")
- **Parse Request**: Trigger to analyze the current input string

### Outputs
- **Parsed Chord Data**: Object containing root note and chord quality
- **Note Array**: List of notes in the chord with their musical functions
- **Visualization Data**: Color-coded note positions for fretboard rendering
- **Validation Status**: Boolean indicating if the chord was successfully parsed

## Implementation Details

**Parsing Logic:**
1. Extract root note using regex pattern `/^[A-G][b#]?/`
2. Remove root from string to isolate quality modifiers
3. Match remaining text against known chord quality patterns
4. Default to "major" if no quality specified

**Supported Chord Types:**
- Major: C, Cmaj, Cmajor
- Minor: Cm, Cmin, Cminor
- Dominant 7th: C7
- Major 7th: Cmaj7, CΔ7
- Minor 7th: Cm7, C-7
- Diminished: Cdim, C°
- Augmented: Caug, C+
- Suspended: Csus2, Csus4
- Add9: Cadd9

**Color Scheme:**
- Root notes: Red (#e74c3c)
- Thirds: Blue (#3498db)
- Fifths: Green (#2ecc71)
- Other extensions: Default colors

**Evolution Notes**: Chord parsing was part of the initial July 2025 implementation, supporting basic chord visualization that evolved alongside the fretboard renderer.
