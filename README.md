# speakerblueprints.com

Single-screen landing page for **The Speaker Blueprints™** quiz (Big Impact HQ).
Plain HTML/CSS, no build step. The page sends visitors to the Interact quiz; the
Kartra tagging and email sequences run on the quiz/Kartra side and are not touched here.

## What must not change
- The quiz link on the button (`quiz.tryinteract.com/?kuid=…&kref=…#/…`). Keep it byte-for-byte.
- The Kartra page-tracking block and scripts, and the Facebook Pixel (`1594130054158449`).

## Run locally
    python3 -m http.server 8765

## Deploy
Render static site, publish path `.`, auto-deploy on push to `main` (see `render.yaml`).
Custom domain: add `speakerblueprints.com` and `www.speakerblueprints.com` on the Render
service, then point DNS at Render (see Render's Custom Domains panel for the exact records).
