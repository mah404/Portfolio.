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
📰 The13thDay — Real-Time News Platform

Built this because no single news site had everything I wanted. So I made one that does.

A full-stack news dashboard that pulls from 7 major news agencies simultaneously, streams live TV, monitors X feeds, and lets you bookmark, filter, and translate — all in one place. Not a simple RSS reader. A proper news operations product.
What makes it different from "just another news app":

Aggregates BBC, Reuters, Al Jazeera, Iran International, Tasnim, Fars, Al Arabiya into one unified feed — deduped, sorted, and ranked
Live IRNN TV streaming via HLS.js with a custom proxy route that rewrites playlist segments so the stream actually works in browser
Search isn't just a one-off filter — it turns into a persistent keyword lens that re-ranks your entire feed
Draggable agency bar — reorder your preferred news sources, toggle them on/off, make the feed yours
Inline Persian translation for non-Persian headlines without leaving the page
Bookmark drawer — save stories, come back later, persisted in localStorage
On mobile it doesn't just shrink — it becomes a completely different intent-based launcher UI with cube tiles for each section
Custom Next.js route handlers handle fan-out to scrapers, normalize responses, merge feeds, and fall back gracefully when upstream sources fail

This is one of those projects that looks simple from the outside and is genuinely complex on the inside.
Tech: Next.js 16 · React 19 · TypeScript · Tailwind CSS 4 · HLS.js · Cheerio · Framer Motion · shadcn/ui · RapidAPI
🔗 View the repo · Live demo
