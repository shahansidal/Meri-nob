MERI NOTEBOOK — iPhone Offline PWA

FILES
- index.html: notebook website
- sw.js: offline app-shell cache
- manifest.webmanifest + icons: install metadata

INSTALL ON IPHONE
1. Upload these files together to an HTTPS static host (for example GitHub Pages, Netlify, or your own HTTPS hosting). Keep the filenames and folder structure unchanged.
2. On iPhone, open the HTTPS site in Safari (not an in-app browser).
3. Let it load once while online. Then tap Share -> Add to Home Screen -> Add.
4. Open it from the new Home Screen icon. Open once online before going offline so the service worker can cache the app shell.
5. Add a test topic and photo, close/reopen the Home Screen app, and verify it is still there.
6. Use Backup regularly. Save the downloaded JSON backup in Files or iCloud Drive.

STORAGE AND LOSS WARNING — PLEASE READ
- Notes and photos are stored in this website's IndexedDB on this iPhone. Photos are stored as image Blobs, not just temporary page previews or localStorage strings.
- The service worker caches the app files for offline opening; it does NOT back up your notes/photos.
- Browser/site data deletion, clearing Safari website data, uninstalling/removing the Home Screen web app, some device resets, storage corruption, or iOS storage eviction can still erase local IndexedDB data. No website can honestly guarantee that data survives those actions.
- The app requests persistent storage when the browser supports it, but iOS may not grant or expose this. This is not a substitute for backup.
- Keep at least two backups (e.g. Files on iPhone + iCloud Drive/Mac). After important photo additions, create a fresh backup and confirm the JSON file exists in Files.
- Restore replaces the current notebook after confirmation. Back up the current copy first.
- Avoid Private Browsing. First install/open and test while online. Do not delete website data if you need the local notebook.

BACKUP FORMAT
One JSON file includes topic text and all photo data. Large photo libraries create large backup files.
