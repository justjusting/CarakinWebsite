# CarakinWebsite

Public marketing and legal pages for [carakin.com](https://carakin.com), served via GitHub Pages from this repository.

## Pages

- `/` — landing page
- `/privacy.html` — Privacy Policy
- `/terms.html` — Terms of Service
- `/data-policy.html` — Data Policy

## GitHub Pages setup

1. Open [CarakinWebsite settings → Pages](https://github.com/justjusting/CarakinWebsite/settings/pages).
2. **Source:** Deploy from branch `main`, folder `/ (root)`.
3. Save. The site will publish at `https://justjusting.github.io/CarakinWebsite/` first, then at `https://carakin.com` after DNS is configured.

## Namecheap DNS for carakin.com

In Namecheap → Domain List → **carakin.com** → **Advanced DNS**:

### Apex domain (`carakin.com`)

Add four **A Record** host `@` entries (TTL Automatic):

| Type | Host | Value |
|------|------|-------|
| A Record | `@` | `185.199.108.153` |
| A Record | `@` | `185.199.109.153` |
| A Record | `@` | `185.199.110.153` |
| A Record | `@` | `185.199.111.153` |

### Optional `www`

Add a **CNAME Record**:

| Type | Host | Value |
|------|------|-------|
| CNAME Record | `www` | `justjusting.github.io` |

Remove any conflicting parking-page A records or URL redirect records for `@` or `www`.

### GitHub custom domain

After DNS is saved, in the same GitHub Pages settings, set **Custom domain** to `carakin.com` and enable **Enforce HTTPS** once the certificate is issued (can take up to 24 hours).

The `CNAME` file in this repo tells GitHub Pages to serve the apex domain.

## Contact

`support@carakin.com` (configure this mailbox in Namecheap email forwarding or your provider).
