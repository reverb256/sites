# sites.reverb256.dev — content source

This repo is the **content source** for the site-agency publishing surface.

It is served from the homelab k3s cluster by [reverb256/sites-k8s](https://github.com/reverb256/sites-k8s)
(ArgoCD + Helm; nginx + git-sync sidecar, synced every 60s) behind the Cloudflare tunnel.

- `/<slug>/` — a business's published site (public only after that business consents)
- `/preview/<token>/` — private, token-gated preview (noindex) sent to the business for review

The [site-agency](https://github.com/reverb256/site-agency) pipeline pushes here; git-sync pulls
content into the serving pod — no redeploy needed.

GitHub Pages for this repo was retired 2026-09-22 (serving moved to k3s).
