# Samaj Survey — Google Sheets version

## 1. Create the Google Sheet

Create a new Google Sheet. Copy the ID from its URL:

https://docs.google.com/spreadsheets/d/YOUR_SHEET_ID/edit

The value between `/d/` and `/edit` is your Sheet ID.

## 2. Create the backend

In the Sheet:
Extensions -> Apps Script

Delete the existing code and paste `google_apps_script.gs`.

Replace:

PASTE_YOUR_GOOGLE_SHEET_ID_HERE

with your actual Sheet ID.

Save.

## 3. Deploy the backend

In Apps Script:

Deploy -> New deployment
- Type: Web app
- Execute as: Me
- Who has access: Anyone

Click Deploy and copy the Web app URL.

## 4. Connect the survey

Open `index.html`.

Find:

const GOOGLE_SCRIPT_URL = "PASTE_YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL_HERE";

Replace the placeholder with the Web app URL.

Save `index.html`.

## 5. Use the app

Open `index.html` in Chrome and submit a test response.

A `Responses` tab will be created automatically in the Google Sheet.

Every survey submission becomes one row.

## Privacy/security note

This form contains personal and family information. The Google Sheet should be access-controlled and shared only with people who need the data. The current app uses the Google Apps Script "Anyone" web-app setting so respondents can submit without signing into Google. Do not publish the Sheet itself publicly.
