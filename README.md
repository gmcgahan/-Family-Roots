# FamilyRoots Web App (phone-friendly PWA)

FamilyRoots is an offline-first genealogy starter designed to run in a mobile browser and be added to an Android home screen.

## Features in this first version
- Family tree explorer with expandable descendant branches
- Individual profiles with alternate names, birth/death details, biography, notes, and optional profile picture
- Father, mother, spouse/partner links and child creation from a profile
- Chronological timeline events for births, baptisms, census entries, marriages, military service, migration, education, employment, property, court records, death, burial, and other events
- Search across names, places, and notes
- JSON backup export and restore
- Browser-local storage; no account or server database is used
- Offline app-shell caching after the first successful load on a secure hosted site

## Important limitations
This is a starter, not yet the complete genealogy system. It does not currently support GEDCOM import/export, attached source documents, gallery albums, citations as structured records, a full zoom-and-pan tree canvas, or cloud sync. Data is stored in the current browser profile. Clearing site data can erase it, so export backups regularly. Browser storage has size limits, especially for photos. Choose small profile pictures. No fictional sample people are inserted.

## Use it on Android
A Progressive Web App needs to be hosted over HTTPS for reliable installation and offline caching. Opening `index.html` directly from a downloaded ZIP is useful for inspecting the files but will not enable the install prompt or service worker.

A phone-only route is GitHub Pages:
1. Sign in or create an account at https://github.com.
2. Create a new public repository named `familyroots` (or another name).
3. Upload `index.html`, `manifest.webmanifest`, and `sw.js` from this folder to the repository root. You can use GitHub's website in Chrome and choose **Add file → Upload files**.
4. Open the repository's **Settings → Pages**. Under build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. Wait for GitHub Pages to publish, then open the HTTPS address shown in Pages on your Android phone.
6. In Chrome, tap the three-dot menu and choose **Add to Home screen** or **Install app** if offered.

## Data and privacy
Family data stays in browser storage on this device unless you export/share a backup or the browser itself syncs data. This starter does not transmit family data to a server. Treat backups as sensitive, especially when living people are included. Keep at least one backup in a safe place outside the phone.

## Development
All app logic is in `index.html`. The app uses plain HTML, CSS, and JavaScript so it can be edited from a phone without a build system. The service worker caches the app shell for offline reopening after the first online visit.
