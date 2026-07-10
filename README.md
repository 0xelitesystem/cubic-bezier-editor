# Cubic Bezier Editor

A visual CSS `cubic-bezier()` easing editor with draggable control points, a live animation preview, and a copy button. No server, no tracking, no third-party scripts.

**Live demo:** https://0xelitesystem.github.io/cubic-bezier-editor/

## Use

Open `index.html` in any modern browser, or visit the GitHub Pages link in the repo description.

- Drag either control point on the curve to shape the easing.
- Read the four values in the numeric inputs, or type them directly.
- Watch a real element animate with the current easing in the live preview, and adjust the duration.
- Pick a preset: `linear`, `ease`, `ease-in`, `ease-out`, `ease-in-out`, or an overshoot curve.
- Copy the `cubic-bezier(a, b, c, d)` string with one click.

The x axis is time (0 to 1) and the y axis is progress. Control point x values are constrained to the 0 to 1 range, which is what CSS requires. The y values can go outside that range to create overshoot and anticipation, and the canvas shows that overshoot.

The curve is drawn with real De Casteljau evaluation of the cubic with endpoints fixed at (0,0) and (1,1), so what you see matches how the browser interpolates the easing.

## Why this exists

Easing editors are useful but the common ones load frameworks, analytics, and sometimes an account wall. This is one HTML file: shape the curve, preview it, copy the string, done. The Bezier math is plain JavaScript you can read.

## Privacy

Everything runs in your browser. There are no network calls at all. Verify by viewing the page source or by opening DevTools and watching the network tab.

## Run locally

```bash
git clone https://github.com/0xelitesystem/cubic-bezier-editor
cd cubic-bezier-editor
# Open index.html in your browser, or:
python -m http.server 8000
```

## Build

There is no build. It is a single HTML file with inline CSS and JavaScript.

## License

MIT.

## Related

- [gradient-generator](https://github.com/0xelitesystem/gradient-generator)
- [box-shadow-generator](https://github.com/0xelitesystem/box-shadow-generator)
- [css-clamp-calculator](https://github.com/0xelitesystem/css-clamp-calculator)
