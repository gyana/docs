# CSV uploads reference

Tips on how to troubleshoot the CSV integration.

The CSV file format is not fully standardised, which means there is a huge variety in the formatting of data outputted from different systems (e.g. how are quotes escaped, how are newline characters treated).

Our CSV importer is designed to be permissive as possible, e.g. accepting jagged rows and quoted newlines.

If your CSV fails to import, here are a few steps you can try:

*   Make sure your CSV file has a header row. This is required for our importer. (If not, open with Excel/Google Sheets and add one.)
    
*   Read the error message and see if it helps.
    
*   Check your CSV is actually ""comma-delimited"". If the separator between records is a tab or pipe (`|`), you can set that in the **Configure** advanced settings.
    
*   Upload the CSV file to Google Drive, open as a Google Sheet and use the Google Sheets integration. (This works because Google Sheets is particularly good for problematic CSV files.)