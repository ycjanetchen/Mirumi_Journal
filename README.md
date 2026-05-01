# Mirumi — Emotion Tracking Journal

> *"The days that made you."*

Mirumi is browser-based emotion journaling tool with an optional Therapist Portal for clinical session preparation. No account required. All data stays in your browser.

**🔗 Live demo:** [ycjanetchen.github.io/Mirumi_Journal](https://ycjanetchen.github.io/Mirumi_Journal/) · [Therapist Portal](https://ycjanetchen.github.io/Mirumi_Journal/therapist.html)

---

## What it does

### Daily Journal

Write about your day — anything on your mind. Mirumi reads the emotional weight of your words and responds with:

- **Mood recognition** — identifies how you're really feeling, not just how you say you are
- **Praise** — finds the strength and courage in your day, even on the hardest ones
- **Gentle feedback** — honest, constructive reflection without judgment
- **Growth tips** — specific, actionable suggestions to move forward

You don't need to summarise or structure your writing. Just write.

### Relationship Archive (optional)

When you mention a person by name in your journal, they can be added to your **Relationship Archive**. You can also log specific situations with someone directly — Mirumi gives you a 5-dimension analysis:

1. Your emotional state in this dynamic
2. Their likely perspective
3. Specific advice (with example phrases)
4. Red flags to watch for
5. Relationship trajectory + health score

Each new entry builds on the history of previous ones, so the advice grows more personalised over time.

### Archive & Emotional Journey

Your past entries are saved privately in your browser. The Archive page shows:

- A **line chart** of your emotional journey over time
- A **mood flower** visualising your emotional distribution
- Full browsable history of journal entries and relationship check-ins

---

## Therapist Portal

When a user wants to bring their week into a therapy session, they can export a **JSON report** from the Archive page. The therapist opens the [Therapist Portal](https://ycjanetchen.github.io/Mirumi_Journal/therapist.html) and uploads the file.

The portal shows:

- **7-day mood timeline** with crisis language signals flagged (⚠)
- **Crisis risk assessment** — green / amber / red based on language patterns, consecutive low-mood days, and relationship health scores
- **Emotional distribution** chart
- **Client overview** — entries count, low-mood days, relationship scores
- **Relationship health** — per-person trend scores and red flags
- **Full journal entries** — expandable, with AI mood analysis inline
- **AI Weekly Summary** — one click generates a 3–5 sentence clinical paragraph covering the emotional arc, key stressors, and any language worth exploring in session

No client data is stored by the portal. Everything is read from the uploaded file and held in memory only.

---
## Demo Video Link

https://drive.google.com/file/d/15MmyiqlfyKppv6oiH5KJtooiG7sue7pF/view?usp=sharing 

---

## How to use

Both portals are live at the links above — no download or setup required.

### API Key (optional)

Mirumi uses the Anthropic Claude API to generate journal responses and clinical summaries. To use live AI:

1. Get an API key at [console.anthropic.com](https://console.anthropic.com)
2. Click the **⚙** button in the top-right corner of either portal
3. Paste your key — stored only in your browser, sent only to Anthropic

### Demo Mode

Both portals include a built-in **Demo Mode** for trying the full experience without an API key:

- Click **DEMO OFF** in the nav bar → it turns green and shows **DEMO ON**
- In the journal: submit any entry — a realistic AI-style response appears instantly, pre-seeded with a 6-day emotional arc in the archive
- In the therapist portal: click **"Load 7-Day Demo →"** to populate a full week of sample data, then click **"Generate Summary →"** for the clinical paragraph

Demo mode is shared across both portals and persists across page refreshes.

---

## Exporting to the Therapist Portal

1. In the Journal portal, go to the **Archive** tab
2. Scroll to **Generate Therapist Report** and click export — a `.json` file downloads
3. Open the [Therapist Portal](https://ycjanetchen.github.io/Mirumi_Journal/therapist.html) and drag the file onto the upload zone

---

## Privacy

- All journal data is stored in your browser's `localStorage` — it never leaves your device unless you explicitly export it
- The API key is stored locally and only used for direct calls to Anthropic
- The Therapist Portal holds uploaded data in memory only — nothing is written to disk or sent anywhere

---

## Tech

- Pure HTML / CSS / JavaScript — no frameworks, no build step, no server
- Anthropic Claude API (`claude-sonnet-4-6`) for AI responses
- SVG-rendered mood charts and relationship flower visualisations
- Crisis signal detection aligned with Columbia C-SSRS passive ideation indicators

---

## Project

Built for the **CBC Hackathon 2026** — Neuroscience & Mental Health category.

*Mirumi* — from 見る (miru, "to see") — because every day deserves to be seen.
