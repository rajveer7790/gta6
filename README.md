# VICEWIRE — GTA 6 and Gaming Guides

VICEWIRE is a fast, static gaming editorial website covering GTA 6, Fortnite, Minecraft, Roblox, ARC Raiders, and Counter-Strike 2.

**Live site:** https://gta6downloadfree.com
**Hosting:** Existing Cloudflare Pages project `vicewire`.

## Build and test

```bash
python -m pip install -r requirements.txt
python scripts/build_multigame.py
python scripts/qa_v4.py
```

Published files are generated under `dist/`. The complete source tree includes `data/`, `scripts/`, `source-art/`, `source-css/`, and `dist/`.

## GitHub Actions

The workflow at `.github/workflows/vicewire.yml` will build and validate on every source push to `main`. A validated website artifact will be saved for download. To automatically deploy to the **existing** Cloudflare Pages project, configure GitHub repository Actions secrets `CLOUDFLARE_API_TOKEN` (Pages Write) and `CLOUDFLARE_ACCOUNT_ID` in Settings → Secrets and variables → Actions.

Without both secrets the workflow builds and tests but does **not** publish to Cloudflare. Preserve existing Cloudflare DNS and custom domain settings.

Original editorial illustrations are not official gameplay screenshots. The site is independent and unaffiliated with publishers and game studios.
