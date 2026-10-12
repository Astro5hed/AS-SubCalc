# AS SubCalc: version history

## v1.0.2

- **Two bookends.** The result is now a range: the shortest sub that overcomes read noise by a chosen factor, and the longest sub before a chosen share of pixels saturates.
- **Read noise factor** setting, from a list (5, 10, 15, 20, 25) or typed in, with the noise it adds shown beside it. Default 10.
- **Saturation limit** setting, as a share of pixels, with the number of pixels shown beside it. Default 0.01%.
- A **range bar** shows the usable range on a time scale, with a mark where the test frame sits.
- The **point of diminishing returns** (factor 25, where the camera adds only 2%) is marked on the range bar in blue and given in the text.
- When the two limits cross, the app says so and suggests what to do.
- Changing either setting updates the results straight away. Both are remembered between runs.
- The results table now shows Shortest sub and Longest sub for each channel, in place of the 10%, 5% and 2% columns.
- **Update check:** once a day the app can check GitHub for a newer version and show a link to it. It can be turned off.
- Wider window.

## v1.0.1

- The window scrolls when the screen is too short for it, with the buttons always in view. On larger screens it opens at full height with no scroll bar.
- Master darks are no longer accepted: they gave sub lengths that were too long.
- Two frames must be the same kind and length (two darks or two bias frames), and the same file cannot be used twice.
- The mouse wheel scrolls the window instead of changing the drop-down boxes by accident.

## v1.0.0

- First release.
