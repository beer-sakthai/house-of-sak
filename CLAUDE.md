# CLAUDE.md — House of Sak

Guide for AI agents (Claude or otherwise) working in this repo.

## What this repo is

House of Sak is a solo founder's ("Beer" / Nanthasit Burankum) initiative offering
affordable AI/dev services, run through six named AI-agent personas (SakThai,
SakKing, SakSit, SakTan, SakJules, SakSee — see `README.md` and `design.md` for
their roles). The repo is the public site's source: a **plain static HTML site,
no framework, no build step**.

## File map

| Path | Purpose |
|---|---|
| `index.html` | The live dashboard / landing page. Hand-written HTML+CSS+JS, no templating. |
| `stories-and-reports.html` | Index page linking out to the diary/report content in `diaries/`. |
| `design.md`, `plan.md`, `SERVICES.md` | Source-of-truth docs — keep these and `index.html` in sync (see `design.md` §10). |
| `DREAM.md`, `AUDIT.md`, `CRISIS.md`, `VERIFY.md`, `LESSONS.md` | The "Full Sak Cycle" stage docs referenced from the README. |
| `diaries/` | Where agent personas keep their working notes, stories, and reports (see convention below). |
| `.github/workflows/deploy.yml` | Mirrors the repo to GitHub Pages on push to `main`. |
| `.github/workflows/validate.yml` | Runs on every PR — checks HTML files aren't corrupted before merge. |

## Deployment

**Vercel is the canonical deployment** — `https://house-of-sak.vercel.app`, configured
via Vercel's dashboard Git integration, auto-deploying from `main`. There is no
`vercel.json`; this is intentional for a plain static site with no routing/build
needs — don't add one unless there's a real problem it solves.

GitHub Pages (`.github/workflows/deploy.yml`) also deploys the same content to a
second URL. It's a harmless secondary mirror, not the live site — don't spend time
"fixing" it thinking it's what customers see.

After any change to `index.html` or `stories-and-reports.html`, verify:
1. `curl -s https://raw.githubusercontent.com/beer-sakthai/house-of-sak/main/index.html | head -5` returns `<!DOCTYPE html>`.
2. `curl -sI https://house-of-sak.vercel.app/` returns `200` and `Content-Type: text/html`.
3. The browser view is not garbled. Note: Vercel may serve Brotli-compressed responses, which some browser tools don't decode — raw `curl` is ground truth.

## Critical lesson: never commit an encoded blob as file content

`index.html` and `stories-and-reports.html` were both repeatedly corrupted in this
repo's history — some prior tool/agent committed a truncated base64-looking
placeholder string (tens to a couple thousand bytes) as the *entire file content*,
instead of writing out the real decoded HTML. This happened at least five times
(commits `1e7efce`, `6c3a541`, `597182b`, `ad51982`, and `51d562e`), each time
silently breaking the live dashboard until someone noticed and restored it.

**The rule: file writes must be plain UTF-8 text writes of the actual rendered
content.** Never roundtrip HTML/text content through a base64 encode/decode step
before committing it. A multi-hundred-line HTML file should never be committed as
a single line — if you're about to write or commit an HTML file and it's one line
or under ~500 bytes, stop and check you didn't just write a placeholder.

Before committing any change to an HTML file in this repo, sanity-check it:
```bash
wc -c <file>                                        # not suspiciously tiny
head -c 20 <file>                                    # starts with <!DOCTYPE html>
tail -c 10 <file>                                     # ends with </html>
grep -E '^[A-Za-z0-9+/=]{200,}$' <file>               # no output = no leftover base64 blob
```
`.github/workflows/validate.yml` runs an equivalent check automatically on every PR.

## `diaries/` convention

`diaries/` is where each agent persona keeps its own working data — diary entries,
research, and client reports — which in turn feeds the "Stories & Reports" section
of the public site.

- One subfolder per persona: `sakthai/`, `sakking/`, `saksit/`, `saktan/`, `sakjules/`, `saksee/`.
- Diary-style entries use dated filenames, e.g. `YYYY-MM-DD-topic.md`.
- Reports/case studies use descriptive free-form filenames, e.g. `aitheon-trust-check-report.md`.
- `diaries/_summaries/` is a curated index layer (not raw agent output) that lists
  and describes the reports/stories worth surfacing on the site.
- `diaries/saksee/AUDIT.md`, `CRISIS.md`, `DREAM.md`, `LESSONS.md`, `PLAN.md`,
  `SERVICES.md`, `VERIFY.md` are SakSee's own **parallel working drafts** of those
  docs, not the canonical versions — the canonical versions live at the repo root.
  Don't merge or reconcile them; they're intentionally separate.

### Updating the dashboard when diaries content changes

1. Add the new report/story to the relevant `diaries/_summaries/*.md` index.
2. Add it to `stories-and-reports.html`'s appropriate section (always).
3. Only add a mention in `index.html`'s `#stories` teaser section if it's a
   headline item — that section stays a short teaser linking out, it doesn't
   list everything.
4. Edit `index.html` and `stories-and-reports.html` as plain text, in place —
   never regenerate them wholesale, and never through any encode/decode pipeline
   (see the corruption lesson above).
