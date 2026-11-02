# How to update your website

Your website is built from the spreadsheet files in the **_data** folder. You never edit the website itself.
Edit a file, upload it to GitHub, wait one or two minutes, and the site updates.

## The files

| File | What it controls |
|---|---|
| profile.csv | Name, title, bio, links, photo, contact details |
| news.csv | Short news items |
| research_interests.csv | Your research interests |
| papers.csv | Work in progress, working papers, published papers, dissertation, other |
| employment.csv, education.csv | Positions and degrees |
| coursework.csv | Courses you have taken |
| talks.csv | Presentations and workshops |
| awards.csv | Grants and awards |
| skills.csv | Programming, languages, software |
| teaching.csv | Courses you have taught or assisted |

## The easy way: the CVtoGit CSV Editor

Open the editor using the link we sent you (bookmark it). It shows your files as a table. Your files are not uploaded, because everything happens in your browser. If you prefer to work offline, use the "Download this editor for offline use" link at the bottom of the editor page and open the saved file by double-clicking it.

1. Drag your CSV files into the window, or click **Open CSV files**.
2. Click any cell to change the text. Use **+ Add row** for a new entry, the arrows to reorder, and the x to delete a row.
3. Click **Download this file** (or **Download all**). The editor always saves the right format, with commas and accents intact.
4. Upload the downloaded files to the **_data** folder on GitHub (step 5 below).

## Opening a CSV in a spreadsheet instead

- **Google Sheets:** File, Import, Upload, choose **Comma** as the separator, then Import data.
- **Excel:** Data, From Text/CSV, set the delimiter to **Comma** and the encoding to **UTF-8**, then Load. Double-clicking a CSV in Excel can put everything in one column.

## How to edit with a spreadsheet

1. Download the file from GitHub (open it, then use the download button), or use the copy on your computer.
2. Open it in Google Sheets or Excel.
3. Change the text. **Add a row** for a new entry. **Delete a row** to remove one. The order of the rows is the order on your site.
4. Save as **CSV**.
   - In Google Sheets: File, Download, **Comma Separated Values (.csv)**. This is the safest option.
   - In Excel: Save As, **CSV UTF-8 (Comma delimited)**. In some countries Excel uses semicolons, which breaks the site. If that happens, use Google Sheets.
5. On GitHub, open the **_data** folder, click **Add file**, then **Upload files**, drop in the file, and click **Commit changes**. The new file replaces the old one.

## Rules

- **Do not change the first row** (the column names) and do not rename the files.
- A **blank cell hides that item**. For example, an empty Twitter value hides the Twitter link, and an empty Slides cell hides the Slides button.
- If **all rows of a section are deleted** (keep the first row), the whole section disappears.
- In **papers.csv**, the `section` column must be one of: `wip`, `working`, `published`, `dissertation`, `other`.
- Write plain text only. Do not type web page code.
- Links to files you upload (papers, slides) look like `files/mypaper.pdf`. Upload the PDF to the **files** folder.
- Your CV must be called **cv.pdf** and sit in the main folder. Your photo goes in the **assets** folder, and its path goes in profile.csv under `photo`, for example `assets/headshot.jpg`.

## If something goes wrong

- If the site does not change after five minutes, open the **Actions** tab on GitHub. A red mark means the file has a problem.
- The usual causes are a changed first row, a missing file, or a semicolon-separated file.
- You can always go back: open the file on GitHub, click **History**, and restore the earlier version.
