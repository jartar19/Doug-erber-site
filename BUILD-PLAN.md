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

**One line (Doug's own, November 2026):** "For more than 30 years, I've helped nonprofit organizations thrive through effective fundraising, donor and member relations, board engagement, strategic leadership, and sound financial and operational management."

**Why it works for a board:** boards hiring an ED fear three things: money drying up, a board that drifts, and compliance trouble. Doug's record answers all three with numbers, plus a statewide credential (appointed to the ICC by Governor Jerry Brown in 2014, elected Vice Chair in 2019) that a search committee can verify.

**Proof points (confirmed by Doug in the questions doc, November 2026):**
- $3M+ raised through JASSC fundraising galas and golf tournaments
- $1.5M relief and recovery fund after Japan's 2011 earthquake, tsunami and nuclear disaster
- 90% member renewal rate against a typical 80% goal
- 14 years running a 100% board-giving campaign
- $250,000 gift from one family for the JASSC Centennial Celebration
- $130,000 in unrestricted donations and grants for IDA over two years, more than its annual net revenue
- 25% membership growth and 90% renewals, backed by a $150,000 three-year capacity grant (Japan Foundation CGP)
- Largest annual budget: $623,000 at JASSC (2010)
- First-ever executive director, twice: IDA (2021 to 2024) and Sister Cities of Long Beach (2025 to 2026)
- California State Interagency Coordinating Council on Early Intervention: appointed 2014, Vice Chair since 2019
- Board President, Autism Partnership Foundation, 2012 to present

**Availability line (Doug's words):** "Open to considering nonprofit board service opportunities aligned with my experience and interests."

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
| Delivery | MP4 in `/assets`, re-encoded for scrubbing: H.264, keyframe every frame, no audio, native width (1108 px), under 10 MB, `faststart` | Done: `assets/hero-orbit.mp4`, 241 frames. Re-encoded Nov 23 with a keyframe every 6 frames (3.9 MB, down from 7.4 MB, no visible change). Poster is its first frame |

**Rule:** AI may move the camera around a real moment. It must not invent crowds, events, logos or people. Every scene starts from a real photo of Doug.

### 6. Three cinematic scenes (three separate shots)

1. **Hero fly-in, "The Field" (done, live).** Opens on all of Dodger Stadium at golden hour with downtown LA on the horizon and a seated audience on the field. As the visitor scrolls, the camera descends and orbits in until it lands on Doug at the Japan America Society podium, matching the real photo. Generated as a pull-back from the photo, then reversed. Scrubbed by scroll in the hero. The name gets clearer as the camera flies in: it starts at 60% strength, and a dark scrim builds in the lower-left corner behind it, so by the time the camera reaches Doug the name is solid white and fully readable. Over the second half of the flight the frame pans so Doug lands dead center (phones slide the crop; wide screens zoom about 10%), and the last 6% of the scroll dissolves into the full-resolution podium photo (`assets/hero-end.jpg`, the original 1536 px shot the clip was generated from), because the video's own last frame is soft.
2. **"The Centennial" (proposed).** From `gala-speech.jpg`: Doug at the "Centennial of Promise, 100 Years" podium. A slow push-in from the back of the ballroom to a medium close-up as stage light warms. For the Story section.
3. **"The Portrait" (proposed).** From `headshot.jpg`: a subtle parallax portrait, slight head turn and a soft smile, studio backdrop. For the final CTA, so the last thing a board sees is Doug looking at them.

---

## Part 3 — Website structure

### 7. Page order

Reworked November 23, 2026 so the page reads as a pitch to a board, not a resume. The hero is unchanged; everything below it leads with what Doug solves, then the proof, then the chronology.

1. **Hero:** full-bleed night stage with the orbit video, name, one-line title, organization marquee.
2. **Mission statement:** Doug's own sentence in the display serif, lighting up word by word, with his availability line under it.
3. **Animated stats strip:** four tiles count up when they scroll into view.
4. **Where I help (`#work`):** "If one of these sounds like your board, let's talk." Five situations a board recognizes, each written as the board would say it, with Doug's answer from his own record and a proof chip. Ends with the main call to action, "Tell me what you're facing" (opens an email).
5. **Selected results:** Doug's three picks ($1.5M relief fund, $250K Centennial gift with the gala photo, +25% membership with a 90% renewal ring).
6. **ICC band:** Vice Chair since 2019, appointed 2014, with three fact chips. The other boards moved to the Experience timeline.
7. **How I work (`#how`):** four principles, each tied to something he has done (bylaws, the Centennial gift, 14 years of 100% board giving, ICC Vice Chair).
8. **Story:** Doug's own four-beat career arc with his studio headshot.
9. **Experience:** a career timeline (staff roles and board seats as bars from 1989 to now), then "Role by role" details behind a button, and the Education card.
10. **Testimonials:** *section built but hidden until Doug's references send quotes.*
11. **Featured writing (phase 2):** home for LinkedIn posts or a Substack if Doug agrees.
12. **Final CTA:** "Let's connect." with a line on who should write and why, Email Doug, Copy email and LinkedIn buttons, and five topic links that open an email with the subject filled in (executive director search, board seat, fundraising or membership, governance and compliance, hello).
13. **Footer:** name, city, email link, year.

### 8. Section notes

- **Hero:** video pinned while the visitor scrolls one screen; the camera orbit plays forward with the scroll and back when scrolling up. Text stays readable over a dark gradient.
- **Stats:** numbers count from 0 over about 1.4 s, ease-out, once. Prefix and suffix (`$`, `M+`, `%`, ` yrs`) stay fixed while the digits move.
- **Mission:** one sentence; the second half is greyed to create rhythm.
- **Story:** four beats in Doug's words; the left column (title and headshot) stays pinned while the beats scroll.
- **Final CTA:** the email button is the primary action on the page and appears in the nav as well.

---

## Part 4 — Style guide

### 9. Color

Forest green (Jared, November 23, 2026), replacing the original purple.

| Token | Hex | Use |
|---|---|---|
| `--a-bg` | `#F4F5F2` | Page |
| `--a-card` | `#E6E9E3` | Cards |
| `--a-ink` | `#131714` | Text |
| `--a-mute` | `#6A7069` | Secondary text |
| `--a-accent` | `#2D6A4F` | Accent, buttons, tags, stat bars |
| `--a-accent-hi` | `#3E8E68` | Hover and active states |
| `--a-accent-soft` | `#95D5B2` | Accent on dark backgrounds |
| `--a-night` | `#06140D` | Hero, ICC seal, footer |

Glows on dark panels use `#1B5E3B`, `#2D8A57` and `#52B788`.

### 10. Typography

Two faces, both self-hosted in `assets/fonts`.

- **Fraunces** (variable, optical size and weight axes, roman and italic) for display: section headings, the mission line, stat numbers, result figures, the ICC seal, problem quotes and card titles. Weight 330 to 400 at optical size 144, tracking about −0.02 em. One or two words in each heading are set in italic accent green (mint on dark panels).
- **Inter Tight** 400/500/600 for body text, labels, buttons and navigation. The hero name stays in Inter Tight.
- Scale: section headings 36 to 66 px, footer headline up to 136 px, lead paragraphs 17 to 20 px, body 15 to 17 px, labels 12 px uppercase with wide tracking and a short rule.

### 11. Animation direction

Calm and expensive: long ease-out curves, nothing bouncy. Section text rises 24 px and fades in. Section headings rise in word by word. The headshot opens from a smaller frame and drifts slightly with the scroll; the gala photo settles in the same way. A green rule draws under each story beat as it arrives. Marquee drifts at 40 s per loop and pauses on hover. Glow blobs drift slowly. A faint film grain sits over the whole page at about 5% opacity.

### 12. Interaction design

Pill buttons in four variants (primary green, light, ghost on dark, outline), each with an icon chip. On hover a fill sweeps up from the bottom and the icon slides out and back in; on press the button scales to 97%; focus shows a ring. Copy email swaps to a check mark when it works. All icons are hand-drawn SVG symbols in one sprite at the top of the body. Sticky left columns on desktop. A floating pill nav (How I help, Results, ICC, Story, Experience, Contact) slides in after the hero and highlights the section you're in. Case index links jump to their cards and highlight while their card is on screen. Cards, stat tiles and role rows lift or brighten on hover; the green glow on the result cards follows the pointer. All motion respects `prefers-reduced-motion` (no smooth scroll, no scrubbing, numbers shown final).

### 13. Scroll behavior

Lenis smooth scrolling, wired into GSAP ScrollTrigger. ScrollTrigger pins the hero for one screen and maps scroll progress to `video.currentTime`. Reveal animations trigger at 85% of the viewport.

### 14. Mobile behavior

Single column under 860 px. Hero stays full-bleed; scrubbing still works on iOS (muted, `playsinline`, video preloaded). Stats become a 2×2 grid. 16 px side gutters, no horizontal scroll.

---

## Part 5 — Technical implementation (instructions for Claude Code)

### 15. Stack

- One file: `index.html` (inline CSS and JS; Jared chose one file over splitting into style.css and script.js).
- `/assets` holds media, fonts and scripts.
- Self-hosted since Nov 23 (no third-party requests): GSAP 3.12.5, ScrollTrigger 3.12.5 and Lenis 1.1.13 in `assets/js/`, Inter Tight 400/500/600 (latin woff2) in `assets/fonts/`.
- The hero video loads after the page's load event, so the photo, text and fonts come first. Visitors with Data Saver on keep the still photo.
- No frameworks, no build step. Vercel serves the folder as-is.

### 16. Repo layout

```
/
├── index.html
├── BUILD-PLAN.md
├── 404.html           (branded not-found page)
├── robots.txt, sitemap.xml
├── favicon.ico, apple-touch-icon.png
├── vercel.json        (cache and security headers)
└── assets/
    ├── js/                (gsap, ScrollTrigger, lenis)
    ├── fonts/             (Inter Tight and Fraunces woff2)
    ├── share.jpg          (1200x630 link-preview card for LinkedIn, iMessage, email)
    ├── favicon-32.png, icon-512.png
    ├── hero-orbit.mp4
    ├── hero-poster.webp   (.jpg kept as a fallback copy)
    ├── hero-end.webp      (full-res final frame of the hero; .jpg kept)
    ├── headshot.jpg       (story section)
    ├── headshot-face.jpg  (footer signature)
    └── gala-speech.jpg    (Centennial result card)
```

### 17. Video encoding

```
ffmpeg -i source.mp4 -an -c:v libx264 -preset veryslow -tune film \
  -crf 25 -g 6 -bf 0 -pix_fmt yuv420p -movflags +faststart assets/hero-orbit.mp4
```

A keyframe every 6 frames (a quarter second) with no B-frames keeps scrubbing smooth while roughly halving the file versus every-frame keyframes.

### 18. Deploy

**Live (November 23, 2026):** https://doug-erber-site.vercel.app, Vercel project `doug-erber-site` (framework "Other", no build step) on Jared's Hobby account, built from the private GitHub repo `jartar19/doug-erber-site`.

1. Edit files and push to `main`.
2. Vercel redeploys production automatically on every push to `main`.
3. Media lives in `/assets` and is served by Vercel directly, cached for 7 days. **When replacing an asset, give it a new filename** (for example `headshot-2.jpg`) and update the reference, or returning visitors may see the old file for up to a week.
4. `.vercelignore` keeps this build plan and the README off the public site.

### 19. Domain (Cloudflare)

1. Buy the domain in Cloudflare Registrar under Doug's name and email.
2. In Vercel → Project → Settings → Domains, add `domain.com` and `www.domain.com`.
3. In Cloudflare DNS, add the records Vercel shows (an A record for the root, a CNAME for `www`) and set each to **DNS only** (grey cloud), so Cloudflare's proxy doesn't conflict with Vercel's SSL.
4. Then swap `https://doug-erber-site.vercel.app` for the new domain in `index.html` (canonical, og:url, og:image, JSON-LD), `robots.txt` and `sitemap.xml`.

### 20. Open items

- [x] Doug confirms the mission line and edits the Story section
- [ ] Doug reviews the new pitch copy (Where I help, How I work, the footer line). It is built only from his own facts, but the framing is new
- [ ] Two or three testimonials (names, titles, quotes, permission)
- [ ] Buy dougerber.com on Cloudflare in Doug's name (no backup picked yet). Email stays dougerber@hotmail.com; no phone number on the site
- [ ] Gated resume download: Doug wants it only behind a full contact form that requires a working business email domain. Needs his resume PDF and a form backend
- [ ] Doug's in-person notes on anything to change or leave off
- [ ] Higgsfield Plus decision: re-render the hero on Seedance 1080p with the headshot as identity reference, then scenes 2 and 3
- [ ] Featured writing section once the content plan is agreed
- [ ] Confirm Doug's availability line. He wrote "Open to considering nonprofit board service opportunities", but the site's main purpose is an ED or senior staff role
- [ ] Optional: a professional email on the new domain (for example doug@dougerber.com) to replace hotmail on the site
- [ ] Optional: Vercel Web Analytics, to see whether boards and recruiters are visiting
