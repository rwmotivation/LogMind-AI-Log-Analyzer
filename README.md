# 🔍 LogMind — AI Log Analyzer

> A free, browser-based AI log analyzer powered by Google Gemini 2.0 Flash. Paste your logs, get instant AI analysis, charts, timelines, and actionable fix recommendations — no backend, no subscriptions, no data stored.

![LogMind Screenshot](./screenshot.png)

---

## ✨ Features

- **🧠 AI Analysis** — Powered by Google Gemini 2.0 Flash (free). Gets you an Executive Summary, Critical Issues, Error Patterns, Service Analysis, Recommendations, and Risk Assessment in plain English
- **📊 Interactive Charts** — Log level distribution donut, error trend line chart, top services bar chart, and error/warning heatmap — all via Chart.js (no API key needed)
- **🕐 Color-coded Timeline** — Every log entry listed and highlighted by severity: CRITICAL / ERROR / WARN / INFO / DEBUG
- **🗺 Service Flow Diagram** — Canvas-rendered visual map of services inferred from your logs
- **🖼 Free Export Options** — Download charts as PNG/SVG, open diagrams in Mermaid Live, Excalidraw, Grafana Play, or Kibana — all free, no login required
- **📋 4 Built-in Sample Logs** — Web Server, Database, Kubernetes, and App Errors to test instantly
- **🔒 Privacy-first** — Runs entirely in your browser; your API key is never stored; log data goes only to the Google Gemini API under your own key

---

## 🚀 Quick Start

### 1. Get a Free API Key

Go to **[aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)**, sign in with your Google account, and click **Create API Key**.

- ✅ No credit card required
- ✅ 1,500 free requests/day on Gemini 2.0 Flash
- ✅ Takes about 60 seconds

### 2. Run the Tool

**Option A — Use directly from GitHub Pages (recommended):**
```
https://YOUR_USERNAME.github.io/logmind
```

**Option B — Run locally:**
```bash
git clone https://github.com/YOUR_USERNAME/logmind.git
cd logmind
# Open index.html in any browser — no build step, no npm install
open index.html
```

### 3. Analyze Your Logs

1. Paste your Google AI Studio API key into the key field
2. Paste any log data into the text area (or click a sample button)
3. Hit **Analyze Logs** (or press `Ctrl+Enter` / `Cmd+Enter`)
4. Explore the AI analysis and visualizations across the tabs

---

## 🖥 Supported Log Formats

LogMind auto-detects the log structure. It works with any log data that contains timestamps, severity levels, and messages, including:

| Format | Example Sources |
|--------|----------------|
| Standard syslog | Linux system logs, nginx, Apache |
| Application logs | Node.js, Python, Java, Go apps |
| Kubernetes events | kubelet, scheduler, ingress, HPA |
| Database logs | PostgreSQL, MySQL, MongoDB |
| Cloud logs | AWS CloudWatch, GCP Cloud Logging |
| Custom app logs | Any log with ERROR / WARN / INFO keywords |

---

## 📸 Screenshots

| AI Analysis | Charts | Timeline |
|-------------|--------|----------|
| ![analysis](./docs/analysis.png) | ![charts](./docs/charts.png) | ![timeline](./docs/timeline.png) |

---

## 🗂 Project Structure

```
logmind/
├── index.html        # Entire application — single self-contained file
├── README.md         # You are here
├── LICENSE           # MIT License
└── docs/
    └── *.png         # Screenshots for README
```

No build tools. No dependencies to install. No node_modules. The entire app is one HTML file using:

- **[Chart.js 4.4](https://www.chartjs.org/)** — loaded via CDN, for all charts
- **[Google Fonts](https://fonts.google.com/)** — IBM Plex Mono + Space Grotesk
- **[Google Gemini API](https://ai.google.dev/)** — AI analysis (free via AI Studio)
- Vanilla HTML / CSS / JavaScript — everything else

---

## 🔐 Privacy & Security

| What | How it's handled |
|------|-----------------|
| API key | Stored only in the browser tab's memory — never saved to localStorage, cookies, or any server |
| Log data | Sent only to Google's Gemini API using **your own API key** on **your own quota** |
| Analysis results | Displayed in-browser only — never stored or transmitted elsewhere |
| No telemetry | Zero analytics, tracking, or usage data collection of any kind |

> ⚠️ **Heads up:** If your logs contain sensitive data (credentials, PII, internal hostnames), review your organisation's policy on sending data to third-party AI APIs before use. For air-gapped environments, consider the self-hosted Gemini via Vertex AI option.

---

## 🆓 Free Visualization Tools Used

All diagram and image export options in LogMind use free, open-source tools — no paid API required:

| Tool | Use case | Cost |
|------|----------|------|
| [Chart.js](https://www.chartjs.org/) | In-app charts | Free / OSS |
| [Mermaid Live](https://mermaid.live/) | Flowcharts & sequence diagrams | Free |
| [Excalidraw](https://excalidraw.com/) | Hand-drawn architecture diagrams | Free |
| [Grafana Play](https://play.grafana.org/) | Observability dashboards | Free (hosted demo) |
| [Elastic / Kibana](https://demo.elastic.co/) | Full log analytics | Free (self-host or demo) |
| PNG/SVG export | Save charts as images | Built-in, free |

---

## 🛣 Roadmap

- [ ] Drag-and-drop log file upload (`.log`, `.txt`, `.json`)
- [ ] Multi-file comparison view
- [ ] Custom log format parser (regex builder)
- [ ] Saved analysis history (local storage)
- [ ] Dark / light theme toggle
- [ ] Share analysis as a public URL (optional, self-hosted backend)
- [ ] Slack / Teams webhook integration for alerts

Have a feature idea? [Open an issue](https://github.com/YOUR_USERNAME/logmind/issues) — contributions are welcome!

---

## 🤝 Contributing

Contributions, bug reports, and feature requests are all welcome.

```bash
# 1. Fork the repo
# 2. Make your changes to index.html
# 3. Test in a browser
# 4. Open a pull request — describe what you changed and why
```

Since this is a single-file project, there's no build pipeline to worry about. Just edit and test.

---

## 📄 License

MIT License — free to use, fork, modify, and distribute. See [LICENSE](./LICENSE) for details.

---

## 🙌 Acknowledgements

- [Google AI Studio](https://aistudio.google.com/) for the free Gemini API
- [Chart.js](https://www.chartjs.org/) for the charting library
- The DevOps & SRE community for the constant inspiration to build better debugging tools

---

<p align="center">
  Built with ❤️ to end 3 AM log debugging spirals<br/>
  <a href="https://aistudio.google.com/app/apikey">Get your free API key</a> · 
  <a href="https://github.com/YOUR_USERNAME/logmind/issues">Report a bug</a> · 
  <a href="https://github.com/YOUR_USERNAME/logmind/issues">Request a feature</a>
</p>
