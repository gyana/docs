# Google Sheets reference

Tips on how to troubleshoot the Google Sheets integration.

## All rows are blank

If you don't add an explicit cell range, the Google Sheets integration will try to infer the cell range in the first sheet by looking at cells with content.

It's possible that if your Google Sheet has a blank cell or a cell with whitespace, this will be included and distort the cell range. For example, we saw an example where a 100 row dataset had a blank cell at row 10,000, and so the imported data had 9,900 blank rows.

The solution is either to copy the data into a new sheet (and delete the old sheet), or explicitly provide a cell range.

## The header is wrong

For the Google Sheets integration, the first row of the data must be the header values (i.e. the column names). If you don't include this, the first row of data will become the column names.

## Schema auto-detection fails

When we import a Google Sheet, we use the top 500 rows of data to infer the schema. If for example, the top 500 values for a column are a number, but further down there is a string, you might get an error like `Could not convert value to integer. Row XYZ, Col AB.`

In the short term, the solution is to manually move that row to the top and repeat the import. We're work on a fix to avoid this error in future.