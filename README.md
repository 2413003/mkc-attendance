# MK Chess Attendance

A static GitHub Pages app for MK Chess attendance analytics and faster session sign-in.

## What It Does

- Shows aggregate attendance analytics from the current Excel workbook.
- Runs a fast returning-attendee search once private roster data is imported, auto-loaded, or created.
- Lets first-time attendees sign in with name, junior/adult, email, and emergency phone.
- Stores private attendee data in the browser on the club device using `localStorage`.
- Exports JSON backups and attendance CSV files.
- Imports the existing Excel workbook client-side using the embedded SheetJS browser script.

## Privacy

The public app files include only aggregate counts from the workbook. Names, emails, and phone numbers are not embedded in the deployed HTML. Importing the workbook happens in the browser and does not upload the file anywhere.

If the Excel workbook is uploaded beside `index.html` with the filename `(copy) 04.02.2026 bletchley mk chess session attendance.xlsx`, the app will auto-load it on first run and create the local player profiles. That workbook file is then publicly accessible to anyone with the Pages URL, so only do this if that is acceptable for your club's privacy setup. Otherwise, use Admin -> Import workbook on the club device.

The `.gitignore` excludes Excel/CSV files, `private/`, and `exports/` to reduce the risk of committing attendee data.

If a club device ever needs a clean local reset, open the app with `?reset=1` once. For example: `https://your-pages-url/?reset=1`.

## Deploy On GitHub Pages

Publish the repository root as a static site. No build command is required.

For GitHub Pages, use:

- Source: deploy from branch
- Folder: `/ (root)`

Then open `index.html` from the published Pages URL.
