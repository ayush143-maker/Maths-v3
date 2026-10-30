# Maths-v3

Maths-v3 is a timed mathematical-art experience centered on the curve **y = -1/x**. The root `index.html` draws a full-screen animated canvas with axes, a starfield, a moving particle, and its trail. It also displays the particle’s changing x and y values and timed Hindi lyrics.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>. The local audio file is `music.mp3`. Dancing Script and Inter are loaded from Google Fonts, so those fonts depend on network access.

## Start and watch

Click or touch the opening screen to begin; Space and Enter also start the experience. An equation title screen runs for five seconds, then the particle animation and `music.mp3` start. The particle follows a programmed x(t) path toward zero, with the corresponding y value shown on screen. Its final rapid descent is scheduled for the last two seconds of the 56-second sequence. A closing message appears when the sequence ends.

When audio plays, animation timing follows the audio element’s playback time. If audio playback does not begin, the animation uses a performance-clock fallback. Browser audio policies may require a user gesture, and the page does not provide pause, seek, or restart controls; reload the page to run it again.

## Editing and rendering notes

The visualization, displayed values, lyrics, timing, and controls are in `index.html`. Keep the displayed values and curve logic consistent if changing the particle path. Keep `music.mp3` at the repository root unless you update its reference in the page. The canvas resizes with the browser window and caps its rendering device-pixel ratio at 2.

The experience is self-contained apart from the external Google Fonts requests: its source makes no external API calls and does not use local storage. No build scripts or deployment configuration are documented. Check the animation and audio together in a browser after changing timing or media; the page has no in-experience controls for recovering from a missed or interrupted sequence.