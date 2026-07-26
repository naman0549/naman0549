<div align="center">

![Header](https://img.shields.io/badge/ANIMATED-GITHUB%20PROFILE-87CEEB?style=for-the-badge&labelColor=0C4A6E)

# 🩵 The Complete Step-by-Step Guide

*Build a profile README with a typing terminal, animated name, hologram scanner,*
*swinging ID badge, trophies, and a snake that eats your contributions — using only AI prompts.*

```
user@github:~$ cat how-to-glow-up.md _
```

![Save](https://img.shields.io/badge/⭐-Save%20this%20guide-38BDF8?style=flat-square) ![Share](https://img.shields.io/badge/↗-Share%20with%20a%20coder%20friend-0EA5E9?style=flat-square)

</div>

---

## ✨ What You'll Build

A GitHub profile README that plays like a mini movie the moment someone opens it:

| Feature | Description |
|---|---|
| 🖥️ **Animated banner** | Terminal typing effect, name popping in letter-by-letter with a flowing gradient, cycling role titles, tech pills, stats bar, a self-writing code card, a flickering neon sign |
| 🔷 **Hologram effects** | Your character image materializes top-to-bottom on load, then a scanner line sweeps the banner forever |
| 🪪 **Swinging ID badge** | A lanyard card with pendulum physics, your avatar, a barcode, and a holographic shine |
| 🌗 **Dark + light mode** | Two banner versions that auto-switch with the viewer's GitHub theme |
| 📊 **Local stat cards** | Animated GitHub stats, top languages, and trophies that never show broken-image errors |
| 🐍 **Snake animation** | The classic snake eating your contribution graph, in custom colors |

---

## 🧰 What You Need

- [ ] A GitHub account (free)
- [ ] An AI image generator (ChatGPT / DALL·E / any) — for your character art
- [ ] An AI coding assistant that can generate SVG files (e.g. Claude) — for the animations
- [ ] 15–20 minutes

> **💡 Why SVG?** GitHub strips all JavaScript from READMEs — normal web animations die there. SVG + CSS/SMIL animations are the only thing that plays inside a README, and they run everywhere with zero libraries.

---

## 🪜 Step 1 — Generate Your Character Image

Create an anime-style illustration of yourself. Ask any AI image tool (ChatGPT / DALL·E, etc.) using the prompt below — customize the look, outfit, and books to match you. A **pure white background** is important: it makes background removal clean later.

<details>
<summary>📋 <strong>AI Image Prompt — click to expand & copy</strong></summary>

```
High-quality anime-style digital illustration of a young developer sitting relaxed in a
round rattan chair with a dark laptop on their lap, softly smiling at the viewer.
[Describe yourself: hair, glasses, features]. Sunglasses resting on head, cozy white
zip-up hoodie over a yellow t-shirt, blue jeans. Beside them a glass-top wicker cafe
table holding: a stack of programming books with spines reading "HTML & CSS",
"JavaScript", "React", "SQL", "The Pragmatic Programmer"; a takeaway coffee cup with
"Code. Coffee. Repeat." handwritten on it; a small potted plant; and a spiral notepad
with a checklist "Today's Plan: Code, Learn, Build, Repeat". Pure white background,
warm soft lighting, clean detailed anime art style, vibrant colors, high resolution,
full body in frame.
```

</details>

> **🎯 Tip:** Generate 3–4 variations and pick the one with the cleanest white background and clearest face — the face becomes your ID-badge avatar later.

---

## 🪜 Step 2 — Create Your Special Repository

1. Go to GitHub and create a **new public repository**
2. Name it **exactly the same as your username** (e.g. `username/username`) — this is GitHub's magic profile repo
3. Tick **"Add a README file"** and create it
4. You should see a hint: *"You found a secret! This special repository..."*

---

## 🪜 Step 3 — Generate the Animated Files

Open your AI coding assistant, attach your character image, and paste the master prompt below. Replace everything in `[brackets]` with your own details.

<details>
<summary>📋 <strong>Master Build Prompt — click to expand & copy</strong></summary>

```
I'm attaching my anime-style character image (white background). Build me a complete
animated GitHub profile README. My details: name [YOUR NAME], role [YOUR ROLE], GitHub
username [USERNAME], email [EMAIL], skills [SKILL LIST], fun tagline [TAGLINE]. Deliver
these files:

1. banner.svg — dark pink/purple animated SVG (about 1280x740): terminal line typing
"user@dev:~$ cat README.md" with blinking cursor; my name in a script font converted to
vector outlines (so it renders identically everywhere) with an animated pink-to-purple
gradient, letters popping in one by one; cycling typed role titles; a typed quote box
with my tagline; tech-stack pills fading in with hover effects; About Me lines; an
animated stats bar; a code-editor card that types out a fun buildDreams() JSX snippet
line by line; a neon sign that flickers on saying "KEEP CODING KEEP GROWING"; floating
hearts, twinkling sparkles, rising particles, pulsing ambient orbs. Remove my image's
white background and embed it as base64 PNG (not WebP — old Safari). Reveal my character
with a one-time top-to-bottom hologram formation led by a glowing scan line, then run a
continuous full-width horizontal scanner sweeping top to bottom every 3.5s, clipped to
the banner's rounded corners. Make every typing reveal window much taller than the text
so no OS font ever clips letters.

2. banner-light.svg — the same banner recolored to blend into a white page, and wire the
README with a <picture> prefers-color-scheme tag so dark/light mode auto-switch.

3. lanyard.svg — a swinging ID badge in pure SVG (React-Bits Lanyard style): pink strap
with printed text, metal clasp and ring, dark glass card with my face cropped from my
image inside a glowing avatar ring, my name, role, handle, a barcode, and a holographic
shine sweep. It should drop in from the top, swing with damped pendulum physics, then
sway gently forever.

4. Local stat cards — stats.svg (animated rank ring + stat rows sliding in), langs.svg
(animated language bars), trophies.svg (trophy cells popping in with glowing ranks and a
shine sweep) — all local files so nothing depends on rate-limited third-party card
services.

5. README.md — centered layout embedding everything, plus a projects table, contribution
activity graph, connect badges, profile-views counter, and the snake animation image.

6. github-snake.yml — a GitHub Action using Platane/snk that generates a
custom-colored snake daily to the "output" branch.

Rules: use only SMIL + CSS animations (GitHub strips JavaScript), verify my real profile
details, and add ?v=1 cache-busting query parameters to every local image reference in
the README.
```

</details>

---

## 🪜 Step 4 — Upload Everything

1. In your `username/username` repo, click **Add file → Upload files**
2. Upload all the SVGs + `README.md` to the repository root
3. Create the folder path `.github/workflows/` and upload `github-snake.yml` there
4. **Commit** — your profile updates instantly (snake appears after Step 5)

---

## 🪜 Step 5 — Activate the Snake

1. Open your repo's **Actions** tab and enable workflows if asked
2. Select the snake workflow → **Run workflow** (runs ~1 minute)
3. It publishes the snake SVG to an `output` branch and refreshes daily automatically

---

## 🪜 Step 6 — The Cache Trick ⚠️

> **Important:** GitHub caches README images hard. If you ever edit an SVG and "nothing changes," the file is fine — the cache is stale.

**Fix:** in `README.md`, bump the version query on that image, e.g. `banner.svg?v=1` → `?v=2`. New URL = instant fresh fetch.

**Best practice:** commit the SVG first, then commit the README with the bumped number.

---

## 💎 Pro Tips

- 🎥 Screen-record the banner booting up — it makes a killer reel/short
- 🛠️ Ask the AI to tweak anything: scanner speed, colors, new sections — iterate freely
- 📈 Numbers in local stat cards are static; refresh them when your stats grow
- 🌗 Test both GitHub themes: **Settings → Appearance → light / dark**

---

<div align="center">

### 🩵 That's it — your profile is now alive.

*If this guide helped, share it forward. Keep coding, keep growing.*

![Footer](https://img.shields.io/badge/Made%20with-SVG%20%2B%20SMIL-38BDF8?style=for-the-badge&labelColor=0C4A6E)

</div>
