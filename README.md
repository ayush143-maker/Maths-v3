# Maths-v3

An animated mathematical-art experiment built around the curve **y = -1/x**. The root `index.html` displays changing x and y values alongside the visualisation and defines the on-screen controls. The project also includes `music.mp3` in the root folder.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Explore and customize

The page, visualisation, displayed values, and controls are defined in `index.html`. When changing the animation or interaction, keep the displayed values aligned with the plotted curve. The page links to Google Fonts; changing or removing those links may affect typography.

Preserve the relative path to `music.mp3` if replacing the audio file. If you rename or move it, update its reference in `index.html`; keep the file in the project folder when hosting the static page.