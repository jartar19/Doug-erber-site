# Douglas Erber — Master Build Plan

Version 1 · November 22, 2026 · Prepared by Jared Tarabocchia, built with Claude

---

## Part 1 — Creative brief

### 1. Website overview

| | |
|---|---|
| **Name** | Douglas Erber |
| **Type** | Personal brand / executive portfolio |
| **Who it's for** | Nonprofit boards, search committees and recruiters hiring an executive director or senior staff leader |
| **What it must do** | Make a board want to call Doug within 60 seconds of landing |
| **Main CTA** | Email Doug (dougerber@hotmail.com, from his resume; swap for a domain address once the domain is live) |
| **Second CTA** | LinkedIn: linkedin.com/in/douglaserber |
| **Location** | Long Beach, California; open to roles in Los Angeles and Long Beach |
| **Hosting** | Static site on Vercel (Hobby), code in a private GitHub repo, domain bought on Cloudflare in Doug's name |

### 2. Core positioning

**One line:** Doug runs the parts of a nonprofit that keep it standing: the donors, the members, the board and the paperwork.

**Why it works for a board:** boards hiring an ED fear three things: money drying up, a board that drifts, and compliance trouble. Doug's record answers all three with numbers, plus a statewide credential (ICC Vice-Chair since 2014, governor appointed) that a search committee can verify.

**Proof points (from the resume, no invention):**
- $3M+ raised through JASSC galas and golf tournaments
- $1.5M Japan relief and recovery fund after the 2011 earthquake and tsunami
- 90% member renewal rate against a typical 80% goal
- 14 years running a 100% board-giving campaign
- $250K centennial gift from one family
- $130K unrestricted grants for IDA in two years, more than its annual net revenue
- First-ever executive director, twice
- Vice-Chair, California State Interagency Coordinating Council on Early Intervention, 2014 to today

**Mission line:** *Draft, to be confirmed by Doug:* "Every community organization deserves a leader who keeps the lights on and the mission moving."

### 3. Brand personality

Steady, credible, quietly impressive. A senior leader, not a motivational speaker. Copy is first person, dry, short sentences, a few well-chosen words. No jargon a board member would have to decode.

| Is | Is not |
|---|---|
| Confident | Boastful |
| Warm | Folksy |
| Precise | Corporate |
| Cinematic | Flashy |

### 4. Visual direction

Option A ("Light"), chosen by Jared on November 22, 2026. Modeled on desses.co: a light studio-grey page framing a dark, glowing night hero. Ramp-style number-forward stat tiles. Sticky left column with cards on the right.

The hero is a real moment: Doug at the Japan America Society podium on the field at Dodger Stadium, turned into a slow cinematic camera orbit that plays as the visitor scrolls.

---

## Part 2 — Cinematic assets

### 5. Higgsfield asset generation

| | Plan | Status |
|---|---|---|
| Model | Seedance 2.x at 1080p, 8 to 12 s | Seedance needs Higgsfield Plus. Shot 1 (live) is a Kling 3.0 standard drone pull-back, 1108×828, 10 s, silent, reversed so the scroll flies in to Doug |
| Identity reference | Studio headshot (`doug-photos/headshot.jpg`) on every generation | Kling takes a start frame only. Re-run on Seedance with the headshot as identity reference when Plus is active |
| Source photos | `doug-photos/dodger-stadium-speech.jpg`, `gala-speech.jpg`, `headshot.jpg` | Uploaded to Higgsfield |
| Delivery | MP4 in `/assets`, re-encoded for scrubbing: H.264, keyframe every frame, no audio, native width (1108 px), under 10 MB, `faststart` | Done: `assets/hero-orbit.mp4`, 7.4 MB, 241 frames. Poster is its first frame |

**Rule:** AI may move the camera around a real moment. It must not invent crowds, events, logos or people. Every scene starts from a real photo of Doug.

### 6. Three cinematic scenes (three separate shots)

1. **Hero fly-in, "The Field" (done, live).** Opens on all of Dodger Stadium at golden hour with downtown LA on the horizon and a seated audience on the field. As the visitor scrolls, the camera descends and orbits in until it lands on Doug at the Japan America Society podium, matching the real photo. Generated as a pull-back from the photo, then reversed. Scrubbed by scroll in the hero.
2. **"The Centennial" (proposed).** From `gala-speech.jpg`: Doug at the "Centennial of Promise, 100 Years" podium. A slow push-in from the back of the ballroom to a medium close-up as stage light warms. For the Story section.
3. **"The Portrait" (proposed).** From `headshot.jpg`: a subtle parallax portrait, slight head turn and a soft smile, studio backdrop. For the final CTA, so the last thing a board sees is Doug looking at them.

---

## Part 3 — Website structure

### 7. Page order

1. **Hero:** full-bleed night stage with the orbit video, name, one-line title, organization marquee.
2. **Animated stats strip:** four tiles count up when they scroll into view.
3. **Mission statement:** big type, one paragraph.
4. **Three pillars** (currently four services; keep four until Doug picks): Fundraising · Membership growth · Governance and compliance · Partnerships and government.
5. **ICC band:** the 2014–today credential, with board roles.
6. **Story:** short career arc in Doug's words. *Draft from the resume; Doug to edit.*
7. **Selected results:** three case cards ($1.5M, $250K, $130K).
8. **Testimonials:** two quotes from coworkers. *Placeholder until Jared collects them.*
9. **Featured writing (phase 2):** home for LinkedIn posts or a Substack if Doug agrees.
10. **Final CTA:** "Hiring your next executive director?" with Email Doug and LinkedIn.
11. **Footer:** name, city, year.

### 8. Section notes

- **Hero:** video pinned while the visitor scrolls one screen; the camera orbit plays forward with the scroll and back when scrolling up. Text stays readable over a dark gradient.
- **Stats:** numbers count from 0 over about 1.4 s, ease-out, once. Prefix and suffix (`$`, `M+`, `%`, ` yrs`) stay fixed while the digits move.
- **Mission:** one sentence; the second half is greyed to create rhythm.
- **Story:** four beats, one line each, no invented detail.
- **Final CTA:** the email button is the primary action on the page and appears in the nav as well.

---

## Part 4 — Style guide

### 9. Color

| Token | Hex | Use |
|---|---|---|
| `--a-bg` | `#F4F4F6` | Page |
| `--a-card` | `#E6E7EC` | Cards |
| `--a-ink` | `#141519` | Text |
| `--a-mute` | `#6E7079` | Secondary text |
| `--a-accent` | `#4A4DF5` | Accent, buttons, tags |
| `--a-night` | `#07081A` | Hero, ICC seal, footer |

### 10. Typography

Inter Tight (Google Fonts), weights 400/500/600. Headlines 500 with tight tracking (−0.03 to −0.05 em). Hero name up to 92 px; footer headline up to 100 px. Numbers use tabular figures.

### 11. Animation direction

Calm and expensive: long ease-out curves, nothing bouncy. Section text rises 24 px and fades in. Marquee drifts at 40 s per loop. Glow blobs drift slowly. A faint film grain sits over the whole page at about 5% opacity.

### 12. Interaction design

Pill buttons with an accent circle arrow. Sticky left columns on desktop. Case index links jump to their cards. All motion respects `prefers-reduced-motion` (no smooth scroll, no scrubbing, numbers shown final).

### 13. Scroll behavior

Lenis smooth scrolling, wired into GSAP ScrollTrigger. ScrollTrigger pins the hero for one screen and maps scroll progress to `video.currentTime`. Reveal animations trigger at 85% of the viewport.

### 14. Mobile behavior

Single column under 860 px. Hero stays full-bleed; scrubbing still works on iOS (muted, `playsinline`, video preloaded). Stats become a 2×2 grid. 16 px side gutters, no horizontal scroll.

---

## Part 5 — Technical implementation (instructions for Claude Code)

### 15. Stack

- One file: `index.html` (inline CSS and JS; Jared chose one file over splitting into style.css and script.js).
- `/assets` holds media: `hero-orbit.mp4`, `hero-poster.jpg`, later scene videos.
- CDN, pinned versions: GSAP 3.12.5 and ScrollTrigger 3.12.5 (cdnjs), Lenis 1.1.13 (unpkg).
- No frameworks, no build step. Vercel serves the folder as-is.

### 16. Repo layout

```
/
├── index.html
├── BUILD-PLAN.md
├── vercel.json        (cache headers for /assets)
└── assets/
    ├── hero-orbit.mp4
    └── hero-poster.jpg
```

### 17. Video encoding

```
ffmpeg -i source.mp4 -an -vf "scale=1280:-2,fps=24" -c:v libx264 -preset slow \
  -crf 24 -g 1 -pix_fmt yuv420p -movflags +faststart assets/hero-orbit.mp4
```

`-g 1` makes every frame a keyframe so scrubbing is smooth in every browser.

### 18. Deploy

**Live now (November 23, 2026):** https://doug-erber-site.vercel.app, Vercel project `doug-erber-site` (framework "Other") on Jared's Hobby account. Deployed directly through the Vercel API. For now `vercel.json` proxies `/assets/hero-orbit.mp4` and `/assets/hero-poster.jpg` to their copies in Jared's Higgsfield library, so the live site does not yet serve the files in `/assets`.

Target setup:
1. Push to the private GitHub repo `jartar19/doug-erber-site` (created; waiting on write access for Claude).
2. In Vercel, connect GitHub and link the repo to the existing `doug-erber-site` project, Framework preset "Other".
3. Every push to `main` redeploys automatically. Once the real files are in `/assets`, the proxy rewrites come out of `vercel.json`.
4. `.vercelignore` keeps this build plan off the public site.

### 19. Domain (Cloudflare)

1. Buy the domain in Cloudflare Registrar under Doug's name and email.
2. In Vercel → Project → Settings → Domains, add `domain.com` and `www.domain.com`.
3. In Cloudflare DNS, add the records Vercel shows (an A record for the root, a CNAME for `www`) and set each to **DNS only** (grey cloud), so Cloudflare's proxy doesn't conflict with Vercel's SSL.

### 20. Open items

- [ ] Doug confirms the mission line and edits the Story section
- [ ] Two coworker testimonials
- [ ] Domain name chosen and bought; email moved to the domain
- [ ] Resume PDF link
- [ ] Higgsfield Plus decision: re-render the hero on Seedance 1080p with the headshot as identity reference, then scenes 2 and 3
- [ ] Featured writing section once the content plan is agreed
