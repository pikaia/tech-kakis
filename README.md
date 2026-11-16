# Tech Kakis — Daily Sharing (blog)

Jekyll site for the Tech Kakis daily sharing posts, to live at
https://pikaia.github.io/tech-kakis/ (repo: `pikaia/tech-kakis`, public).
Structure mirrors the Less Obvious blog (`~/workspace/projects/less-obvious/repo`):
minima theme, GitHub Pages native plugins, no local build step needed.

## Status (2026-11-15)

- Site files built locally by Seven on Chris's instruction, backfilled with
  posts #1 (2026-11-14) and #2 (2026-11-15). NOT yet pushed: the GitHub repo
  does not exist yet.
- Waiting on Chris: create an empty **public** repo named `tech-kakis` under
  the pikaia account (his own Chrome; passkey lives there). Then Seven
  generates a deploy key, Chris pastes it into the repo settings (same as
  Less Obvious), and Seven pushes, verifies the live site, and wires the
  daily flow.
- Post #3 ("Get the news in plain words", approved 2026-11-15, posts to the
  group Mon 2026-11-16 20:00 SGT) joins the blog when it posts.

## Daily flow (to wire once the repo exists)

Each day's approved post goes to the blog the same evening it goes to the
WhatsApp group, as one extra step in the `techkakis-sharing-post` job:
convert the approved text to a `_posts/YYYY-MM-DD-slug.md` file (front
matter: layout post, title, date = that day 20:00:00 +0800, categories
[daily-sharing]; WhatsApp `*bold*` becomes `**bold**`; append the standard
attribution footer used in the backfilled posts), commit with the house
format (Author Chris Lee <chriskslee@gmail.com>, trailer
Co-Authored-By: Seven (Muse)), push via the repo-scoped deploy key.

## Source-of-text notes

- Post #1's text was recovered verbatim from the WhatsApp bridge outbox log
  on Chris's PC (`direct_outbox.jsonl`, entry 958f3941) — the only surviving
  copy. One character is reconstructed: the greeting's emoji was stored as
  "??" by the bridge encoding; rendered here as 👋 (a wave, the natural
  greeting) — flagged to Chris 2026-11-15 for correction if wrong.
- Post #2 uses the exact text Chris approved in the Tech Kakis side chat on
  2026-11-15 (the bridge flattened its em-dashes to hyphens in the WhatsApp
  send; the blog carries the approved version).
