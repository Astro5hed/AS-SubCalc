# AS SubCalc: version history

## v1.0.5

- **Read noise** column, in electrons, replaces e-/ADU. With darks it is headed **Read + dark noise**, as a dark also holds a little dark-current noise; bias frames give the read noise alone.
- **e-/ADU is no longer shown.** Many 12- and 14-bit cameras scale their values up to fill 16-bit files, so the figure measured from the file came out 4 or 16 times below the published one. The read noise in electrons is not affected by this scaling. Nothing else depended on e-/ADU: the sub lengths are unchanged.
- The results table's columns are sized to fit their contents, with spare width shared out, so the table always fills the window.
- Clearer message when two dark or bias frames have different lengths, for example "a 10 ms frame and a 1 ms frame".

## v1.0.4

- **Fixed:** on a test frame with no saturated pixels and nothing brighter than about 4,180, the app took a 16-bit camera for a 12-bit one, and the longest sub came out about 16 times too short. It now assumes 65,535, right for nearly all astro cameras.
- **Camera bit depth** setting, for cameras that save unscaled 12-bit or 14-bit values. Only used when nothing in the test frame has clipped.
- A note says when the camera's ceiling had to be assumed, because nothing in the test frame had clipped.
- A longest sub beyond 30 minutes is shown as **over 30 min**: at that point saturation is not what stops you, and guiding, satellites and frame count set the practical limit.
- A few bright pixels that happen to share the same value are no longer mistaken for the camera's ceiling.

## v1.0.3

- **Point of diminishing returns** (factor 25, where the camera adds only 2%) marked on the range bar in blue and given in the text. If saturation stops you before that point, the app says so instead.

## v1.0.2

- **Two bookends.** The result is now a range: the shortest sub that overcomes read noise by a chosen factor, and the longest sub before a chosen share of pixels saturates.
- **Read noise factor** setting, from a list (5, 10, 15, 20, 25) or typed in, with the noise it adds shown beside it. Default 10.
- **Saturation limit** setting, as a share of pixels, with the number of pixels shown beside it. Default 0.01%.
- A **range bar** shows the usable range on a time scale, with a mark where the test frame sits.
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
