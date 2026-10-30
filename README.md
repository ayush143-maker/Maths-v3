# Maths-v3

An animated mathematical-art experiment built around the curve **y = -1/x**. The root `index.html` displays changing x and y values alongside the visualisation and defines the on-screen controls. The project includes `music.mp3` in the root folder.

## Project files and resources

- `index.html` — page entry point, visualisation, displayed values, and controls.
- `music.mp3` — local audio file; check `index.html` to determine whether and where the page references it.
- The page links to Google Fonts, including requests to `fonts.googleapis.com` and `fonts.gstatic.com`.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deployment-readiness checklist

The following are recommendations, not verified deployment results. No deployment host or publishing configuration is specified here.

- [ ] **Choose the correct published root/output.** The entry point is the root `index.html`. Configure the publishing process to serve the project folder containing `index.html` and the resources it references. Check that the published root does not point to a folder that omits the entry point or required assets. The supplied inventory lists no scripts, so do not assume a build output directory exists.
- [ ] **Keep relative asset paths valid.** Inspect `index.html` to see whether and where `music.mp3` is referenced. If it is used, include it at the corresponding path or update the page reference when moving or renaming it. Check filename capitalization and confirm that local resources are present at their referenced paths.
- [ ] **Account for external fonts.** Google Fonts requests require network access. A font request failure may change typography; distinguish it from a missing local resource.
- [ ] **Review content and configuration for safety.** The supplied root-file inventory lists no `.env.example` or separate configuration file. This static page has no server-side environment in which to keep secrets: anything placed in its HTML or delivered browser files can be viewed by visitors. Do not put passwords, tokens, or other secrets in the page or tracked files. Review the page and `music.mp3` for private information, and publish audio only if you have permission to distribute it.
- [ ] **Preview after publishing.** Open the published page and check that it loads from the intended root, the visualisation and displayed values appear as expected, and the on-screen controls have the intended effect. Check the browser console and network panel for failed page, media, or font requests. Compare displayed x and y values with the plotted curve when reviewing animation changes. This is a recommended manual review, not a completed check.

## Explore and troubleshoot

The page, visualisation, displayed values, and controls are defined in `index.html`. When changing the animation or interaction, keep the displayed values aligned with the plotted curve. Before moving or replacing `music.mp3`, check whether and where `index.html` references it. When a local resource is missing, compare its page reference with the file’s location and capitalization.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- [ ] Use Tab and Shift+Tab to check keyboard access, logical focus order, and visible focus indicators for every on-screen control.
- [ ] Review controls for meaningful accessible names. Check that changing x and y values are available as text and whether the curve needs a text explanation.
- [ ] Check text and control-label contrast against their backgrounds, including around the visualisation.
- [ ] Check behavior with the operating system’s reduced-motion preference enabled and whether the visualisation remains usable.

## Final release review

- Open `index.html` from the published location and confirm the page loads as expected.
- Test with network access available and keep a sensible fallback for externally loaded resources.
- Review the published result once on a narrow screen and once on a wider screen; treat this as a release check, not an automated test report.
