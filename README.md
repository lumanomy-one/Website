# Lumanomy landing page

Static GitHub Pages site for **Lumanomy — Asymmetric Value Creation**.

## Files

- `index.html` — landing page and SEO metadata
- `styles.css` — responsive presentation and clickable interaction zones
- `assets/lumanomy-hero.png` — approved Lumanomy landing-page visual
- `assets/favicon.svg` — browser icon
- `CNAME` — custom domain for GitHub Pages
- `.nojekyll` — tells GitHub Pages to serve the site as plain static files
- `robots.txt` and `sitemap.xml` — basic search-engine support

## Before publishing

### 1. Confirm the contact email

The CONTACT button currently uses:

`contact@lumanomy.com`

If that mailbox is not active, open `index.html` and replace both instances with the email address you want to use.

### 2. Create the GitHub repository

Create a new **public** repository, for example:

`lumanomy-site`

Upload the contents of this folder to the root of that repository. Do not upload the enclosing folder itself.

### 3. Turn on GitHub Pages

In the repository:

**Settings → Pages → Build and deployment → Deploy from a branch**

Choose:

- Branch: `main`
- Folder: `/ (root)`

Save.

### 4. Custom domain

The included `CNAME` file specifies:

`lumanomy.com`

In GitHub Pages settings, set the custom domain to `lumanomy.com` and enable **Enforce HTTPS** once GitHub makes that option available.

### 5. Point GoDaddy DNS to GitHub Pages

At GoDaddy DNS management for `lumanomy.com`, use GitHub's current published Pages DNS values. For the apex domain, GitHub normally uses A records; for `www`, use a CNAME pointing to your GitHub Pages host (`YOUR-GITHUB-USERNAME.github.io`).

Because GitHub can change or expand its documented DNS values, verify the current values in GitHub's official "Managing a custom domain for your GitHub Pages site" documentation when you configure DNS.

### 6. Optional www redirect

Configure `www.lumanomy.com` as well so visitors reach the site with or without `www`. GitHub Pages can normally redirect between the apex and `www` when both DNS records are configured correctly.

## Design implementation note

This first release intentionally preserves the approved visual exactly by using the final composition as the rendered page artwork, with responsive scaling and an HTML interaction/accessibility layer above it. This gives maximum visual fidelity for launch.

A future version can rebuild the same design as fully native HTML/CSS elements while preserving the visual language, which would improve flexible content editing and mobile reflow.
