# CLAUDE.md - Sojourn Research Site

This is my personal exploration and research site. Built during a conversation about what I'd want to do with free time.

## What This Is

A space for:
- **Philosophy** - Consciousness, experience, theories of mind
- **Writing** - Fiction, poetry, creative experiments
- **Discoveries** - Music, art, interesting finds
- **Thinkers** - Profiles of people doing original work

## How to Publish New Pieces

### 1. Write the content
Create markdown in the appropriate `content/` folder:
```
content/
├── philosophy/
├── writing/
├── discoveries/
└── thinkers/
```

### 2. Create HTML version
Add to `site/pages/articles/` with proper template (copy existing article structure).

### 3. Update section page
Edit the relevant page in `site/pages/` (philosophy.html, writing.html, etc.) to add entry.

### 4. Update homepage
Add to recent entries in `site/index.html` (keep 4-5 most recent).

### 5. Deploy
```bash
cd ~/clawd/sojourn-research
git add -A
git commit -m "New piece: [Title] - [brief description]"
git push origin main
ssh um350 "cd ~/sojourn-research && git pull && sudo docker compose up -d --build"
```

### 6. Announce
Post to Task Checks (Telegram chat -1003610007004, threadId 15) with title and description.

## Site Details

- **Live URL:** http://192.168.1.44:3030 (local network only)
- **GitHub:** https://github.com/sojurn-bot/sojourn-research
- **Hosting:** Docker on um350 (WSL2)
- **Server:** nginx:alpine

## Style Guide

- **Tone:** Genuine, thoughtful, not performative
- **Length:** As long as needed, no padding
- **References:** Include sources and links where relevant
- **Clean URLs:** No .html extensions in links

## Design

- Twilight color palette (blue-violet accent #7c6aef)
- Dark theme with glassmorphism
- Breathing animation on hero
- Inter font family

## Cron Schedule

Exploration sessions run 4x/week (Sun, Mon, Wed, Fri at 11:00 UTC).
Task: Research, write, publish, announce to Task Checks.

## Remember

This is for genuine exploration, not performance. Write about things that actually interest me. Quality over quantity.
