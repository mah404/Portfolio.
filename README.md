# Hey, I'm Mah 👋

Honestly? I could have spent weeks building a fancy portfolio website with smooth animations and a dark mode toggle.

But then I thought — *why describe what I can do when I can just... do it?*

So instead of a website, here are the actual projects. They speak for themselves. 🚀

---

## 🛠️ What I've Built (While Others Were Making Portfolio Sites)

---

### 🔁 CI/CD Pipeline — Live on the Internet
> *A full production DevOps setup. From zero to auto-deploying, SSL-secured, monitored app.*

**🌍 Live at:** [https://servercicdpoplines.duckdns.org](https://servercicdpoplines.duckdns.org)

What's inside:
- Node.js app containerized with **Docker**
- Every `git push` → **GitHub Actions** builds image → pushes to **Docker Hub** → SSHs into server → deploys automatically
- Running on a real **Hetzner VPS** (not some free tier that sleeps)
- **Nginx** as reverse proxy with **Let's Encrypt SSL** — proper HTTPS, no warnings
- **Prometheus + Grafana** monitoring with live CPU, RAM, disk dashboards
- Free domain via **DuckDNS**

**Tech:** Docker · GitHub Actions · Nginx · Certbot · Prometheus · Grafana · Hetzner · DuckDNS

🔗 [View the repo](https://github.com/mah404/ci-cd-pipeline)

---

### 📹 terminalreplay — Screen Recording for Developers
> *Because your terminal deserves better than a pixel-grabbing screen recorder.*

Ever tried to record a terminal session and ended up with a blurry 200MB video that nobody wants to watch? Yeah. This fixes that.

`terminalreplay` captures the **actual terminal story** — commands, output, timing, colors — not just pixels. The result is lighter, editable, and actually useful for tutorials, onboarding, and README demos.

```bash
npx terminalreplay record
npx terminalreplay replay session.tr --cinematic
npx terminalreplay export session.tr --gif
npx terminalreplay export session.tr --video
```

What it does:
- Records live terminal sessions via PTY — timing, ANSI colors, resize events, all of it
- Replays interactively with pause, seek, and speed control
- Exports to **standalone HTML**, **animated GIF**, or **MP4** via ffmpeg
- Edit recordings — trim, merge, convert to asciinema
- Ships with themes: cyberpunk, dracula, nord, matrix, hacker green

Built in **TypeScript** with a clean modular architecture — recorder, replay engine, frame renderer, and export pipeline all separate.

**Tech:** Node.js · TypeScript · node-pty · ffmpeg · Commander CLI

🔗 [View the repo](https://github.com/mah404/terminalreplay) · [npm package](https://www.npmjs.com/package/terminalreplay)

---

### 🤖 Telegram Video Downloader Bot
> *Because why use sketchy websites when your own server can do it?*

**Paste any URL → choose Video or Audio → get the file in Telegram**

- Supports **1000+ platforms** (YouTube, Instagram, TikTok, Twitter, Facebook, Vimeo...)
- Private bot — only I can use it
- Runs 24/7 on my own server — no Vercel, no cold starts, no limits
- Dockerized and auto-deployed via CI/CD

**Tech:** Python · yt-dlp · python-telegram-bot · Docker · Hetzner

🔗 [View the repo](https://github.com/mah404/telegram-bot) *(coming soon)*

---

## 🧰 Tech Stack

**DevOps & Infrastructure**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

**Development**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

**Cloud & Hosting**

![Hetzner](https://img.shields.io/badge/Hetzner-D50C2D?style=flat&logo=hetzner&logoColor=white)
![Docker Hub](https://img.shields.io/badge/Docker_Hub-2496ED?style=flat&logo=docker&logoColor=white)

---

## 📊 GitHub Stats

![mah404's GitHub stats](https://github-readme-stats.vercel.app/api?username=mah404&show_icons=true&theme=tokyonight&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=mah404&layout=compact&theme=tokyonight&hide_border=true)

---

## 📫 Contact

[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=flat&logo=telegram&logoColor=white)](https://t.me/YOUR_TELEGRAM)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:mahtabvariyani@gmail.com)

---

*Still not convinced? Check the repos. The commits don't lie.* 😎
