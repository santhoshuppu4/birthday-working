# Akshithi's Birthday Site — Setup Guide

Everything is in **one file**: `index.html`. You never need to touch the design/animation code — just edit the `CONFIG` block near the bottom of the file (search for `const CONFIG`) and add a few folders of media next to `index.html`.

## 1. Folder structure
Put these folders **next to** `index.html`:
```
index.html
photos/       → her photos for "Growing Up Gorgeous" (1.jpg, 2.jpg, 3.jpg ... up to 32.jpg)
reasons/      → one small photo per reason (1.jpg ... 20.jpg), optional — text still shows if missing
letter/       → letter.jpg (your letter, scanned or exported as an image)
videos/       → wishes.mp4 (friends & family montage), summer.mp4 (your summer recap)
```
If a photo/video isn't there yet, the site shows a soft placeholder instead of a broken image — nothing looks broken while you're still adding content.

## 2. Edit CONFIG (in index.html, near the bottom `<script>`)
- `BIRTHDAY_TARGET_UTC` — already set to Aug 30, 2026, 12:00 AM Qatar time.
- `REUNION_TARGET_UTC` — already set to Sept 22, 2026, 12:00 AM Pacific time. Change the clock time if you meant a different hour.
- `BIRTH_DATE_UTC` — used to calculate "days you've been shining." Set to her actual birth date if Aug 30, 2006 isn't exactly right.
- `PHOTOS` — auto-generates 32 slots (`photos/1.jpg` ... `photos/32.jpg`). Add/remove entries, or add real captions.
- `LETTER_IMAGE` — path to your letter image.
- `REASONS` — edit the `text` for each of the 20 reasons, and point `image` at a photo if you have one for that reason.

## 3. How it flows
1. **Countdown gate** — locked "Not yet…" screen with a live countdown until Aug 30, 12:00 AM Qatar time.
2. **Happy Birthday gate** — appears automatically the moment the countdown hits zero, with the "Start the Surprise" button.
3. **Age reveal** — animates 0 → 20, then counts up to her exact number of days lived.
4. **Growing Up Gorgeous** — scrapbook-style photo grid, alternating rotation and frame styles.
5. **A Letter for You** — tap the envelope, it opens, and your letter image appears full-screen.
6. **20 Reasons** — flip cards one at a time, "Reveal Next," or "Reveal All."
7. **Let's Make Ramen** — 4-step mini interactive activity (cut the packet, microwave, drain, mix), ending in a cozy "watching Lost together" scene.
8. **Wishes From Those Who Love You** — video montage player.
9. **Beautiful Summer With You** — video montage + a live countdown to when you see each other again.

## 4. Sending her the link
This is a static site, so any of these work (all free):
- **Netlify Drop** — go to app.netlify.com/drop, drag the whole folder in, get a link instantly.
- **GitHub Pages** — push the folder to a repo, enable Pages.
- **Vercel** — `vercel deploy` from the folder.

Send her the link 2 days early — the countdown gate keeps the surprise locked until the exact moment.
