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

## Manual review checklist

This is a checklist of actions to perform, not a record of verified results.

- Open the root `index.html` in a browser, or use the local preview steps above. Review the animation and the displayed x and y values.
- Try the on-screen controls defined in `index.html`; observe how they affect the visualisation and displayed values.
- Check whether `index.html` references `music.mp3` and, if so, confirm the file is available at that relative path.
- Inspect the page at a narrow mobile-sized viewport and a wide desktop-sized viewport. Check that the visualisation, values, and controls remain visible and usable.
- After changing the animation or interaction, compare the displayed values with the plotted curve. If you change the Google Fonts links, review the typography too.