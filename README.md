# Hey, I'm Mah 👋

Honestly? I could have spent weeks building a fancy portfolio website with smooth scroll animations, a dark mode toggle, and a "hire me" button that does nothing.

But then I thought — *why describe what I can do when I can just... do it?*

So instead of a website, here are the actual projects. They speak for themselves. 🚀

---

## 🛠️ Projects (While Others Were Making Portfolio Sites)

---

### 🔁 CI/CD Pipeline — Live on the Internet
> *From laptop to live server. Automatically. Every single push.*

🌍 **Live at:** [https://servercicdpoplines.duckdns.org](https://servercicdpoplines.duckdns.org)
🔒 **Secured with SSL — proper HTTPS, no browser warnings**

You push code. GitHub Actions wakes up. Docker image gets built. Pushed to Docker Hub. SSH'd into a real Hetzner server in Germany. Old container gone. New one running. Done — in under 2 minutes. Zero manual work.

What's inside:
- 🐳 Node.js app containerized with **Docker**
- ⚙️ **GitHub Actions** pipeline — build → push → deploy on every `git push`
- 🖥️ Running on a real **Hetzner VPS** — not some free tier that falls asleep
- 🔀 **Nginx** reverse proxy with **Let's Encrypt SSL** — free HTTPS, auto-renewing
- 📊 **Prometheus + Grafana** — live CPU, RAM, disk dashboards
- 🦆 Free domain via **DuckDNS**

**Tech:** `Docker` `GitHub Actions` `Nginx` `Certbot` `Prometheus` `Grafana` `Hetzner` `DuckDNS` `Node.js`

🔗 [View the repo →](https://github.com/mah404/ci-cd-pipeline)

---

### 🐳 Auto-Dockerize CLI — Dockerize Any Project in One Command
> *Because writing the same Dockerfile for the 10th time is nobody's idea of fun.*

```bash
python dockerize_project.py /path/to/project
```

Point it at any project. It figures out what it is. Generates the right Dockerfile. Validates it. Builds it. Commits and pushes to GitHub. One command, done.

- 🔍 **Auto-detects** Python, Node.js, Next.js, or static HTML
- 📄 Generates matching `Dockerfile` + `.dockerignore` for that stack
- ✅ **Validates** for common Docker mistakes before building
- 🏗️ Runs `docker build` to verify it actually works
- 📤 **Commits and pushes** to your existing GitHub remote automatically

Useful flags:
```bash
--skip-build    # No Docker installed? No problem
--skip-push     # Review before publishing
--force         # Overwrite existing Dockerfile
--type python   # Override auto-detection
```

**Tech:** `Python` `Docker` `Git` `HTML` `CSS`

🔗 [View the repo →](https://github.com/mah404/Auto-Dockerize-CLI)

---

### 📹 terminalreplay — Screen Recording for Developers
> *Because your terminal deserves better than a blurry 200MB pixel recording.*

Most screen recorders capture pixels. `terminalreplay` captures the actual terminal story — commands, output, timing, ANSI colors. Lighter. Editable. Actually useful.

```bash
npx terminalreplay record
npx terminalreplay replay session.tr --cinematic
npx terminalreplay export session.tr --gif
npx terminalreplay export session.tr --video
```

- 🎬 Records live terminal sessions via PTY — timing, colors, resize events, everything
- ⏯️ Replays interactively — pause, seek, speed control
- 📦 Exports to **standalone HTML**, **animated GIF**, or **MP4** via ffmpeg
- ✂️ Edit recordings — trim, merge, convert to asciinema
- 🎨 Themes: `cyberpunk` `dracula` `nord` `matrix` `hacker green`

**Tech:** `Node.js` `TypeScript` `node-pty` `ffmpeg` `Commander CLI`

🔗 [View the repo →](https://github.com/mah404/terminalreplay) · [npm →](https://www.npmjs.com/package/terminalreplay)

---

### 📰 The13thDay — Real-Time News Platform
> *No single news site had everything I wanted. So I built one that does.*

A full-stack news dashboard pulling from **7 major agencies simultaneously** — BBC, Reuters, Al Jazeera, Iran International, Tasnim, Fars, Al Arabiya — deduped, sorted, ranked, and presented in one place. With live TV. And bookmarks. And Persian translation. Yeah.

- 📡 **Live IRNN TV streaming** via HLS.js with a custom proxy route that rewrites playlist segments so the stream actually works in browser
- 🔍 Search isn't just a filter — it becomes a **persistent keyword lens** that re-ranks your entire feed
- 🏷️ **Draggable agency bar** — reorder and toggle your preferred news sources
- 🌐 **Inline Persian translation** for non-Persian headlines without leaving the page
- 🔖 **Bookmark drawer** — save stories, come back later, persisted in localStorage
- 📱 On mobile it doesn't just shrink — it becomes a **cube tile launcher UI**
- 🛡️ Custom Next.js route handlers fan out to scrapers, normalize responses, and fall back gracefully when upstream fails

This is one of those projects that looks simple from the outside and is genuinely complex on the inside.

**Tech:** `Next.js 16` `React 19` `TypeScript` `Tailwind CSS 4` `HLS.js` `Cheerio` `Framer Motion` `shadcn/ui` `RapidAPI`

🔗 [View the repo →](https://github.com/mah404/The13thDay) · [Live demo →](https://the13thday.vercel.app/)

---

### 🧅 AnonChat — Anonymous Chat on the Dark Web
> *No accounts. No logs. No IP addresses. Just chat. On the actual dark web.*

Most developers deploy to AWS or Vercel. This one runs as a **Tor hidden service** — a real `.onion` site, only reachable through Tor Browser. Not as a gimmick. Because the whole point is that nobody knows you're there.

- 🎭 Visit the `.onion` address → get assigned `Anon1`, `Anon2`... → chat in real time
- 💨 Server restarts? **All messages gone.** No history, no trace, no database
- 🔒 Tor handles encryption natively — no HTTPS needed on `.onion`
- 📡 Socket.IO runs on polling transport — WebSockets don't play nicely through Tor
- ⚙️ Managed with `systemd` — survives reboots, auto-restarts on crash
- 🗝️ Your `.onion` address is cryptographically tied to a private key on the server — lose it, it's gone forever

**Tech:** `Python` `Flask` `Flask-SocketIO` `Tor` `systemd` `Ubuntu VPS`

🔗 [View the repo →](https://github.com/mah404/Tor-Anon-Chat) · 🧅 `.onion` address in the repo

---

### `>_` Web Terminal — SSH in Your Browser
> *Your server, from any browser, anywhere. No SSH client needed.*

A full browser-based SSH terminal. Open a tab, you're in. No PuTTY. No terminal app. Just a browser.

- 🖥️ Full terminal emulation via **xterm.js** — colors, cursor, scrollback, ANSI, all of it
- 🗂️ **Multiple tabs** simultaneously — `Ctrl+T` new tab, `Ctrl+W` close, just like a real terminal
- ⚡ **WebSocket bridge** — keystrokes go browser → Socket.io → SSH2 → server in real time
- 🔐 SSH credentials never touch the browser — they stay server-side
- 📊 **Live status bar** — connection status, uptime timer, latency
- 📱 **PWA** — install it as a desktop or mobile app
- 🌐 **HTTPS via Cloudflare Tunnel** — free HTTPS URL, zero domain or certificate setup

**Tech:** `NuxtJS 3` `Vue 3` `xterm.js` `Socket.io` `ssh2` `pm2` `Cloudflare Tunnel` `Hetzner VPS`

🔗 [View the repo →](https://github.com/mah404/-Web-Terminal)
🔗 [View Live →](https://gap-cylinder-metabolism-implemented.trycloudflare.com/)


---

## 🧰 Tech Stack

**DevOps & Infrastructure**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![Hetzner](https://img.shields.io/badge/Hetzner-D50C2D?style=flat&logo=hetzner&logoColor=white)

**Development**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat&logo=vuedotjs&logoColor=white)

**Tools & Platforms**

![Docker Hub](https://img.shields.io/badge/Docker_Hub-2496ED?style=flat&logo=docker&logoColor=white)
![Tor](https://img.shields.io/badge/Tor-7D4698?style=flat&logo=torproject&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=cloudflare&logoColor=white)
![npm](https://img.shields.io/badge/npm-CB3837?style=flat&logo=npm&logoColor=white)

---
