# UI Controller

## Summary

The UI Controller manages all user interface interactions, mode switching, and event handling for the fretboard application. It coordinates between user inputs and the various visualization and audio components, providing a seamless interactive experience.

## Features

- **Mode Switching**: Radio button controls for Chords, Scales, and Free modes
- **Dynamic UI Updates**: Shows/hides relevant controls based on selected mode
- **Real-time Input Handling**: Instant response to chord typing and dropdown selections
- **Event Coordination**: Routes user interactions to appropriate processing functions
- **Responsive Layout**: Adapts control layout for different screen sizes
- **State Management**: Maintains UI state consistency across mode changes

## Inputs / Outputs

### Inputs
- **Mode Selection**: Radio button changes (chords/scales/free)
- **Chord Input**: Text input for chord names with real-time updates
- **Scale Selection**: Dropdown changes for key and scale type
- **Free Mode Controls**: Checkbox and button interactions
- **MIDI Device Selection**: Dropdown changes for audio output

### Outputs
- **UI State Changes**: Visibility toggles for control groups
- **Display Updates**: Triggers for fretboard re-rendering
- **Event Bindings**: Dynamic attachment of event listeners
- **Form Population**: Dynamic creation of dropdown options

## Implementation Details

**Control Groups:**
- **Mode Radios**: Three radio buttons controlling primary application mode
- **Chord Controls**: Text input for chord names (chords mode only)
- **Scale Controls**: Key and scale type dropdowns (scales mode only)
- **Free Controls**: Show all notes checkbox and clear button (free mode only)
- **MIDI Controls**: Output device selection (when devices available)

**Event Handling:**
- `DOMContentLoaded`: Initializes UI and binds all event listeners
- `input` events: Real-time chord parsing and display updates
- `change` events: Dropdown selections and mode switches
- `click` events: Button interactions and fretboard note clicks

**Mode Logic:**
```javascript
if (mode === 'chords') {
    show chord input, hide scale/free controls
} else if (mode === 'scales') {
    show scale dropdowns, hide chord/free controls
} else if (mode === 'free') {
    show free controls, hide chord/scale controls
}
```

**Initialization Sequence:**
1. Populate scale and key dropdowns from data structures
2. Set up mode radio button event listeners
3. Bind input/change events for real-time updates
4. Initialize fretboard display
5. Attempt MIDI device detection

**Evolution Notes**: UI controller evolved from basic mode switching in July 2025 to include free mode controls added in September 2025. The responsive design and real-time input handling were part of the initial implementation.
