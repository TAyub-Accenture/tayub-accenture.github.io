# Taha Ayub — One-Pager Resume Site

A static, dark-mode, single-page resume site. No build step. Just open `index.html`.

## Files

- `index.html` — page content (look for `<!-- EDIT: ... -->` markers)
- `styles.css` — dark theme + print-friendly styles
- `photo.jpg` — your headshot (replace this file to change the photo)
- `README.md` — this file

## Editing the resume

Open `index.html` in **Notepad**, **VS Code**, or any text editor. Every editable
spot has an `<!-- EDIT: ... -->` comment right above it. Change only the text
between the tags — never the tags themselves.

**To swap the photo:** drop a new image into this folder, named exactly
`photo.jpg` (overwriting the old one), then refresh the browser. A square-ish
photo at 400×400 px or larger looks best.

**To add a new role:** copy a whole `<article class="role">...</article>` block
in the *Selected Client Experience* section and edit its contents.

**To remove a role:** delete the entire `<article class="role">...</article>`
block.

## Preview locally

Double-click `index.html`, or run a tiny static server from this folder:

```powershell
# Python 3
python -m http.server 8080
# then open http://localhost:8080
```

## Deploy free on GitHub Pages

### 1. Create the GitHub repo

1. Go to https://github.com/new
2. Repository name: `my-website` (or `taha-ayub.github.io` for a root URL — see step 4)
3. Public, no README/license (we already have files locally), then **Create**

### 2. Push this folder

In PowerShell from `C:\Users\taha.ayub\Projects\my-website`:

```powershell
git init
git add index.html styles.css README.md
git commit -m "Initial one-pager resume site"
git branch -M main
git remote add origin https://github.com/<your-github-username>/my-website.git
git push -u origin main
```

Replace `<your-github-username>` with your actual GitHub handle.

### 3. Enable GitHub Pages

1. In the repo on github.com → **Settings** → **Pages**
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`, then **Save**
4. Wait ~1 minute. Your URL will be:
   `https://<your-github-username>.github.io/my-website/`

### 4. (Optional) Root URL trick

If you name the repo exactly `<your-github-username>.github.io`, the site lives at
`https://<your-github-username>.github.io/` (no `/my-website` suffix).

## Updating later

```powershell
git add .
git commit -m "Update resume"
git push
```

GitHub Pages redeploys automatically within a minute.

## Print / Save as PDF

Click **Print / Save as PDF** in the footer (or `Ctrl+P`). The print stylesheet
switches to a clean light layout that fits well on one page.
