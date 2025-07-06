# Interactive Fretboard

This is a web-based, interactive guitar fretboard visualizer. It helps musicians see the positions of notes for various chords and scales directly on the fretboard. The application is built with plain HTML, CSS, and JavaScript, and requires no server to run.

## Features

*   **Chord Visualization:** Enter a chord name (e.g., `C`, `Am`, `G7sus4`) to see all corresponding notes highlighted on the fretboard.
    *   Notes are color-coded by their function in the chord (root, third, fifth).
*   **Scale Visualization:** Select a root note and a scale type (e.g., Major, Minor Pentatonic, Dorian) to display all the notes of that scale.
    *   Notes are color-coded for easy identification.
*   **MIDI Output:** If your browser supports the Web MIDI API and you have a MIDI device connected, you can click on any displayed note to play it.
*   **Responsive Design:** The fretboard and controls adapt to different screen sizes.
*   **No Dependencies:** Runs entirely in the browser without needing any external libraries or build steps.

## How to Use

1.  **Open the file:** Simply open the `index.html` file in a modern web browser (like Chrome, Firefox, or Edge) that supports the Web MIDI API.
2.  **Select a Mode:**
    *   **Chords:** Choose the "Chords" radio button and type a chord name into the input field. The fretboard will update automatically as you type.
    *   **Scales:** Choose the "Scales" radio button. Select a root key from the first dropdown and a scale type from the second dropdown.
3.  **Play Notes (Optional):**
    *   If a MIDI output device is detected, a "MIDI Output" dropdown will appear.
    *   Select your desired MIDI device.
    *   Click on any of the highlighted notes on the fretboard to send a MIDI signal and hear the note.

## Technologies Used

*   **HTML5**
*   **CSS3**
*   **Vanilla JavaScript**
*   **Web MIDI API** for audio output.
