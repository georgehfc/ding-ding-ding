# 🔔 Ding Ding Ding
### Design Intelligence for a Digital Growth Agency

A single-file internal tool for design teams to catalog incoming clients, track them through the pipeline, and auto-generate moodboard briefs.

---

## What it does

1. **Paste a sales email** → AI extracts the client profile, deliverables, team, value prop, and design direction in seconds
2. **Kanban pipeline** → Tracks every client across: Strategy → Wireframes → Copy Signoff → Research → Moodboard → Design
3. **Auto-generates moodboard brief** when a card reaches the **Research** phase — complete with:
   - Awwwards, Webflow, and Framer search keywords (clickable links)
   - Tone, typography pairings, animation guidance
   - Stock imagery directions + Unsplash search links
   - Color palette direction
   - Competitor context + 10-reference research guide
   - Avoid list

---

## Setup (5 minutes)

### Option A — GitHub Pages (recommended)

1. Fork or clone this repo
2. Go to **Settings → Pages → Source** → select `main` branch, root folder
3. Your app will be live at `https://yourusername.github.io/ding-ding-ding`

### Option B — Local

Just open `index.html` in any modern browser. No build step, no dependencies.

---

## API Key

You need an [Anthropic API key](https://console.anthropic.com/) to use the parsing and brief generation features.

- Paste your key (`sk-ant-...`) in the **bottom-left sidebar** and click Save
- The key is stored in your browser's `localStorage` — it never leaves your device
- Each team member sets their own key in their own browser

---

## How to use

### Adding a new client
1. Paste the raw sales announcement email into the **New client intake** textarea
2. Click **Parse email**
3. Claude extracts and enriches the brief — client appears in the **Strategy** column

### Moving through the pipeline
- Open any client card to see their full brief
- Use **Move phase** buttons to advance them through the pipeline
- When a card reaches **Research**, the moodboard brief generates automatically

### Moodboard brief
The brief includes:
- **Search links** — click any keyword pill to search Awwwards, Webflow, or Framer directly
- **Unsplash links** — stock imagery search terms, one click to open
- **Typography pairings** — two specific font pair suggestions with rationale
- **Colour direction** — descriptive palette guidance
- **Avoid list** — what NOT to bring into this project

---

## Data & privacy

All client data lives in your browser's `localStorage`. Nothing is sent to any server except the Anthropic API when you parse an email or generate a brief. No backend, no database, no accounts.

---

## Tech stack

- Vanilla HTML/CSS/JS — zero dependencies, zero build step
- [Anthropic Messages API](https://docs.anthropic.com/en/api/messages) — `claude-sonnet-4-20250514`
- Google Fonts — Syne + DM Sans + DM Mono
- localStorage for persistence

---

## Customising

All configuration is at the top of the `<script>` block in `index.html`:

```js
const PHASES = ['Strategy','Wireframes','Copy Signoff','Research','Moodboard','Design'];
```

Rename or reorder phases to match your agency's actual workflow.

---

*Built for design teams at digital growth agencies. Not for resale.*
