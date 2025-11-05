# Free Mode

## Summary

Free Mode provides users with complete creative freedom to manually select and highlight individual notes on the fretboard. Unlike chord and scale modes which follow music theory rules, free mode allows arbitrary note combinations for experimentation, composition, or custom pattern exploration.

## Features

- **Manual Note Selection**: Click any note position to toggle it on/off
- **Visual Feedback**: Selected notes highlighted with boomwhacker colors
- **MIDI Playback**: Click selected notes to hear them through MIDI output
- **Clear Function**: Reset all selections with a single button
- **Show All Notes Toggle**: Option to display all note names or only selected ones
- **State Persistence**: Maintains selection state during mode switches
- **Real-time Updates**: Instant visual response to user interactions

## Inputs / Outputs

### Inputs
- **Click Events**: User clicks on fretboard note positions
- **Clear Command**: Button press to reset all selections
- **Show All Toggle**: Checkbox to control note name visibility
- **Mode Switch**: Transition to/from free mode

### Outputs
- **Selection State**: Array of currently selected note positions
- **Visual Updates**: Fretboard rendering with selected notes highlighted
- **MIDI Triggers**: Audio playback when notes are clicked
- **UI State**: Updated button and checkbox states

## Implementation Details

**State Management:**
- `selectedNotes[]`: Array storing {stringIndex, fret, note} objects
- `isNoteSelected()`: Checks if a position is currently selected
- `toggleNoteSelection()`: Adds/removes notes from selection
- `clearAllNotes()`: Resets selection to empty state

**Interaction Flow:**
1. User clicks note position
2. Check if note is already selected
3. Toggle selection state (add/remove from array)
4. Update visual display immediately
5. Play MIDI note if selection was added

**Visual States:**
- **Selected Notes**: Highlighted with boomwhacker colors, always visible
- **Unselected Notes**: Gray (#444) when "show all" is enabled, transparent when disabled
- **Clickable Areas**: All positions respond to clicks regardless of visibility

**MIDI Integration:**
- Plays note on selection (not deselection)
- Uses `getMidiNote()` for accurate pitch calculation
- 500ms duration with velocity 127

**Evolution Notes**: Free mode was added in September 2025 as the latest feature, expanding the application from structured music theory visualization to creative exploration tools.
