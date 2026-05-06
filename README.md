🍀 Lucky Number Picker
A sleek, mobile-optimized web application built with Google Apps Script and hosted via GitHub Pages. This tool allows users to generate permutations of 4-digit numbers with a high-quality "slot machine" animation and automatically logs the results to a Google Spreadsheet.

🚀 Key Features
Permutation Engine: Automatically calculates all unique mathematical permutations for any 4-digit input.

Dynamic UI:

Responsive split-screen layout (70:30) for mobile and desktop.

Animated digit "spinning" effect for a premium user experience.

Image rotation gallery for visual engagement.

Google Sheets Integration: Saves every "Go!" result with a timestamp, base number, and chosen permutation to a backend spreadsheet.

History Tracking: Fetches the last 50 entries directly from the spreadsheet to display in the app.

🛠️ Technical Stack
Frontend: HTML5, CSS3 (Flexbox, Dynamic Viewport Units dvh), and Vanilla JavaScript.

Backend: Google Apps Script (GAS) utilizing HtmlService and SpreadsheetApp.

Data Storage: Google Sheets (used as a lightweight NoSQL database).

Deployment: Embedded via <iframe> with ALLOWALL frame options to support custom domains and GitHub Pages.

📦 Setup & Deployment
1. Google Spreadsheet Setup
Create a new Google Sheet.

Rename the first tab to Sheet1.

Add headers to the first row: Timestamp, Base Number, Permutation.

2. Google Apps Script (Code.gs)
Open Extensions > Apps Script from your sheet.

Paste the doGet, saveToSheet, and getHistory functions.

Crucial: Use .addMetaTag('viewport', 'width=device-width, initial-scale=1') in your doGet function to ensure mobile scaling works correctly.

3. Web Deployment
Click Deploy > New Deployment.

Select Web App.

Set Execute as: Me.

Set Who has access: Anyone.

Copy the Web App URL.

4. GitHub Integration
Paste the provided index.html into your GitHub repository.

In your GitHub index.html, ensure the iframe src points to your Google Web App URL.

The CSS includes overflow: hidden and height: 100dvh to ensure a "no-scroll" app-like experience.

📝 Usage
Input: Enter 4 digits to see available permutations.

Randomize: Leave the input blank and click "Go!" to generate a random 4-digit base.

Pick: Select how many results you want to "win" from the total permutations.

Reset: Clears all states and stops active animations immediately.

⚠️ Maintenance Note
When updating the frontend logic in Google Apps Script, remember to Redeploy as a New Version to ensure the changes reflect inside the GitHub iframe.
