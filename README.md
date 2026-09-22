# vyrdlabs.com

Static site for Vyrd Labs LLC, served by GitHub Pages from the root of `main`. Plain HTML and one
stylesheet (`assets/site.css`); no build step.

| URL | File | Used by |
|---|---|---|
| `/` | `index.html` | |
| `/daily/` | `daily/index.html` | Play listing website and support |
| `/daily/privacy/` | `daily/privacy/index.html` | Play listing, Data safety, Daily Plus paywall, app Settings |
| `/daily/terms/` | `daily/terms/index.html` | Daily Plus paywall, app Settings |
| `/daily/delete-account/` | `daily/delete-account/index.html` | Play Data safety "delete account" URL |

## Preview locally

```bash
python3 -m http.server 8000
```

## Hosting

GitHub Pages: Settings → Pages → Deploy from branch `main`, folder `/`. The `CNAME` file sets the
custom domain; tick **Enforce HTTPS** once the certificate is issued.

DNS for `vyrdlabs.com` (leave the Google Workspace `MX` and `TXT` records alone):

| Host | Type | Value |
|---|---|---|
| `@` | A | `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` |
| `@` | AAAA | `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153` |
| `www` | CNAME | `mpkasp.github.io` |

Verify the domain under the GitHub account's Settings → Pages to stop other accounts claiming it.
