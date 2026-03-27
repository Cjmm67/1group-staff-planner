# 1-Group Staff Planner

AI-powered staff planning tool for 1-Group Singapore hospitality venues.

## Features
- **Upload Staff Schedules** — CSV or Excel, auto-extracted by AI
- **Upload Revenue Targets** — calculates staffing requirements per venue
- **AI Assistant** — ask questions about staffing, compliance, costs

## Venues
1-Alfaro, 1-Altitude Coast, 1-Altitude Melaka, 1-Arden (Kaarla, Oumi, Sol & Luna, Bar Op, Concierge), 1-Atico, 1-Flowerhill, Monti, The Alkaff Mansion, The Garage, The Riverhouse, The Summerhouse.

## Setup

### 1. Clone & push to GitHub
```bash
git clone https://github.com/YOUR_USERNAME/1group-staff-planner.git
```

### 2. Deploy to Vercel
- Import the repo at [vercel.com/new](https://vercel.com/new)
- No build settings needed — auto-detected

### 3. Add API Key
In Vercel dashboard → **Settings** → **Environment Variables**:
- `ANTHROPIC_API_KEY` = your key (starts with `sk-ant-...`)

### 4. Redeploy
Vercel auto-deploys on push. Or trigger manually from the dashboard.

## Project Structure
```
├── public/
│   └── index.html          ← the app (no build step)
├── api/
│   └── claude.js           ← serverless proxy for Anthropic API
├── vercel.json             ← Vercel config
└── .gitignore
```

## Tech
- Vanilla HTML/CSS/JS (no framework, no build)
- [SheetJS](https://sheetjs.com/) for Excel parsing (loaded from CDN)
- Vercel serverless function for secure API proxy
- Claude Sonnet for AI extraction & chat
