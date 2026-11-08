# MissionStack Academy — promo site

Public promo site for [MissionStack Academy](https://missionstack.madethis.app) and the archive of the weekly **Tech Snapshot**.

Live at **https://missionstack1.github.io/** — GitHub Pages, deployed from `main` / root. No build step, no Jekyll (`.nojekyll` is present), no dependencies: every page is a single self-contained HTML file.

## Layout

```
index.html              promo site (hero, nine paths, youth/adult tracks, Operator Pro, Tech Snapshot, YouTube)
404.html                custom not-found page
snapshots/index.html    Tech Snapshot archive (renders manifest.json)
snapshots/manifest.json list of published issues — the single source of truth for the archive
snapshots/_template.html template for a new issue
snapshots/YYYY-MM-DD.html  one file per issue
robots.txt, sitemap.xml
```

Design tokens match the app: background `#0b0f14`, panel `#111821`, text `#e8f0f8`, muted `#94a3b8`, teal `#14b8a6`, amber `#f59e0b`, system sans + monospace labels, mission-briefing styling.

## Publishing a Tech Snapshot (Monday workflow)

1. Copy `snapshots/_template.html` to `snapshots/YYYY-MM-DD.html` and fill in every `{{FIELD}}`.
2. Add an entry to the **top** of `issues` in `snapshots/manifest.json`:

```json
{
  "issue": 1,
  "date": "2026-11-10",
  "file": "2026-11-10.html",
  "title": "Headline for the week",
  "summary": "One-sentence summary shown on the home page and archive.",
  "topics": ["Nvidia", "Palantir", "Crypto", "Space"]
}
```

3. Commit both files to `main`. Pages redeploys in about a minute; the home page and archive pick the new issue up automatically — no other edits needed.

Rules for issue content: public, sourced, no fabricated quotes, no investment advice, no government or certification claims. Keep the "Mission of the week" tied to a live academy path.

## Access rule reflected on the site

Lesson 1 of every path is free. Lessons 2+ require an Operator Pro enrollment (Option A).

## Contact

missionstack1@gmail.com
