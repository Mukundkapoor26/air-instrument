# air/instrument

A string that hangs in the air in front of your webcam. Swipe a fingertip through it to play, and pinch an end to stretch it and change the note. It runs entirely in the browser: nothing to install, and no video leaves your device.

**Try it:** https://mukundkapoor26.github.io/air-instrument/

## What it does

- One string fixed in the air, so you don't have to hold it
- Swipe an index fingertip through it to pluck. Where you pluck changes the tone, and how fast you pluck changes the volume
- Pinch near an end and stretch it to tune it, then let go to leave it there. Moving it while a note rings bends the pitch
- **Tension mode (default):** stretching tightens the string like a tuning peg, so longer = higher. Turn it off for **length mode**, where shorter = higher, like fretting a guitar
- Pinch empty air with both hands and pull them apart to draw a brand new string between them (up to 6), each tuned by its own length
- Every string keeps its own sound: pick a sound and it applies to new strings and the one you last played, so clean and rock strings can ring side by side
- Pinch the middle of a string to move the whole thing
- High notes throw glitter, and the higher the note, the more stars
- 1, 3 or 6 strings, tuned as a chord and spaced so you can pick one out
- Snap to scale (major or minor pentatonic) so it always sounds musical
- 7 sounds, physically modelled in a Web Audio worklet, each with its own visual:

| Sound | Visual |
| --- | --- |
| clean | silk threads |
| rock (power chords) | retro spectrum bars driven by the real audio |
| bass | silk flame |
| sitar | mandala |
| harp | iridescent filaments |
| glass | prism interference |
| synth | pastel smear |

- Metal strings with chromatic edges, and plucks that ripple through the visuals
- Works with the mouse or touch too, so no camera is needed

## Controls

| Input | Action |
| --- | --- |
| Swipe through the string | Play |
| Pinch an end / drag an end | Stretch it, which changes the note |
| Both hands pinch empty air and pull apart / shift-drag | Draw a new string |
| T | Tension vs length mode |
| C | Clear back to one string |
| ← → | Change sound |
| 1, 3, 6 | Number of strings |
| Space | Strum |
| H | Hide the UI |

## Run it locally

```bash
python3 -m http.server 5179
```

Then open http://localhost:5179. The camera needs `localhost` or HTTPS.

## Built with

- [MediaPipe Tasks Vision](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) for hand tracking
- A Karplus-Strong string model in an AudioWorklet
- WebGL fragment shaders for the visuals

Made by [Mukund Kapoor](https://mukundkapoor.com) with AI. MIT licensed.
