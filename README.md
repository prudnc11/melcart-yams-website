# Melcart Yams website

Static website for Melcart Yams, a Ghanaian exporter of fresh Puna and white yam. Built with plain HTML, CSS, and JavaScript; no build tools or package installation required.

## Preview locally

From the project folder, run:

```sh
python3 -m http.server 8000
```

Open <http://localhost:8000>. Stop the server with `Ctrl+C`.

You can also open `index.html` directly in a browser. A local server is a better preview for video and other site assets.

## Project files

- `index.html` — page content, styles, and small interactive behaviors
- `images/` — product, warehouse, certification, and hero media assets

There is no build step. Keep `index.html` and `images/` together when deploying.

## Deploy

This site can be hosted as static files on GitHub Pages, Cloudflare Pages, Netlify, or another static host. Free plans and limits can change; check the provider’s current terms.

### Cloudflare Pages

1. Push this repository to GitHub.
2. In Cloudflare, open **Workers & Pages** and create a Pages project connected to the GitHub repository.
3. Set the production branch to `main`.
4. Leave the build command empty. Set the build output directory to `/` (repository root).
5. Deploy. `index.html` at the project root is the site’s entry page.
6. In the Pages project’s **Custom domains** settings, add your domain and follow Cloudflare’s DNS instructions. Root domains require the domain’s nameservers to use Cloudflare; a subdomain can use a CNAME record.

### GitHub Pages

1. In the repository on GitHub, open **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
3. To use a custom domain, enter it in the Pages settings and configure the DNS records at your domain provider using GitHub’s instructions. Enable **Enforce HTTPS** once available.

## Updating the site

Edit `index.html` for page text, styles, links, or interactions. Add or replace media in `images/`, then update the matching asset paths in `index.html`. Commit and push changes to `main`; connected hosting providers will publish the update automatically.

## Contact form

The quote form opens a prefilled email to `info@melcart.co` using the visitor’s default mail app. It does not submit to a server, so visitors need an email app configured to send the message.
