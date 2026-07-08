# Aryan Tripathi - AI Web Builder Portfolio

A minimal, premium, and high-performance single-page developer portfolio designed to make a bold first impression. Built from scratch with vanilla technologies and modern CSS/JS interactions, showcasing top projects, GitHub activity, and a professional "Hire Me" call-to-action.

## 🚀 Features

- **Bat Loader Overlay**: A retro canvas pixel-art bat loader that wipes left-to-right to reveal the website upon load.
- **Interactive Cursor**: Custom double-circle cursor follower that expands magnetically on links, buttons, cards, and interactive chips.
- **Hero Torchlight Effect**: Dual-layer background in the Hero section that reacts dynamically to cursor coordinates, creating a sleek spotlight reveal effect.
- **Selected Work Grid**: Highlighting the top 5 projects with details, live links, and stack tags:
  1. **JeevanRoute (GoldenHour)**: AI emergency routing platform.
  2. **Vertex3**: Teammate-finder network for hackathons.
  3. **BloodEConnect**: Real-time blood donor connector.
  4. **AI Spend Calc**: Financial spend categorization tool.
  5. **Free Fire Frenzy**: Tournament management application.
- **More Projects Accordion**: Collapses client and client-work sites (*Aditya Singh Sengar*, *Tanish FX*, *Shreyansh AV*, *Point Tables*) with a smooth CSS-only height transition.
- **GitHub Activity Section**: Integrates an SVG contribution calendar graph and custom repository cards which fetch live star and fork counts from the GitHub API.
- **AI Stack Swear-By Grid**: A clean, categorized dashboard detailing the AI and core web tools used.
- **"Hire Me" CTA & Form**: Interactive pitch, social cards with copyable email popup, and a Google Sheets-backed form utilizing Google Apps Script.

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3 (Custom variables, transitions, responsive grids), ES6+ JavaScript (Vanilla)
- **APIs**: GitHub REST API (Repo stats), Google Sheets Google Apps Script API (Contact form submissions), GitHub Contribution Chart API
- **Fonts**: Space Grotesk & Space Mono (Google Fonts)

## 💻 Local Setup & Development

Since this project consists of static assets, you can run it directly:

1. **Direct Load**: Double-click or open `index.html` in any web browser.
2. **Local HTTP Server**: For features like API calls, load testing, or clean routes, run a local web server:
   - **Python**:
     ```bash
     python -m http.server 8000
     ```
   - **Node.js**:
     ```bash
     npx serve
     ```
3. Open `http://localhost:8000` (or the port specified by serve) in your browser.

## 📦 Deployment

The portfolio is fully responsive and configured to be deployed on **Vercel** or **GitHub Pages**:
- Push changes to a GitHub repository.
- Link the repository to Vercel.
- Vercel will automatically detect the entry point (`index.html`) and deploy it instantly.
