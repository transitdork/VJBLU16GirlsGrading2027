# VJBL U16 Girls Grading Map PWA

This GitHub Pages package installs as a home-screen app and displays the live grading map. The shared map service keeps the results database and manager PIN; this repository contains no PIN or result data. Updates pushed to `main` deploy automatically. Installed apps check for a new GitHub Pages build when opened and reload when the service worker changes.

## Publish

1. Create a GitHub repository named `vjbl-u16-grading-map` and upload these files to its `main` branch.
2. In **Settings → Pages**, set the source to **GitHub Actions**.
3. Wait for the **Deploy grading map PWA** workflow to finish. GitHub will show the Pages URL in the workflow run and Pages settings.
4. Open the Pages URL in Safari on iPhone/iPad, tap **Share → Add to Home Screen**, and enable **Open as Web App** if iOS shows that option.

## Notes

- The GitHub Pages app uses a full-screen frame pointed at the current live grading map, preserving the shared results and manager edit flow.
- The app icon is the supplied VJBL U16 logo in `assets/`.
- GitHub commits automatically deploy. An installed app checks for the latest wrapper files on launch; a new service worker causes a reload. The embedded map itself also loads its latest published version from the live map service.
- Results entry still requires the existing manager PIN. Do not store that PIN in this repository.
- The app needs an internet connection to load the live map and shared results.
