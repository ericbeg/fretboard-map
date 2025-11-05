# MIDI Controller

## Summary

The MIDI Controller manages Web MIDI API integration, enabling audio playback of notes through connected MIDI devices. It provides optional sound output functionality that enhances the visual fretboard experience with audible feedback.

## Features

- **Web MIDI API Integration**: Detects and connects to MIDI output devices
- **Device Selection**: Dropdown menu for choosing from available MIDI outputs
- **Note Playback**: Converts fretboard positions to MIDI note numbers and sends playback commands
- **Graceful Degradation**: Functions normally without MIDI devices (visual-only mode)
- **Error Handling**: Manages MIDI access permissions and device connection issues
- **Performance Timing**: Proper note on/off timing with configurable duration

## Inputs / Outputs

### Inputs
- **MIDI Access Request**: Browser permission request for MIDI device access
- **Device Selection**: User choice of MIDI output device from dropdown
- **Note Trigger**: Fretboard click events requesting audio playback
- **Note Parameters**: MIDI note number, velocity, and duration

### Outputs
- **MIDI Messages**: Note on/off commands sent to selected output device
- **Device List**: Available MIDI outputs populated in UI dropdown
- **Connection Status**: Visual indication of MIDI device availability
- **Error Messages**: Console logging for troubleshooting

## Implementation Details

**MIDI Setup Process:**
1. Check for `navigator.requestMIDIAccess` support
2. Request user permission for MIDI access
3. Enumerate available output devices
4. Populate dropdown with device names
5. Store selected device reference for playback

**Playback Mechanics:**
- **Note Numbers**: Calculated using `getMidiNote(stringIndex, fret)`
- **Velocity**: Fixed at 127 (maximum volume)
- **Duration**: 500ms with automatic note-off scheduling
- **Channel**: Default MIDI channel 1

**Device Management:**
- `midiAccess`: Global Web MIDI API access object
- `midiOutput`: Currently selected output device
- `onMIDISuccess()`: Handles successful MIDI access
- `onMIDIFailure()`: Handles access denial or API unavailability

**Error Scenarios:**
- Browser doesn't support Web MIDI API
- User denies MIDI access permission
- No MIDI output devices connected
- Device becomes unavailable during use

**Evolution Notes**: MIDI integration was part of the initial July 2025 implementation, providing audio feedback that enhances the visual learning experience. The feature gracefully degrades when MIDI devices are unavailable.
