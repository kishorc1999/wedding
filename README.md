# Arjun ❋ Priya — Luxury South Indian Wedding Invitation

A cinematic, single-file wedding invitation website. Deep maroon and temple gold palette, opening temple doors loader, floating jasmine petals, live countdown, WhatsApp RSVP, and a Tamil + English bilingual feel.

**No build step. No backend. Just one file.**

---

## 🚀 Deploy in 2 minutes

### Option A — Vercel (recommended, takes 30 seconds)
1. Go to [vercel.com](https://vercel.com) and sign in with GitHub.
2. Click **"Add New" → "Project" → "Browse / Import"**.
3. Drag the folder containing `index.html` onto the import area (or push it to a GitHub repo first and import that).
4. Click **Deploy**. Done. You get a live URL like `your-wedding.vercel.app`.

### Option B — GitHub Pages
1. Create a new GitHub repo (e.g. `arjun-priya-wedding`).
2. Upload `index.html` to the root.
3. Go to **Settings → Pages**.
4. Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)**, Save.
5. Your site goes live at `https://<your-username>.github.io/<repo-name>/` in ~1 minute.

### Option C — Netlify drag & drop
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag the folder containing `index.html`. Done.

---

## ✏️ Customizing the invitation

Open `index.html` in any editor (VS Code, Notepad++, even Notepad). Everything is clearly commented.

### 1. Names & date (most important)
Find and replace these throughout the file:
- `Arjun` → groom's name
- `Priya` → bride's name
- `26 · April · 2026` → your wedding date
- The first letters `A` and `P` in the bride/groom portrait circles (search for `<!-- Replace with`)

### 2. Wedding date for countdown
In the `<script>` section, find:
```js
const WEDDING_DATE = new Date('2026-04-26T09:30:00+05:30').getTime();
```
Change to your date. Format is `YYYY-MM-DDTHH:MM:SS+05:30` (the `+05:30` is India Standard Time — keep that).

### 3. Parents' names
Search for `Mr. & Mrs. Ramesh Kumar` and `Mr. & Mrs. Venkatesh Iyer` — replace with the actual names.

### 4. Venue
Search for `Sri Krishna Mahal` and the address that follows. Also update the Google Maps iframe `src` URL:
- Open Google Maps, search your venue, click **Share → Embed a map**, copy the `src=...` URL into the iframe.
- Update the **Get Directions** button `href` too.

### 5. WhatsApp RSVP number
Find:
```html
href="https://wa.me/919876543210?text=..."
```
Replace `919876543210` with your number (country code + number, no `+` or spaces). The text after `?text=` is the pre-filled message (URL-encoded — use `%20` for spaces).

### 6. Couple photos (optional but recommended)
1. Place your photos in the same folder as `index.html` (e.g., `groom.jpg`, `bride.jpg`).
2. Find the two `<div class="person-portrait-inner">` blocks.
3. Replace `A` (and `P`) with `<img src="groom.jpg" alt="Arjun">` (and bride likewise).

### 7. Background music
Replace the audio source URL in `<audio id="bgAudio">` with your own nadaswaram/temple-bells MP3 (host it in the same folder and use `src="music.mp3"`).

### 8. Colors
At the very top of the `<style>` section there's a `:root` block with all colors as CSS variables. Tweak `--gold`, `--maroon`, etc. to taste.

### 9. Events
The five event cards (Engagement, Mehendi, Haldi, Kalyanam, Reception) are in the `<section class="events">` block. Edit each card's `.event-date` and `.event-time` text.

---

## 📱 What's included

- **Cinematic loader** — animated temple doors part to reveal the site
- **Floating jasmine petals** — ambient motion throughout
- **Bilingual** — Tamil + English with proper Noto Serif Tamil font
- **Live countdown** — auto-updating to your wedding moment
- **Embedded venue map** — Google Maps with directions button
- **WhatsApp RSVP** — one-tap with pre-filled message
- **Optional background music** — user-controlled toggle
- **Fully responsive** — looks great in WhatsApp browser, Instagram, mobile, desktop
- **Smooth scroll animations** — GSAP + IntersectionObserver
- **Reduced-motion respect** — accessible for sensitive users
- **SEO + Open Graph tags** — pretty WhatsApp share previews

---

## 🎨 Tech notes

- Pure HTML + CSS + vanilla JS. GSAP loaded from CDN.
- Google Fonts: Cinzel, Cormorant Garamond, Tangerine, Noto Serif Tamil.
- No frameworks, no npm, no build tools. Edit and deploy.

---

## 💛 Sharing

After deploying, your URL works perfectly when pasted into WhatsApp — the Open Graph meta tags give you a clean preview card.

May your celebration be blessed.

✦ ❋ ✦
