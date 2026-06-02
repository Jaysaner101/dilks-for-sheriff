# Dilks For Sheriff 2028 — Campaign Website

Static site. No build step, no framework — just HTML/CSS/a little JS.
Works on any host (Vercel, Netlify, GitHub Pages).

## What's in here

```
/
├─ index.html      Home (hero, why I'm running, get involved, contact form)
├─ about.html      About (full statement, credentials, photo)
├─ donate.html     Donate (amount tiles + slot for the donation processor)
├─ 404.html        Branded "page not found"
├─ images/
│   ├─ logo.png    ← YOU ADD THIS  (campaign logo)
│   └─ dilks.jpg   ← YOU ADD THIS  (photo of Michael)
└─ README.md       this file
```

---

## STEP 1 — Add the two images
See `images/README.txt`. Save the logo as `images/logo.png` and the photo as
`images/dilks.jpg`. Until you do, only those two images show broken; nothing else
is affected.

## STEP 2 — Put the files on GitHub
1. Repo already created: `Jaysaner101/dilks-for-sheriff`.
2. On the repo page → "Add file" → "Upload files" (or press `.` for github.dev).
3. Drag in `index.html`, `about.html`, `donate.html`, `404.html`, and the whole
   `images` folder (with your two images inside).
4. Commit changes.

## STEP 3 — Deploy on Vercel
1. vercel.com → Add New → Project → import `dilks-for-sheriff`.
2. Framework Preset: **Other**. Leave build/output blank (it's static).
3. Deploy → live at `dilks-for-sheriff.vercel.app` in ~20s. Every commit auto-redeploys.

## STEP 4 — Connect the domain (dilksforsheriff.com)
Registered at Squarespace — no transfer needed.
1. Vercel → project → Settings → Domains → add `dilksforsheriff.com`.
2. Vercel shows the DNS records.
3. Squarespace → Settings → Domains → your domain → DNS Settings → add those records.
4. Wait for it to verify.

## STEP 5 — Turn on the contact form (Formspree, free)
The contact form on the Home page is wired and just needs an endpoint:
1. Go to **formspree.io** → sign up free → create a new form, send notifications to
   **dilksforsheriff@gmail.com**.
2. Formspree gives you a form ID like `xqyzabcd`.
3. In `index.html`, find `YOUR_FORM_ID` (one place, near the contact form) and replace
   it with your ID. Done — submissions now email the campaign inbox.

## STEP 6 — Turn on donations (once the committee is registered)
1. Set up the committee account on **Anedot** or **WinRed** (committee name + EIN +
   committee bank account; file Florida Form DS-DE 9 first).
2. Copy your donation page's **Embed** code from that platform.
3. In `donate.html`, find the comment `DONATION PROCESSOR EMBED` and replace the
   `<div class="embed-box">...</div>` beneath it with the pasted embed.

Anedot/WinRed automatically collect the legally required donor info (name, address,
occupation, employer) and enforce Florida's $1,000-per-election limit.

---

## Already built in
- Social-share meta tags (Open Graph / Twitter) so the link previews nicely on
  Facebook, Instagram, and text. The preview image points at
  `https://dilksforsheriff.com/images/dilks.jpg` — works once the domain is live.
- Favicon (your logo in the browser tab).
- Mobile-responsive, with load + scroll animations.

## Later / optional
- **Newsletter:** create a free MailerLite or Kit account, grab the embed form, and it
  can drop into the footer. (Send me the form and I'll wire it.)
- **Yard-sign requests:** can be its own form or folded into the contact form.

## Editing notes
- Each page is self-contained (its own CSS). Colors live in the `:root { ... }` block
  near the top of each file (`--gold`, `--pink`). For bigger changes, ask for fresh
  full-file replacements.
