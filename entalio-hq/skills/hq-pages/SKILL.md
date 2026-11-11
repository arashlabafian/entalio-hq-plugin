---
name: hq-pages
description: Publish an explainer, memo, brief, report or decision page into Entalio HQ (hq_page_publish), on HQ's page kit. Use whenever you write up something for someone at Entalio to read or decide - never as a claude.ai artifact.
---

# Pages in HQ

A page for someone at Entalio goes into HQ with `hq_page_publish`, linked to the items it belongs to (`link: ["HQ-12"]`). Revise it by publishing a new version of the same key (`key: "PG-7"`) with a `note`. Find pages with `hq_pages_search`; read one back with `hq_page_get` (`html: true` to revise it). Questions about a page are comments on it (`hq_comment` with its PG key).

## The file
One self-contained HTML file on the page kit: link `https://hq-86189444959.europe-west2.run.app/pages-kit/v1/kit.css` and `kit.js`; the reference is `/pages-kit/v1/example.html` there. Pages run sealed: no network calls, scripts inline, from the kit, or pinned from cdn.jsdelivr.net, cdnjs.cloudflare.com or unpkg.com; images inline or from the kit.

## The order
Header (kind, title, for whom, its items, version), the short answer, what the reader needs to do, then the chapters of its kind, then what happens next:
- **decision:** Why, Options (three, recommended first, with pros, cons and evidence), Recommendation, Evidence.
- **explainer:** Why, How it works, What changes for you.
- **brief:** Situation, What we ask, Timeline, Documents.
- **report:** What happened, Numbers, Problems, Asks.

## Style
Plain, short words. Components, charts and diagrams only where they explain something; nothing moves by itself. Use the kit's full width: never set `--page`, a `max-width` on `.page` or `main`, or a tighter prose cap. No client names or questionnaire answers. Link HQ items as `https://hq-86189444959.europe-west2.run.app/work/KEY`.
