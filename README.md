# Tech Kakis — Daily Sharing (blog)

Jekyll site for the Tech Kakis daily sharing posts, live at
https://pikaia.github.io/tech-kakis/ (repo: `pikaia/tech-kakis`, public).
Structure mirrors the Less Obvious blog: minima theme, GitHub Pages native
plugins, no local build step needed.

## Status (2026-11-15)

- LIVE. Repo created by Chris via the `gh` CLI (GitHub admin goes through
  `gh` in the terminal relay, not the web UI — Chris's standing rule).
  First push a8a8f49 from the PC clone (`C:\Users\chris\projects\tech-kakis`)
  by Chris; GitHub Pages enabled on main, path /.
- Canonical repo is the PC clone. Seven's VM copy (`~/workspace/techkakis-blog`)
  is a drafting mirror only — never push from it.
- Daily flow wired into the `techkakis-sharing-post` job: after the group
  post is verified, the same text is added to the blog (see below), committed
  and pushed from the PC over the bridge via the repo-scoped deploy key
  (`C:\Users\chris\projects\keys\tech-kakis-deploy.key`, git remote `deploy`).
- Backfilled: post #1 (2026-11-14) and post #2 (2026-11-15). Post #3
  ("Get the news in plain words", approved 2026-11-15) joins when it posts
  to the group Mon 2026-11-16 20:00 SGT.

## Daily flow

Each day's approved post goes to the blog the same evening it goes to the
WhatsApp group, as one extra step in the `techkakis-sharing-post` job:
convert the approved text to a `_posts/YYYY-MM-DD-slug.md` file (front
matter: layout post, title, date = that day 20:00:00 +0800, categories
[daily-sharing]; WhatsApp `*bold*` becomes `**bold**`; append the standard
attribution footer used in the backfilled posts), write it into the PC
clone over the bridge, commit with the house format (Author Chris Lee
<chriskslee@gmail.com>, trailer Co-Authored-By: Seven (Muse)), push via
the `deploy` remote, and verify the post's live URL returns 200.

## Source-of-text notes

- Post #1's text was recovered verbatim from the WhatsApp bridge outbox log
  on Chris's PC (`direct_outbox.jsonl`, entry 958f3941) — the only surviving
  copy. One character is reconstructed: the greeting's emoji was stored as
  "??" by the bridge encoding; rendered here as 👋 (a wave, the natural
  greeting) — flagged to Chris 2026-11-15 for correction if wrong.
- Post #2 uses the exact text Chris approved in the Tech Kakis side chat on
  2026-11-15 (the bridge flattened its em-dashes to hyphens in the WhatsApp
  send; the blog carries the approved version).
