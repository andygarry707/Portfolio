# Andrey Volkov Portfolio

Local proof-first portfolio for freelance platforms.

The goal is simple: a prospect can open one link, inspect live work, understand the offer,
and continue the conversation with better questions. This is not positioned as a loud
"replacement for reviews"; it is a proof-of-work portfolio for new Upwork/Fiverr profiles.

## Local Entry Points

- `index.html` (root) - redirects to the brand site so the bare domain never 404s.
- `brand-site/index.html` - main portfolio page, EN/DE toggle, portfolio assistant, placeholders.
- `demos/dubai-real-estate/index.html` - Demo #1: NUR luxury Dubai real estate.
- `demos/clinic-de/index.html` - Demo #2: German-first dental clinic.
- `demos/solar-de/index.html` - Demo #3: German-first solar / photovoltaics.
- `demos/saas/index.html` - Demo #4: B2B SaaS product page.
- `demos/restaurant/index.html` - Demo #5: fine dining restaurant.
- `LAUNCH-INPUTS.md` - all personal data, links, assets, and launch decisions to fill.

Open `brand-site/index.html` directly in a browser, or use Playwright/browser tooling for
screenshots. No build step is required.

## Current Status

Done locally:

- Portfolio-first brand page v2, with web fonts restored (Space Grotesk / Inter / IBM Plex Mono).
- Five local demo pages. The four secondary demos were rebuilt, each with its own visual identity
  (typography, palette, layout, and a signature element) so the "five different designs" claim holds.
- AI/chatbot demo flow on the brand page and every demo page.
- German-first demos and the brand-site DE dictionary corrected to proper umlauts (ä/ö/ü/ß).
- Accessibility pass (skip links, focus-visible, aria-labels, reduced-motion) and favicons on every page.
- Local-only lead forms with required-field validation.
- Desktop + mobile QA via Playwright: 0 console errors, correct web fonts, no horizontal overflow.
- Placeholder map for profile photo, bio, platform links, GitHub, domain, contact data.

Still required before public launch:

- Replace portrait placeholder with a real photo or intentional avatar.
- Fill `PROFILE` in `brand-site/index.html`.
- Decide final platform-safe CTA wording for Upwork/Fiverr.
- Review or replace `brand-site/og.png` with a final production social preview.
- Connect forms/chat lead capture to a webhook/backend, or remove form capture until backend exists.
- Run final desktop/mobile visual QA.
- Deploy to domain/VPS and test live.

Explicitly postponed:

- VPS/Caddy/Cloudflare deployment.
- Production LLM chatbot backend.
- Analytics and CRM automation.
- Upwork/Fiverr/Telegram/GitHub copy kits.

## Positioning

Primary positioning:

> AI conversion sites and chatbots for service businesses, SaaS, and local lead generation.

Portfolio behavior:

- Show work before claims.
- Keep copy scannable.
- Use demos as the main proof layer.
- Route platform prospects back to the platform for ordering/conversation.
- Use direct Telegram/email only where it is appropriate outside platform rules.

## Verification Notes

Use `npm.cmd`, not `npm`, in PowerShell if script execution policy blocks `npm.ps1`.

Playwright browser binaries were installed locally with:

```powershell
npm.cmd exec --yes playwright@latest -- install chromium
```

Useful checks:

```powershell
npm.cmd exec --yes playwright@latest -- screenshot --viewport-size=1440,1100 "file:///C:/Users/andrvolf/portfolio/brand-site/index.html" ".codex-research/brand-v2-desktop.png"
npm.cmd exec --yes playwright@latest -- screenshot --viewport-size=390,1000 "file:///C:/Users/andrvolf/portfolio/brand-site/index.html" ".codex-research/brand-v2-mobile.png"
```
