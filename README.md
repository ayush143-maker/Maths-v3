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

## Asset and loading review checklist

This is a checklist of actions to perform, not a record of verified results.

- Inspect `index.html` for local image, audio, and other media references. If it references `music.mp3`, confirm the root file exists at that path and check how it is used; do not assume the file is loaded or played just because it is present.
- Remove media only after confirming it is not referenced. For used media, prefer files sized for their role and avoid keeping unnecessarily large originals or unused variants.
- Review the Google Fonts links in `index.html`. Keep external font requests only if the page intentionally uses them, and check typography when those requests are unavailable.
- Check any other external font or script references in the HTML and confirm each is intentional. After renaming or moving local files, verify their relative paths.

## Manual review checklist

This is a checklist of actions to perform, not a record of verified results.

- Open the root `index.html` in a browser, or use the local preview steps above. Review the animation and the displayed x and y values.
- Try the on-screen controls defined in `index.html`; observe how they affect the visualisation and displayed values.
- Inspect the page at a narrow mobile-sized viewport and a wide desktop-sized viewport. Check that the visualisation, values, and controls remain visible and usable.
- After changing the animation or interaction, compare the displayed values with the plotted curve. If you change the Google Fonts links, review the typography too.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check whether every on-screen control defined in `index.html` can be reached and operated without a pointer. Check that focus order is sensible and that no action depends only on pointer input.
- Check that keyboard focus is clearly visible on each focused control and is not lost against the visualization.
- Review the controls for meaningful accessible names. Check that the changing x and y values are available as text and whether the curve has a suitable text explanation for information conveyed by its plotted appearance.
- Check text and control-label contrast against their backgrounds, including around the visualization, and review legibility with the linked fonts unavailable.
- Because the experiment is animated, check its behavior with the operating system's reduced-motion preference enabled. Review whether the visualization and controls remain usable when motion is reduced.