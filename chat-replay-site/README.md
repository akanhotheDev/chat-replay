# Chat Replay: deploy guide

This folder is a complete static website. No build step, no server code.

## Fastest: Netlify Drop (about 2 minutes)
1. Go to https://app.netlify.com/drop and sign in (free).
2. Drag this whole folder onto the page. You get a public https link at once.
3. Rename the site in Site settings, or add your own domain under Domain management.

## Alternatives
- GitHub Pages: push these files to a repo, then Settings > Pages > deploy from the main branch.
- Cloudflare Pages / Vercel: create a project from the repo or upload the folder; set no build command and "." as the output folder.

## Installing as an app
Installing needs https (all hosts above provide it). On Android Chrome and desktop Chrome/Edge, an "Install the app" button appears on the start screen. On iPhone, tap Share > Add to Home Screen. After the first visit the app also opens offline.

## Notes
- Chats are processed entirely in the browser; nothing is uploaded.
- The AI summary only works inside Claude. A public site would need a small backend holding an API key, so the Summary button stays hidden here.
- To ship an update, redeploy and change `chat-replay-v1` in sw.js to `chat-replay-v2` so installed copies refresh.
