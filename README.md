# Heritage Guide – National Museum of Ras Al Khaimah

Beige, bilingual (EN/AR) museum guide: home page, artefact cards with search and a
"when" timeline, AI guide, quiz, and the original AR walk.

## Deploy on GitHub Pages
1. Create a repo and push these files to `main`.
2. Settings → Pages → Source: **GitHub Actions**.
3. Open `https://<user>.github.io/<repo>/` (HTTPS is required for camera and motion sensors).

## AI guide
GitHub Pages is static, so there is no built-in AI. Without setup, the guide answers by searching
the collection. For real AI answers, host a small proxy that keeps your API key secret, and set its
URL in `config.js` (`window.HERITAGE_AI_ENDPOINT`). Request: `POST {system, messages}` → `{ "text": "..." }`.

## Notes
- Museum text and photos come from the Heritage Hackathon kit (National Museum of RAK panels).
- Gallery date ranges in the timeline are approximate; verify against the panels.
- Data is embedded in `index.html` (`window.__DATA`).
