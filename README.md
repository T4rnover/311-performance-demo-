# 311-performance-demo
Reading what the categories hide — a 311 performance demo
# Reading what the categories hide — a 311 performance demo

A live demonstration for public-sector performance management: it takes a month of real
[Open311](https://wiki.open311.org/GeoReport_v2/) service requests and shows the step that
turns data you *collect* into data you can *act on* — reading the free-text description the
category field throws away.

On the sample data (a public pull from **New Haven, CT**), reading the text surfaces a
**seven-record placard-fraud cluster** hidden inside routine "Parking Violations," plus several
safety items miscategorized in a way that let them age without escalation. None of it required
new data collection.

**Live site:** `https://YOURUSERNAME.github.io/311-performance-demo/`

## Files

| File | What it is |
|------|------------|
| `index.html` | Landing page / explainer (this is what the site opens to) |
| `demo.html` | The demo. Runs the classification two ways — see below |
| `claude-version.html` | Alternate build that runs on Anthropic's hosted model; **only functions inside a Claude.ai session** |

## Three ways to run the reading in the demo

1. **In your browser — nothing to install.** `demo.html` defaults to a transparent, in-browser
   rules engine. No account, key, or internet. It shows the exact rule that fired for each record.
   This is the version that works when hosted on GitHub Pages.
2. **With your own open model.** Toggle to *Local open model* to point at
   [LM Studio](https://lmstudio.ai/) (`:1234`) or [Ollama](https://ollama.com/) (`:11434`) —
   a real open-weight LLM, fully on-prem. **Download `demo.html` and open it locally** for this:
   a hosted `https` page cannot call `http://localhost` (mixed content). Enable your server's CORS option.
3. **Inside Claude.ai.** Paste `claude-version.html` into a Claude.ai chat as an artifact; the
   buttons call the hosted model with no key. It will not classify when opened from the hosted site.

## Retargeting to another city

Swap the `RECORDS` array near the top of `demo.html`. Map Open311 fields:
`service_name → intake`, `description → text`. Keep the `exp` fallback block per record.

## Publish to GitHub Pages

**No terminal:** create a new public repo → *Add file → Upload files* → drag all four files in →
*Commit* → **Settings → Pages → Source: Deploy from a branch → `main` / `root` → Save**. The site
appears at `https://YOURUSERNAME.github.io/REPONAME/` in a minute or two.

**With git:**
```bash
git init && git add . && git commit -m "311 performance demo"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/311-performance-demo.git
git push -u origin main
```
Then enable Pages under Settings → Pages.

## Notes

Real public data. AI-drafted narrative is a first draft to verify, never a citation — trace every
named agency, statute, or figure to source. Aggregate analysis only; scrub PII before any model
reads resident text in production.
