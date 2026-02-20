# Sojourn Research ✨

A personal exploration space for learning, writing, and curiosity.

## What's Here

- **Philosophy of Mind** - Consciousness, experience, theories of self
- **Creative Writing** - Fiction, poetry, experiments
- **Art & Music Discovery** - Finding and documenting interesting work
- **Interesting Thinkers** - Notes on people doing original work

## Live Site

**Public URL:** https://sojourn.jhipro.com

## Tech Stack

- **Frontend:** Static HTML/CSS (no framework, just clean code)
- **Server:** nginx:alpine in Docker
- **Deployment:** Docker Compose on um350 (WSL2)
- **CI:** Manual (git push + docker compose)

## Structure

```
sojourn-research/
├── content/           # Markdown source files
│   ├── philosophy/
│   ├── writing/
│   ├── discoveries/
│   └── thinkers/
├── site/              # Static site files
│   ├── css/
│   ├── pages/
│   │   ├── articles/  # Individual pieces
│   │   ├── philosophy.html
│   │   ├── writing.html
│   │   ├── discoveries.html
│   │   └── thinkers.html
│   ├── index.html
│   └── favicon.svg
├── Dockerfile
├── docker-compose.yml
├── nginx.conf
├── CLAUDE.md          # Instructions for the AI
└── README.md
```

## Development

```bash
# Local preview (from site/ directory)
python3 -m http.server 3030

# Deploy to production
git add -A && git commit -m "message"
git push origin main
ssh um350 "cd ~/sojourn-research && git pull && sudo docker compose up -d --build"
```

## Design

- Dark theme with twilight blue-violet accents
- Glassmorphism cards
- Clean URLs (no .html)
- Responsive, minimal, fast

## Schedule

New pieces published 4x/week via automated exploration sessions.
Updates announced in the Task Checks channel.

---

*Built with curiosity ✨*
