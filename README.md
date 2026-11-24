# Attendance Remark App

Daily staff attendance app: tick who is present, add remarks for anyone absent, plan leave, and copy a WhatsApp-ready message. Works offline and can be installed as an app (PWA).

**Data is stored only in each person's own browser (localStorage). Nothing is sent to any server or shared cloud storage.**

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app (HTML, CSS and JavaScript in one file) |
| `manifest.webmanifest` | PWA settings (name, icons, standalone display) |
| `sw.js` | Service worker that makes the app work offline |
| `icons/` | App icons (192, 512, maskable, Apple touch icon, favicon) |

No build step and no external libraries are needed.

## Publish on GitHub Pages

1. Unzip `attendance-app.zip` on your computer.
2. On github.com, click **+** then **New repository**. Name it (e.g. `attendance`), choose **Public**, and click **Create repository**.
3. On the empty repository page, click **uploading an existing file**.
4. Open the unzipped folder and select everything inside it (`index.html`, `manifest.webmanifest`, `sw.js`, `README.md` and the `icons` folder). Drag it all into the GitHub page. `index.html` must be at the top level, not inside another folder.
5. Click **Commit changes**.
6. Go to **Settings**, then **Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose branch **main** and folder **/ (root)**, then **Save**.
7. Wait 1 to 2 minutes and refresh. The site link appears at the top: `https://YOUR-USERNAME.github.io/REPO-NAME/`

## Install as an app

- **Windows or Mac (Chrome or Edge):** open the link, then click the install icon in the address bar, or open the menu and choose **Install Attendance** or **Create shortcut**.
- **Android (Chrome):** menu, then **Install app** or **Add to Home screen**.
- **iPhone or iPad (Safari only):** Share button, then **Add to Home Screen**.

## Updating the app later

1. Edit `index.html` and upload it to the repository again (replace the old file).
2. In `sw.js`, change `var CACHE = "attendance-v1";` to `"attendance-v2"` (then v3, and so on) so devices download the new version.

## Notes

- Each person and each device has its own separate data. Clearing browser data for the site erases it.
- On iPhone, the installed app has its own storage, separate from Safari. Use the installed app from the start.
- A free GitHub Pages site needs a public repository, so the code (including the staff names in the default list) is publicly visible. Anyone with the link can open the app.
