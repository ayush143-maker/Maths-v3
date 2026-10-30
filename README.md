# Maths-v3

Maths-v3 is an animated mathematical-art experiment built around the curve **y = -1/x**. The root `index.html` contains the visualization, changing x and y values, and on-screen controls. The project also includes `music.mp3` in the root folder.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Explore and customize

The visualization, displayed values, and controls are defined in `index.html`. When changing the animation or interaction, keep the displayed x and y values aligned with the plotted curve. Review the controls and rendered result in a browser after making changes.

The project includes `music.mp3`; inspect `index.html` to determine whether and where the page references it before moving or replacing the file. If it is used, keep its location aligned with the page reference or update that reference. Check filename capitalization when investigating a missing local resource.

The page also requests Google Fonts from `fonts.googleapis.com` and `fonts.gstatic.com`, so typography depends on network access to those external resources. No build scripts or deployment configuration are documented.

## Project files

- `index.html` — page entry point, visualization, displayed values, and controls.
- `music.mp3` — local audio file included in the project.