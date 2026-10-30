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

## Configuration and data handling

The listed root files contain no `.env.example` or separate configuration file. This static page has no server-side environment in which to keep secrets: anything placed in its HTML or delivered browser files can be viewed by visitors. Do not put passwords, tokens, or other secrets in the page or tracked files.

Review the page and `music.mp3` before publishing. Avoid including private information in page content, and distribute audio only if you have permission to do so.

## Browser and platform reliability review checklist

This is a checklist for a future review, not a record of completed testing or verified results.

- Review the animated page in current desktop browsers relevant to your audience and on mobile browsers such as Safari on iOS and Chrome on Android where applicable. Identify target versions and devices; no compatibility results are recorded here.
- Use developer tools while loading the page and trying its on-screen controls. Inspect the console for runtime errors and the network panel for failed local or remote requests. Check the Google Fonts requests and whether typography remains legible if they fail.
- Inspect `index.html` for local media references. If it references `music.mp3`, confirm the root file and path resolve; do not infer that the file is loaded or played merely because it exists. For any hosted version, check the deployed path and filename capitalization.
- Compare narrow mobile-sized and wide desktop-sized viewports. Check that the visualisation, changing x and y values, and controls remain visible and usable; where practical, also review on an actual mobile device.
- After changing the animation or layout, check the plotted curve against the displayed values and repeat the console, network, and viewport review.

## Manual review checklist

These are review steps, not verified results.

- Open the root `index.html` or use the local preview steps above. Review the animation and displayed x and y values.
- Try the on-screen controls defined in `index.html` and observe their effect on the visualisation and values.
- After changing the animation, controls, or fonts, repeat the relevant browser and layout checks above.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check keyboard access, logical focus order, and visible focus indicators for every on-screen control.
- Review controls for meaningful accessible names. Check that changing x and y values are available as text and whether the curve needs a text explanation.
- Check text and control-label contrast against their backgrounds, including around the visualisation.
- Because the experiment is animated, check behavior with the operating system's reduced-motion preference enabled and whether the visualization remains usable.