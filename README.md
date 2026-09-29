# car-site

Static site for `car.shlomowolf.com`, served by GitHub Pages.

Its one job is to host the public key for a personal Tesla Fleet API app at:

```
https://car.shlomowolf.com/.well-known/appspecific/com.tesla.3p.public-key.pem
```

## Rules

- Only the **public** key goes in this repo. `.gitignore` blocks other key files.
- `.nojekyll` must stay. Without it, GitHub Pages skips the `.well-known` folder.
- `CNAME` holds the custom domain.

## DNS

Cloudflare record for `shlomowolf.com`:

| Type | Name | Target | Proxy |
|---|---|---|---|
| CNAME | `car` | `sh-wolf.github.io` | DNS only |

If this site is ever deleted, delete the DNS record too.
