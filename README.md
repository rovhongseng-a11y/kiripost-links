# Kiripost link-in-bio page

The page behind the link in Kiripost's Instagram bio, served at **https://links.kiripost.com** (GitHub Pages).

## Files

| File | What it is |
|---|---|
| `index.html` | The whole page. Edit only the `SETTINGS` block near the bottom (Sheet address, buttons, tabs, tagline). |
| `assets/` | Logos (navy for light mode, white for dark mode) and icons. |
| `cards/` | Optional: Instagram card images uploaded here are served at `https://links.kiripost.com/cards/<file name>`. |
| `CNAME` | Tells GitHub Pages to use links.kiripost.com. Don't delete it. |

## Adding a post (no code)

Open the Google Sheet **Kiripost link-in-bio posts**, insert a new row **under the header row** (newest on top) and fill in:

| Column | What to put | Example |
|---|---|---|
| date | The post date as YYYY-MM-DD | 2026-10-05 |
| image | Address of the image to show (4:5 works best) | https://links.kiripost.com/cards/factory-union.jpg |
| link | The story's address on kiripost.com | https://kiripost.com/stories/… |
| headline | The headline shown under the tile | Qi Heng Xin Factory Alleged of Union Busting… |
| tag | Short topic label | Business |
| tab | Leave empty, or Data and/or Academy (comma between) to also show it in those tabs | Data |
| hide | `yes` to hide a post without deleting the row | |

The page reads the Sheet each time someone opens it. Google refreshes the published copy every few minutes, so a new row can take up to about 5 minutes to appear.

## If the Sheet stops loading

The page then shows the `BACKUP_POSTS` list in `index.html`. Check that the Sheet is still published (File > Share > Publish to web) and that the address in `SETTINGS.sheetCsvUrl` matches.
