# Interactive Scroll Portfolio — Ummu Salma Hasmy

A high-performance, modern single-page web developer portfolio featuring a smooth, canvas-driven background video frame animation on scroll, dynamic glassmorphism UI components, and data-driven content loading via `content.json`.

---

## 🌟 Features

- **Canvas Scroll Animation**: Synchronizes 240 high-resolution background frames (`bg_frames/`) with user scroll progress using an HTML5 Canvas rendering engine.
- **Data-Driven Content**: All portfolio copy (bio, metrics, skills, featured projects, process steps, and social links) is dynamically loaded from `content.json`.
- **Glassmorphism Design System**: Dark mode aesthetic styled with glowing HSL orange accents, backdrop blurring, subtle border highlights, and interactive hover states.
- **Responsive Layout**: Designed for seamless viewing across ultra-wide monitors, laptops, tablets, and smartphones.
- **Zero-Dependency Core**: Built with vanilla HTML5, CSS3, and modern JavaScript (ES6+), alongside Lucide icons for clean visual indicators.

---

## 📁 Directory Structure

```text
portfolio-vibed/
├── bg_frames/          # Contains background image sequence (ezgif-frame-001.jpg ... ezgif-frame-240.jpg)
├── content.json        # Dynamic content source file for text, metrics, projects & links
├── index.html          # Main application file (HTML structure, CSS styles & JS animation engine)
└── README.md           # Project documentation and local execution guide
```

---

## 🚀 How to Run Locally

Because the application fetches `content.json` asynchronously via JavaScript `fetch()`, opening `index.html` directly via the `file://` protocol in a browser may trigger local CORS security restrictions. Operating a local HTTP server is recommended.

### Method 1: Using VS Code Live Server Extension (Recommended)
1. Open the project folder in **VS Code**.
2. Install the **Live Server** extension (by Rita Wickramasinghe).
3. Right-click `index.html` and select **"Open with Live Server"**.
4. The site will launch automatically in your browser at `http://127.0.0.1:5500/`.

### Method 2: Using Python (Built-in)
Run one of the following commands in your terminal inside the project directory:

```bash
# Python 3
python -m http.server 8000
```
Then open your browser and navigate to: [http://localhost:8000](http://localhost:8000)

### Method 3: Using Node.js / npx
If you have Node.js installed, execute:

```bash
npx serve .
```
or
```bash
npx http-server .
```
Then open the server URL provided in the terminal output.

---

## ⚙️ Customization Guide

- **Update Copy & Projects**: Modify `content.json` to update stats, project descriptions, skills, or social handles without touching HTML code.
- **Adjust Frame Sequence**: To change the background animation, replace frame images in `bg_frames/` and adjust `MAX_PROBE_FRAMES` in `index.html` if necessary.
