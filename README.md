# Aurelia Bloom — Commission Website

A responsive, single-page commission website built with plain HTML, CSS, and JavaScript. No framework or paid hosting is required.

## Files
- `index.html` — the entire website. Edit text, prices, links, colors, and gallery here.
- `CNAME.example` — example custom-domain configuration. Rename to `CNAME` and put your domain inside it only after you own/configure the domain.

## Before publishing
Search in `index.html` for:
- `Starting at $300`, `$100`, `$70`, `$10`, and `Custom quote` — confirm these are your current prices.
- `https://x.com/AureliaArt` — replace if your current X link differs.
- `https://discord.com/` — replace with your invite/profile link.
- `https://ko-fi.com/` — replace with your exact Ko-fi page.
- FAQ answers about payment, revisions, and commercial rights — make sure they match your actual terms.
- Placeholder art and portfolio boxes — replace them with your own images.

## Add your artwork
1. Create an `images` folder in the repository.
2. Upload your image files there, e.g. `images/hero.png`.
3. In `index.html`, find the relevant gallery placeholder. Replace the placeholder `<div class="gallery-placeholder">...</div>` with:
   `<img src="images/your-image.png" alt="Short description of your artwork">`
4. Add `has-image` to that gallery item's class, for example `class="gallery-item has-image"`.
5. For the hero, replace the contents of `<div class="art-frame">...</div>` with:
   `<img src="images/hero.png" alt="Aurelia Bloom artwork" style="width:100%;height:100%;object-fit:cover;position:absolute;inset:0">`
   Make sure the artwork is yours or you have permission to display it.

## Publish on GitHub Pages
1. Sign in or create an account at https://github.com/
2. Click **New repository**. Name it something like `aurelia-commission-site`.
3. Set it to **Public** (the simplest GitHub Pages setup for a beginner), then create the repository.
4. On the repository page, choose **Add file → Upload files**.
5. Upload `index.html` (and any image files/folders you added), then click **Commit changes**.
6. Open **Settings → Pages**.
7. Under **Build and deployment**, choose **Deploy from a branch**.
8. Choose branch **main** and folder **/(root)**, then click **Save**.
9. Wait for the published URL to appear in Settings → Pages. It will usually look like `https://YOUR-USERNAME.github.io/aurelia-commission-site/`.

## Connect a custom domain
You must own or register a domain first; GitHub Pages does not provide a custom domain for free.
1. Buy/register a domain through a domain registrar of your choice.
2. In your repository, open **Settings → Pages → Custom domain**, enter your domain (e.g. `www.example.com`) and save.
3. At your domain registrar, configure the DNS records using GitHub's current official instructions:
   https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
   For a `www` subdomain, this is commonly a `CNAME` record pointing to `YOUR-USERNAME.github.io` (no repository name). For an apex/root domain such as `example.com`, GitHub documents the required `A`/`AAAA` records. Use the exact current records shown in GitHub's documentation.
4. Wait for DNS to propagate. In Settings → Pages, enable **Enforce HTTPS** when available.
5. Keep the `www` and root/apex domain configuration consistent with GitHub's documentation. Avoid setting DNS records to an IP address from an unofficial source.

## Important limitations
- GitHub Pages is static hosting. This template does not process payments, collect orders into a database, or provide a private admin panel. The buttons link visitors to your contact/commission platforms.
- A custom domain costs money from the domain registrar; GitHub Pages hosting itself can be free.
- Do not upload private client files or personal information to a public repository.
