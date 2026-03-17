# 🛠️ Portfolio Customization Guide
### Step-by-step guide to make this portfolio your own

> This portfolio was originally built by **Aryan Tripathi**. This guide helps you fork it and customize every part — no advanced coding needed. Just follow the steps in order.

---

## 📁 Files You Need

Before starting, make sure you have these 3 files:

| File | What it is |
|---|---|
| `index.html` | The entire website (HTML + CSS + JS all in one file) |
| `front.png` | Your **main portrait image** (shown in the hero section with the torch reveal effect) |
| `bg of main.png` | The **background image** behind your portrait |

---

## ✅ STEP 1 — Replace Your Images

This is the most important visual change. The hero section has a cool **torch/flashlight reveal effect** — as you move your mouse, it reveals your portrait over the background.

### 1a. Prepare your images
- **`front.png`** → Your main portrait / illustration. Ideally a wide image (1400×900px or similar). The subject (you) should be centered.
- **`bg of main.png`** → A background image. Can be an art piece, blurred cityscape, or abstract image.

### 1b. Replace the file names in the code
Open `index.html` and find these two lines (around line 318–329):

```css
.hero-bg-layer {
  background: url('bg of main.png');   /* ← Change this to your background image filename */
}

.hero-main-layer {
  background: url('front.png');        /* ← Change this to your portrait image filename */
}
```

**Example:** If your files are named `my-bg.png` and `my-photo.png`, change it to:
```css
background: url('my-bg.png');
background: url('my-photo.png');
```

> ⚠️ Keep all 3 files in the **same folder**. The image filenames are case-sensitive.

---

## ✅ STEP 2 — Change Your Name

Your name appears in **4 places**. Find and replace all of them:

### 2a. Browser Tab Title
```html
<!-- Around line 5 -->
<title>Aryan Tripathi — AI Web Builder</title>
```
Change `Aryan Tripathi` and `AI Web Builder` to your name and your title/niche.

### 2b. Navigation Logo (top-left)
```html
<!-- Around line 1052 -->
<a href="#" class="logo">AT.</a>
```
Change `AT.` to your own initials (e.g., `JS.` for John Smith).

### 2c. Hero Heading (the big name on screen)
```html
<!-- Around line 1071–1073 -->
<h1 class="hero-name">
  <span class="solid">Aryan</span>
  <span class="solid">Tripathi<span class="outline"> .</span></span>
</h1>
```
Replace `Aryan` with your first name and `Tripathi` with your last name. Keep the `<span class="outline"> .</span>` for the stylistic dot effect, or remove it if you prefer.

### 2d. About Section & Footer
```html
<!-- Around line 1114 -->
Hey! I'm <strong>Aryan Tripathi</strong> — a passionate web builder...

<!-- Around line 1327 -->
Designed &amp; built by <span>Aryan Tripathi</span>
```
Replace both instances of `Aryan Tripathi` with your name.

---

## ✅ STEP 3 — Update Your Taglines & Roles

### 3a. Hero Eyebrow Text
```html
<!-- Around line 1069 -->
<div class="hero-eyebrow">AI Web Builder — Portfolio 2025</div>
```
Change this to describe yourself, e.g.: `Full Stack Developer — Portfolio 2025`

### 3b. Typewriter Roles (the animated text that cycles)
```javascript
<!-- Around line 1383 -->
const roles = ['AI Web Builder.', 'Creative Developer.', 'Fast Executor.', 'UI Enthusiast.', 'Freelancer.'];
```
Replace the items in the array with your own roles. Keep each one short (2–3 words + period).

**Examples:**
```javascript
const roles = ['Frontend Developer.', 'React Specialist.', 'Open Source Lover.', 'Freelancer.'];
```

### 3c. Hero Description Paragraph
```html
<!-- Around line 1077–1080 -->
<p class="hero-desc">
  I build <strong>bold, modern websites</strong> using the power of AI tools — turning ideas into live
  experiences, <strong>fast.</strong>
</p>
```
Rewrite this to describe what you do in 1–2 sentences. Keep the `<strong>` tags around important words for emphasis.

---

## ✅ STEP 4 — Edit the About Section

### 4a. About Paragraphs
```html
<!-- Around line 1113–1119 -->
<p>Hey! I'm <strong>Aryan Tripathi</strong> — a passionate web builder who uses the latest AI tools...</p>
<p>I'm a <strong>fresher</strong> who believes that AI is a superpower...</p>
<p>My approach: <strong>AI for speed, creativity for impact.</strong>...</p>
```
Rewrite all 3 paragraphs to tell your own story. Keep using `<strong>` to highlight key phrases.

### 4b. Stats Box (the 4 number cards)
```html
<!-- Around line 1136–1152 -->
<div class="stat-n">3+</div>  <div class="stat-l">Projects Built</div>
<div class="stat-n">10+</div> <div class="stat-l">AI Tools Used</div>
<div class="stat-n">∞</div>   <div class="stat-l">Ideas to Build</div>
<div class="stat-n">100%</div><div class="stat-l">Passion Driven</div>
```
Change the numbers and labels to reflect your real stats. You can use `∞`, `+`, `%`, or any symbol.

### 4c. Skill Chips (the small tag badges)
```html
<!-- Around line 1120–1132 -->
<span class="chip">Claude AI</span>
<span class="chip">ChatGPT</span>
... etc
```
Delete any chips that don't apply to you and add your own skills. Each skill needs:
```html
<span class="chip">Your Skill</span>
```

---

## ✅ STEP 5 — Replace Projects

Each project follows this exact structure. Find the `proj-list` div (around line 1161) and edit or replace each block:

```html
<div class="proj-item rv">
  <div class="proj-n">001</div>           <!-- Project number -->
  <div class="proj-info">
    <h3>Student Portal</h3>               <!-- ← Project name -->
    <p>Mangalmay Group · 2025</p>         <!-- ← Client/Context · Year -->
  </div>
  <div class="proj-desc">
    A comprehensive student portal...     <!-- ← Short description (1–2 sentences) -->
  </div>
  <div class="proj-tags">
    <span class="ptag">Next.js</span>     <!-- ← Tech stack tags -->
    <span class="ptag">Supabase</span>
  </div>
</div>
```

**To add a clickable link to a project**, change the opening `<div class="proj-item rv">` to:
```html
<div class="proj-item rv" style="cursor:none;" onclick="window.open('https://your-project-url.com','_blank')">
```

**To add more projects**, copy the entire block and paste it after the last one. Update the number (`001`, `002`, etc.) and all the content inside.

**To remove a project**, delete the entire `<div class="proj-item rv"> ... </div>` block.

> The last project (004 "Hire Me") is a special CTA that scrolls to contact — you can keep or remove it.

---

## ✅ STEP 6 — Update the Tools / Stack Section

Find the `tools-grid` div (around line 1235). Each card looks like this:

```html
<div class="tool-card" data-type="AI">
  <span class="tool-icon">✦</span>
  <div class="tool-name">Claude AI</div>
  <div class="tool-type">Coding + Design</div>
</div>
```

- **`data-type`** → The small label in the top-right corner of the card (e.g., `AI`, `Code`, `Design`, `Core`, `Deploy`)
- **`tool-icon`** → Any unicode symbol or emoji (e.g., `⚡`, `◈`, `🔥`, `⬡`)
- **`tool-name`** → The tool's name
- **`tool-type`** → A short description of how you use it

Replace, delete, or add cards to match your actual stack. The grid auto-adjusts to any number of cards.

---

## ✅ STEP 7 — Update Contact Info

### 7a. Email Address
The email appears in **two places**:

**In the HTML popup** (around line 1309):
```html
<span>[email protected]</span>
```
Replace with your email.

**In the JavaScript copy button** (around line 1516):
```javascript
const email = 'tripathiaryan346@gmail.com';
```
Replace with your email here too (this is what actually gets copied to clipboard).

### 7b. Social Links
```html
<!-- Around line 1313–1314 -->
<a href="https://www.linkedin.com/in/aryan-tripathi52" target="_blank" class="soc">↗ LinkedIn</a>
<a href="https://instagram.com/_aryan_tripathi_52" target="_blank" class="soc">↗ Instagram</a>
```
Replace the URLs with your own LinkedIn and Instagram profile URLs.

To **add more social links** (e.g., GitHub, Twitter):
```html
<a href="https://github.com/yourusername" target="_blank" class="soc">↗ GitHub</a>
```

To **remove a social link**, just delete that `<a>` line.

### 7c. Contact Section Intro Text
```html
<!-- Around line 1303 -->
<p class="contact-note rv">Open to freelance projects, collaborations, and cool ideas...</p>
```
Rewrite this to match what you're open to (freelance, internships, full-time, etc.).

---

## ✅ STEP 8 — Connect the Contact Form to Google Sheets

Right now, form submissions go to **Aryan's** Google Sheet. You need to create your own to receive messages.

### Step-by-step:
1. Go to [Google Sheets](https://sheets.google.com) → Create a new spreadsheet
2. Name the columns in row 1: `Timestamp`, `Name`, `Email`, `Message`
3. Go to **Extensions → Apps Script**
4. Delete any existing code and paste this:

```javascript
function doPost(e) {
  const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  const data = JSON.parse(e.postData.contents);
  sheet.appendRow([new Date(), data.name, data.email, data.message]);
  return ContentService.createTextOutput("OK");
}
```

5. Click **Deploy → New deployment → Web App**
6. Set "Who has access" to **Anyone**
7. Copy the **Web App URL** you get

8. In `index.html`, find this line (around line 1467):
```javascript
const SHEET_URL = 'https://script.google.com/macros/s/AKfycbzuo4AQcdZqmx-.../exec';
```
Replace the long URL with **your own Web App URL**.

---

## ✅ STEP 9 — Update the Marquee Strip

The scrolling text banner below the hero lists your tools/skills. Find it around line 1095:

```html
<span class="dot">✦</span> Claude AI <span class="dot">✦</span> ChatGPT <span class="dot">✦</span> v0.dev ...
```

Replace the tool names with your own stack. The strip is **duplicated** (appears twice) to create the seamless loop effect — make sure both copies match.

Pattern for each item:
```html
<span class="dot">✦</span> Your Skill Name
```

---

## ✅ STEP 10 — Final Polish

### Page Title & Meta
At the top of `index.html` (line 5), also update:
```html
<title>Your Name — Your Title</title>
```

### Footer Year
```html
<!-- Around line 1327 -->
Powered by <span>AI ✦</span> 2025
```
Change `2025` to the current year.

### Nav "Available for projects" status
```html
<!-- Around line 1060 -->
<div class="avail-dot"></div>Available for projects
```
Change this text to whatever your current availability is, e.g., `Open to internships` or `Currently busy`.

---

## 🚀 Deploying Your Portfolio

Once done, deploy for free using one of these:

| Platform | How |
|---|---|
| **GitHub Pages** | Push to a repo → Settings → Pages → Deploy from branch |
| **Vercel** | Drag and drop the folder at vercel.com |
| **Netlify** | Drag and drop at netlify.com/drop |

> Make sure `index.html`, `front.png`, and `bg of main.png` (or your renamed versions) are all in the **same folder** when deploying.

---

## 🗂️ Quick Reference Cheat Sheet

| What to change | Where to find it |
|---|---|
| Browser tab title | Line ~5 |
| Nav logo initials | Line ~1052 |
| Hero name (big heading) | Line ~1071 |
| Typewriter roles | Line ~1383 (JavaScript) |
| Hero description | Line ~1077 |
| About paragraphs | Line ~1113 |
| Stats numbers & labels | Line ~1136 |
| Skill chips | Line ~1120 |
| Projects | Line ~1163 |
| Tools/Stack cards | Line ~1235 |
| Email address (HTML) | Line ~1309 |
| Email address (JS copy) | Line ~1516 |
| LinkedIn URL | Line ~1313 |
| Instagram URL | Line ~1314 |
| Google Sheets URL | Line ~1467 |
| Marquee skill strip | Line ~1095 |
| Footer name & year | Line ~1327 |
| Background image | Line ~318 (CSS) |
| Portrait image | Line ~327 (CSS) |

---

*Guide written for the open-source release of Aryan Tripathi's portfolio. Feel free to fork, customize, and ship. 🚀*
