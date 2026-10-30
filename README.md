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

Before moving or replacing `music.mp3`, check whether and where `index.html` references it. Keep any existing relative path and filename aligned with the file, or update the reference when intentionally changing its location. The font links are external; local files must be available at their referenced paths.

## Troubleshooting

These are diagnostic checks, not reports of known problems.

1. Confirm you opened the root `index.html`, the experiment’s entry point.
2. If a local resource is missing, inspect its reference in `index.html`, confirm the file exists, and check the relative path and filename capitalization. Do not assume `music.mp3` is loaded without checking the page reference.
3. Inspect the browser console for errors and the network panel for failed page, media, or font requests. When reviewing animation changes, compare the displayed x and y values with the plotted curve.
4. Google Fonts requests require network access; local resources must be present at their referenced paths.

## Configuration and publishing

The listed root files contain no `.env.example` or separate configuration file. This static page has no server-side environment in which to keep secrets: anything placed in its HTML or delivered browser files can be viewed by visitors. Do not put passwords, tokens, or other secrets in the page or tracked files.

Review page content and `music.mp3` before publishing. Avoid including private information, and distribute audio only if you have permission to do so.

## Contributor handoff

Keep changes scoped to the intended page, animation, controls, or audio. Preserve existing filenames and relative references unless a change requires updating them; when changing a path, update the corresponding reference in `index.html`. In your handoff, briefly describe what changed and which files or references were affected. Manually review the result before publishing, including the relevant checks below. These are review steps, not verified results.

- Review the animation, displayed x and y values, and controls at narrow and wide viewport sizes.
- Try the on-screen controls defined in `index.html` and observe their effect on the visualisation and values.
- After changing animation, controls, layout, or resource references, inspect the browser console and network panel and confirm affected local resources load.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check keyboard access, logical focus order, and visible focus indicators for every on-screen control.
- Review controls for meaningful accessible names. Check that changing x and y values are available as text and whether the curve needs a text explanation.
- Check text and control-label contrast against their backgrounds, including around the visualisation.
- Because the experiment is animated, check behavior with the operating system’s reduced-motion preference enabled and whether the visualisation remains usable.