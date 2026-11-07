# Lally Namol Photography — Website

A clean, responsive photography portfolio for GitHub Pages, including a browser-based portfolio manager at `admin.html`.

## Publish to GitHub Pages

1. Create a **public** GitHub repository (for example, `lally-namol-photography`).
2. Upload all website files and folders from this ZIP to the repository root. **Do not upload the outer `lally-namol-photography` folder as a nested folder.**
3. In the repository, open **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. Your site will be at `https://YOUR-USERNAME.github.io/lally-namol-photography/` (or your custom domain).
5. Visit `https://YOUR-USERNAME.github.io/lally-namol-photography/admin.html` to manage the site.

## Updating photos and website text from the portal

GitHub Pages is static hosting, so the management page uses GitHub's API to commit changes into your repository directly.

1. In GitHub, go to **Settings → Developer settings → Personal access tokens → Fine-grained tokens**.
2. Create a token scoped to **only this website repository**, granting **Contents: Read and write**. GitHub may require approval on organizational repositories.
3. Open `admin.html`. Enter the repository owner's GitHub username, repository name, branch (`main`), and token. Leave folder path blank unless the website files were placed in a subfolder.
4. Use the text editor, upload photos, set photo categories, remove gallery items, or upload a hero image / logo. Select the relevant **Publish** button.
5. Reload the website after GitHub Pages deploys the changed files. Deploys are not always instantaneous.

**Security:** Never paste your token into a code file, commit it to GitHub, or send it to anyone. The portal holds it in `sessionStorage`, scoped to that tab's session. Anyone visiting `admin.html` can see the login interface, but they cannot edit without a GitHub token with write access. For stronger security, consider a dedicated authenticated CMS/backend.

## Enquiry form

The enquiry form opens a new WhatsApp chat with the visitor's details prefilled, directed to **+61 451 941 830**. The visitor must press Send in WhatsApp to complete the enquiry. This works without a server, database, or email setup. If you prefer email submissions stored in an inbox, you will need to supply an email address and configure a form provider.

## Photos and logo

The initial portfolio, hero image and about image are **sample Unsplash photography**, not photos belonging to Lally Namol Photography. Replace them in the portal with your own work before going live. The initial geometric camera-logo mark is a temporary built-in SVG; upload your official transparent logo in the portal to replace it.

## Website files

- `index.html` — public-facing website.
- `style.css` — responsive styling.
- `content.json` — site copy, social details, photos.
- `js/site.js` — gallery, mobile menu, WhatsApp enquiries.
- `admin.html`, `admin.css`, `js/admin.js` — GitHub publishing portal.
- `assets/logo.svg` — placeholder logo mark.

## Contact links

- India: +91 98153 25750
- Australia: +61 451 941 830
- Instagram / Facebook: prefilled from supplied links in `content.json`.

To test locally, run `python -m http.server 8000` in the directory and browse `http://localhost:8000`. Opening `index.html` with `file://` may block loading `content.json` in some browsers.
