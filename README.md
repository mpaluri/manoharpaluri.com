# manoharpaluri.com

Personal site for Manohar Paluri. Plain static HTML, deployed via GitHub Pages.

## Deploy

1. Push this repo to `github.com/mpaluri/manoharpaluri.com`.
2. GitHub → Settings → Pages → Source: `Deploy from a branch`, Branch: `main`, Folder: `/ (root)`.
3. The `CNAME` file already specifies `manoharpaluri.com`. GitHub Pages picks it up automatically.

## DNS (at your registrar)

Apex (`manoharpaluri.com`) — add four A records pointing to GitHub Pages:

```
A  @  185.199.108.153
A  @  185.199.109.153
A  @  185.199.110.153
A  @  185.199.111.153
```

Also add AAAA records if you want IPv6 (optional):

```
AAAA  @  2606:50c0:8000::153
AAAA  @  2606:50c0:8001::153
AAAA  @  2606:50c0:8002::153
AAAA  @  2606:50c0:8003::153
```

`www` subdomain — CNAME:

```
CNAME  www  mpaluri.github.io
```

## HTTPS

After DNS propagates (usually minutes to a few hours), go to Settings → Pages and check **Enforce HTTPS**. GitHub provisions a free Let's Encrypt cert automatically.

## Files

- `index.html` — the home page
- `CNAME` — tells GitHub Pages which custom domain to serve
