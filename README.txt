Public Health Calculator: The Essentials, website version 1.2
A WizeLabs initiative of WizeLabs Health.
Created and compiled by Dr Surendran Venkataraman and Dr Angusubalakshmi Rajasivachalam. (c) 2026. All rights reserved.

Upload every file in this folder to the top level of a GitHub repository named phc-essentials, then turn on GitHub Pages
(Settings > Pages > Deploy from a branch > main > / (root)). The site will open at https://docsuren.github.io/phc-essentials/
If you choose another repository name, the QR codes in reports and the app's config link will point to the wrong address;
tell Claude the new address and the files will be rebuilt.

index.html             The application (works offline after the first visit)
manifest.webmanifest   Makes the site installable on phones
sw.js                  Enables offline use. Its version number changes with each release
config.json            Holds the address of the Google Sheet board used by the @ icon
PHC-Essentials.apk     The Android app offered for download from the menu
icon-192.png, icon-512.png, maskable-512.png, favicon-48.png   App icons from the logo

To connect the @ board (queries, feedback, discussion) and the visitor count:
1. Create a Google Sheet, open Extensions > Apps Script, paste community_google_script.txt, save, run setup once.
2. Deploy > New deployment > Web app; Execute as: Me; Who has access: Anyone. Copy the web app address.
3. Edit config.json so that it reads:  { "api": "https://script.google.com/macros/s/YOUR_ID/exec" }
The Android app reads the same config.json from the website, so it needs no rebuild.

Keep the signing key (phc-essentials-release.jks) safe and private. Do not upload it to GitHub.
Every future update of the Android app must be signed with the same key, or phones will refuse to update.
