# Sky Vivaldi

Four climates, side by side.

A browser tool for learning the EnergyPlus Weather (EPW) file format and comparing climates.

**Live app:** https://shafiarch.github.io/Sky_Vivaldi/

## What it does

- Shows the year as a 3D layered chart ("climate ridges") at the top, one layer per file, or daily max, mean and min for a single file.
- Opens up to four `.epw` files side by side. Use the **+** button to add a pane, or drop several files on the page.
- Shows how the file is built: the eight header lines, then one record per hour with 35 comma separated fields.
- Decodes the header (location, design conditions, typical and extreme weeks, ground temperatures, calendar).
- Lists all 35 hourly fields with units, missing codes and each file's statistics.
- Charts any field: hour by day heatmap, monthly range, average day by month, daily envelope, plus overlay charts when several files are open.
- Reads any single record with every value labeled.
- Draws a wind rose for each file.
- Shows the whole file as a collapsible tree, like a JSON viewer, with paths and explanations for every node.
- Checks each file for common problems (missing header lines, short records, missing values, odd day lengths).
- Four themes: White, Night, Clay and Trace (an e-ink and newsprint palette).
- Fills the whole screen and adapts to phones, tablets, laptops and large monitors in portrait or landscape.

## Privacy and load

Everything runs in the visitor's browser. Files are never uploaded, and there is no server doing any work, so many students can use it at the same time without slowing each other down.

## Sample files

The built-in samples (marine, hot desert, cold continental) are synthetic. They are generated in the browser to show how the tool works and are not measured weather. Real EPW files are available from the EnergyPlus weather page and Climate.OneBuilding.org.

## Files

- `index.html` is the whole app: HTML, CSS and JavaScript in one file, with no build step and no dependencies other than Google Fonts.

## Run locally

Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server
```
