# Circular lake travel-time applet

## Deploy to the existing GitHub Pages repository
1. Extract this ZIP.
2. Upload index.html and .nojekyll from this folder to the root of the Optimizing-Travel-Time-Through-Land-and-Water repository, replacing index.html.
3. In repository Settings > Pages, choose Deploy from a branch, main, / (root), and Save (or keep those settings if already enabled).
4. Wait for the Pages deployment to finish, then refresh the existing website.

No installation, build step, external library, or account is needed to run the applet. You can also open index.html directly in a browser.

## Corrections
- Exact radius 150 m, so the diameter is 300 m (previously 300.6 m).
- Robot 1: water 1 m/s and land 3 m/s. Robot 2: water 2 m/s and land 3 m/s.
- Exact editable speeds; draggable selector rounds its state to the same two decimal places displayed.
- Flexible page height and scrolling replace clipped fixed-height content; compact laptop layout and stacked narrow-screen layout.
- Keyboard-accessible route slider supplements dragging C; preset buttons preserve the chosen route.
- Canvas resolution follows its actual display dimensions.

## Mathematics
Let theta be angle C-O-B in radians, from 0 to pi.
Water distance = 300 cos(theta/2) metres.
Land distance = 150 theta metres.
Total seconds = 300 cos(theta/2)/waterSpeed + 150 theta/landSpeed.

For the supplied robots the time is concave as a function of theta, so a minimum occurs at an endpoint:
- Robot 1: all shore, 150 pi / 3 = 157.0796... seconds.
- Robot 2: straight across the diameter, 300 / 2 = 150 seconds.

Validation: script execution and 2,007 mathematical cases passed; browser controls confirmed 157.08 s at the shore endpoint and 150.00 s for Robot 2 across water. Narrow browser preview checked; physical iPad testing was not available.
