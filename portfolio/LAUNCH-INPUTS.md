# Launch Inputs Checklist

Fill this before publishing the portfolio or linking it from freelance platforms.

## Personal Identity

- Public name spelling: `Andrey Volkov`
- Photo: replace the `PHOTO PLACEHOLDER` block in `brand-site/index.html`.
- Short bio: real background, years/experience, relevant technical/business strengths.
- Location wording: remote studio / Europe-facing / EN-DE clients.
- Working languages: final wording for English, German, Serbian levels.
- Availability: timezone, working hours, expected response time.
- Delivery policy: preview timeline, revision rounds, refund/satisfaction wording.

## Links

Fill the `PROFILE` object in `brand-site/index.html`:

```js
var PROFILE = {
  upwork:"",
  fiverr:"",
  telegram:"",
  email:"",
  github:"",
  domain:"andreyvolkov.dev",
  photo:""
};
```

Required:

- Upwork profile URL
- Fiverr profile URL and gig URLs
- Telegram handle
- Contact email
- GitHub username and public repos
- Final domain

## Platform-Safe CTA

For Upwork/Fiverr traffic, avoid making direct contact the primary path.

Recommended pattern:

- Primary: `Continue on Upwork` / `Continue on Fiverr`
- Secondary: `View live work`
- Direct Telegram/email: visible only for direct outreach version, or lower priority

Before launch, check current platform rules inside the account UI.

## Assets

- Real portrait or deliberate avatar
- `brand-site/og.png` production social preview
- Optional favicon refinement
- Screenshots/thumbs for platform portfolio items

## Backend Later

Local forms currently do not send anywhere.

Production options:

- simple webhook endpoint on VPS
- Telegram notification
- email notification
- CRM route
- real LLM chatbot backend with server-side API key

## Final QA

- Desktop: 1440px and 1280px
- Mobile: 390px and 360px
- All demo links open
- Chat widgets do not cover essential CTAs
- No horizontal overflow
- Text fits buttons and cards
- OG image exists
- Platform CTA links are filled
