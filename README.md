# Sudhir Karmarkar — Astrology Website

A single static HTML file (`index.html`) — no build step, no server, no dependencies. Works on any static host. Content switches instantly between **English / हिन्दी / मराठी** using the buttons in the top navigation.

## Before you deploy
The site is already set up with the real contact number: **+91 77988 48859**. If it ever changes, search `index.html` for `917798848859` (it appears 6 times: two `tel:` links, two `wa.me` WhatsApp links, and two visible text spots) and replace it everywhere.

## Deploy options

### Vercel
1. Go to vercel.com → **Add New Project** → **Deploy without Git** (or drag-and-drop).
2. Drag the folder containing `index.html` into the upload area.
3. Deploy — you'll get a `*.vercel.app` URL instantly. Add a custom domain under Project → Settings → Domains if you have one.

### GitHub Pages
1. Create a new GitHub repo, upload `index.html` to the root.
2. Go to **Settings → Pages** → set Source to the `main` branch, root folder.
3. Your site goes live at `https://<username>.github.io/<repo-name>/`.

### GoDaddy (or any shared hosting / cPanel)
1. Log in to GoDaddy hosting → **File Manager** (or connect via FTP).
2. Upload `index.html` into the `public_html` folder (this is your domain's root).
3. Visit your domain — it will load automatically since `index.html` is the default file name.

### Azure Static Web Apps
1. In the Azure Portal, create a **Static Web App** resource.
2. Choose "Other" as the deployment source (no GitHub needed) and use the Azure CLI or Static Web Apps CLI (`swa deploy`) pointing at the folder with `index.html`.
3. Alternatively, push the file to a GitHub repo and connect it during Static Web App creation for automatic deploys.

### Netlify (bonus option)
Drag the folder onto app.netlify.com/drop — same as Vercel, live in seconds.

## Notes
- All three languages live in one file — nothing to rebuild or re-upload when switching hosts.
- The page is fully responsive and works without JavaScript frameworks, so it will load fast on any plan, including the cheapest shared hosting.
- If you want a custom domain (e.g. `sudhirkarmarkar.com`), buy it from GoDaddy or any registrar and point its DNS/nameservers to whichever host you choose above — each platform's dashboard has a "Domains" section with exact instructions.
