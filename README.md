# Lucar Technologies Inc. website

A responsive, single-page corporate website built with plain HTML, CSS and JavaScript for GitHub Pages. No build tools or paid hosting are required.

## Before publishing

1. Open `index.html` and replace `REPLACE_WITH_YOUR_BUSINESS_EMAIL` in the contact button with the real corporate email address (for example, `info@your-domain.ca`). Do not publish the placeholder.
2. Confirm that every service description accurately reflects services the company currently offers or intends to offer. Adjust wording as needed.
3. Confirm the company name, tagline and logo. The supplied logo image is in `assets/lucar-logo.png`.
4. Optional: update the SEO description and page title in the `<head>` section of `index.html`.

## Test locally

Open `index.html` in a browser. For a local web server, from this folder run:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Publish with GitHub Pages

1. Create a GitHub repository named `lucar-website` (public repository for GitHub Free Pages).
2. Upload `index.html`, `styles.css`, `script.js`, `README.md` and the `assets` folder to the repository root. Keep the folder structure intact.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Wait for the Pages deployment to finish. The initial address will look like `https://YOUR-USERNAME.github.io/lucar-website/`.

## Connect lucartechnologies.ca later

Only do this after registering and controlling the domain.

1. In **Settings → Pages → Custom domain**, enter `lucartechnologies.ca` and save.
2. At the domain registrar, configure the apex (`@`) A records to GitHub Pages' current published IP addresses. Verify the current values in GitHub's official documentation rather than relying on an old copied list.
3. Add a `www` CNAME pointing to `YOUR-USERNAME.github.io` (replace with your actual GitHub username).
4. Wait for DNS propagation and certificate provisioning, then enable **Enforce HTTPS** in GitHub Pages settings.
5. Revisit the site using both the apex and `www` domain and confirm they resolve securely.

Official instructions: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## Important notes

- GitHub Pages is static hosting. The email button opens the visitor's email application; it does not store or process form submissions.
- Do not collect confidential, classified, personal or sensitive client information through an ordinary website form.
- The site currently makes no claims of security certification, clearance, government endorsement or authorization.
- Google Fonts are loaded from Google's CDN. The rest of the site assets are local. If you prefer no third-party font request, remove the `@import` line at the top of `styles.css` and the page will use system fallbacks.
