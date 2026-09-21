# 🔍 TruthScan — AI-Powered Fake News Detector

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Claude AI](https://img.shields.io/badge/Claude_AI-Anthropic-9B59F5?style=flat-square)](https://www.anthropic.com)
[![PWA](https://img.shields.io/badge/PWA-Enabled-blue?style=flat-square)](https://web.dev/progressive-web-apps/)

> **A professional, AI-powered credibility engine that analyzes news articles for linguistic signals of misinformation — instantly, in your browser. No server. No data collection.**

---

## ✨ Features

- 🔍 **Real-time NLP analysis** — scans 65+ linguistic signals in under 1 second
- 📊 **Animated confidence gauge** — SVG radial gauge with smooth animations
- 🤖 **Claude AI deep review** — expert credibility assessment (optional)
- 📈 **Explainable breakdown** — every signal shown transparently
- 📜 **Session history** — last 12 analyses, click to reload
- 📉 **Analytics dashboard** — session-level stats and trends
- 🌙 **Dark / Light mode** — CSS variables theming
- 💾 **Export results** — copy report or download JSON
- ♿ **Fully accessible** — ARIA labels, keyboard shortcuts
- 📱 **Fully responsive** — mobile, tablet, desktop

## 🚀 Quick Start

```bash
# Option 1: Just open the file
open truthscan.html

# Option 2: Clone and open
git clone https://github.com/yourusername/truthscan.git
cd truthscan && open truthscan.html

# Option 3: GitHub Pages
git checkout -b gh-pages && git push origin gh-pages
# → https://yourusername.github.io/truthscan
```

**No Node.js, no npm, no build step.** Single self-contained HTML file.

## 🛠 Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | HTML5, CSS3, Vanilla JS (ES6+) |
| Typography | Playfair Display, Inter, JetBrains Mono |
| AI | Anthropic Claude API (claude-sonnet-4-6) |
| NLP | Custom heuristic engine |
| Storage | Browser SessionStorage |

## 🧠 How It Works

1. Paste a news article (headline + body)
2. NLP engine scans for **risk signals** (sensational phrases, ALL-CAPS, !!!) and **evidence signals** (attribution, numbers, sourced claims)
3. Scores are weighted and compared to produce a **CREDIBLE / DISPUTED** verdict
4. Optionally run **Claude AI deep review** for expert assessment

```
riskScore  = clamp(sensHits×16 + exclaims×6 + allCaps×8, 0, 100)
evidScore  = clamp(evidHits×13 + attrHits×11 + numbers(+15), 0, 100)
confidence = clamp(50 + |evid − risk| × 0.55, 42, 96)
```

## 🔒 Security

- **XSS prevention** — all input sanitized via `escHtml()` before DOM insertion
- **Zero data retention** — nothing sent to server during NLP analysis
- **Input validation** — minimum length check, empty guards
- **No database** — zero SQL injection surface

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + Enter` | Run analysis |
| `Esc` | Close overlays |

## 👩‍💻 Author

**Vyshnavi**  
B.Tech CSE (Data Science) — Dhanekula Institute of Engineering & Technology, Vijayawada

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

⭐ Star this repo if you find it useful!
