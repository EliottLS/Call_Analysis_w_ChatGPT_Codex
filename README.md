# Resonate — sales call coaching

A responsive, green-themed account executive coaching demo built with React and Vite. This repository is independent of the Territory planning application.

Expected GitHub Pages URL after Pages is enabled and deployment succeeds:
**https://eliottls.github.io/Call_Analysis_w_ChatGPT_Codex/**

## Local development

Requires Node.js 24 (see `.nvmrc`) and npm.

```sh
npm ci
npm run dev
```

## Build and test

```sh
npm run build
npx playwright install chromium
npm test
```

If system Chromium is already installed, use `CHROMIUM_PATH=/usr/bin/chromium npm test`. The four browser tests exercise call review and coaching, transcript uploads, draft exports, and mobile navigation. Playwright starts its own local Vite server on port 4174. To preview the production build, run `npm run preview`.

## Demo features

- **The call:** sample call visual, searchable transcript, session notes, a rule-based copilot, takeaways, and follow-up actions.
- **Coaching:** performance score, sample metrics, BANT / MEDDPPIC / value-selling checklists, strengths, and improvement prompts.
- **Performance:** fictional call history with period, account, and industry filters, chart, and CSV export.
- **Learning:** expandable sales frameworks, YouTube and LinkedIn Learning resource searches, and a downloadable practice reminder.

## Honest demo boundaries

All people, calls, and commercial metrics are fictional. This independent demonstration is not affiliated with LinkedIn, Stripe, Salesforce, or Gong.

Audio and video uploads play locally. TXT, SRT, and VTT uploads replace the transcript and update a clearly labelled keyword-based coaching estimate. The demo does not transcribe recordings or use a live AI model. Recording-only uploads retain sample coaching. Uploads, notes, and chat last for the browser session and are not sent to a backend.

Email actions open a draft in the user's email application. CRM actions download draft JSON. Calendar actions download a proposed ICS event. The demo does not send emails or invitations, or modify CRM records. Production integrations require authenticated services and appropriate consent, privacy, and retention controls.

## Publish to GitHub Pages

1. Open this repository's **Settings → Pages**.
2. Set **Build and deployment → Source** to **GitHub Actions**.
3. In **Actions**, open **Deploy Resonate to GitHub Pages** and run it on `main` if needed.
4. Wait for both the build and deployment jobs to pass. The deployment job supplies the public URL.

Pushes to `main` run a locked dependency install, browser tests, production build, and Pages deployment. Relative asset URLs support the repository's GitHub Pages path.

The original Territory website remains at https://eliottls.github.io/Website_Creation_w_ChatGPT_Codex/ and is maintained in its own repository. The earlier `/resonate/` copy remains there until the new deployment is verified.

## Codex project

Create a dedicated Codex project/environment connected to `EliottLS/Call_Analysis_w_ChatGPT_Codex`. Use `npm ci` for setup, `npm run dev` for development, and the checks above for validation. Each cloud task is already isolated; use its existing checkout and create a worktree only when explicitly requested.
