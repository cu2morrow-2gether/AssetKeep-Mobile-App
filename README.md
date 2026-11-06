# AssetKeep

A mobile-friendly, read-only asset inventory based on the 15 records in `Asset_for_AppSheet.xlsx`.

## Included
- Asset list with search and GOOD/BAD filtering
- Asset details and embedded asset pictures
- QR code display and scanning (camera / QR image / manual asset number)
- Dashboard with asset totals and condition charts
- Installable PWA shell for supported mobile browsers

## Publish with GitHub Pages
1. Create or open your GitHub repository.
2. Upload **all files and folders inside this project folder** to the repository root (not just the ZIP).
3. Commit the changes to your default branch.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select your default branch and `/ (root)`, then click **Save**.
7. Wait for GitHub Pages to publish, then open the URL it provides.

## Install on a phone
- Open the published HTTPS URL in a supported browser.
- Android/Chrome: use the browser menu and choose **Install app** or **Add to Home screen**.
- iPhone/Safari: use **Share → Add to Home Screen**.

## Important notes
- This version is intentionally read-only. It does not add, edit, or delete assets.
- Asset records and images are bundled into `index.html`; all visitors see the same original 15 records.
- This version does not synchronize edits because editing is disabled and there is no cloud database.
- QR camera scanning requires HTTPS and browser camera permission. GitHub Pages provides HTTPS.
- QR scanning uses the html5-qrcode library from a CDN, so that feature requires an internet connection. The rest of the app shell can be cached for offline opening after first visit.


## QR code photo scanning

On the Scan screen, choose **Scan from a QR photo** and select an image containing a QR code.
AssetKeep decodes the selected image locally in the browser using jsQR, then matches the decoded
asset number against the 15 records in the app. Keep the full QR code visible and use a sharp,
well-lit image. The QR decoder library is loaded from a CDN, so an internet connection is needed
when first loading the app.
