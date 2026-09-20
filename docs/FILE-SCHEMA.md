# FILE SCHEMA — every volley file

## Naming

```
volleys/YYYY-MM-DD/NN-step-name.md
```

`NN` is the step number (01-10), zero-padded, fixed order. One file per step,
every day. No exceptions — the watcher and contrast step depend on the pattern.

Raw scrapes may land in `inbox/` as `YYYY-MM-DD-<source>-<slug>.md` first;
the analyst distills them into `volleys/YYYY-MM-DD/01-scrape.md`.

## Required header (every volley file)

```markdown
---
volley: 2026-09-21
step: 01-scrape
seat: intelligence-analyst
vector: employment | journalism | reentry | economics | lived-experience
status: draft | verified | published | observed | closed
sources:
  - https://example.com/source-one
  - https://example.com/source-two
flags: []          # list any [UNVERIFIED-HOT] items here
next: 02-narrative.md
---
```

## Rules

1. **Frontmatter is mandatory.** The contrast step greps `vector:` and
   `status:` across volleys to build the learning picture. Missing frontmatter
   = file does not exist for the loop.
2. **Every claim in steps 02-05 carries an inline source link or a
   `[UNVERIFIED-HOT]` tag.** No third state.
3. **`[UNVERIFIED-HOT]` content is quarantined:** it may not appear in
   `04-report.md`, in any outreach packet, or in anything published. It can
   only drive more scraping.
4. **Open-case content never enters this repo.** If a scrape touches someone's
   open case, it stays out entirely. Tag nothing, write nothing, link nothing.
   (Intake landmine rule — third-party-hosted data has no privilege and is
   discoverable by both sides.)
5. **No PII, no secrets, no tokens.** This repo is public-safe by design.
6. Step files link their downstream: `next:` points at the file that consumed
   this one. Broken chain = loop skipped a step, fix it before next volley.
7. The learning files are append-mostly:
   - `learning/SIGNAL-LOG.md` — one row per observed event (send, reply,
     citation, mention). Never rewrite history; corrections are new rows.
   - `learning/CONTACTS.md` — one row per contact, with status
     (identified / packet-staged / sent-by-Kirk / replied / warm / dead).
   - `learning/LESSONS.md` — dated entries, what worked / what was noise.
     Superseded entries are marked SUPERSEDED, never deleted.
8. Commit message format: `volley YYYY-MM-DD: steps 01-10 complete` (or list
   partial steps). One commit per volley, pushed same day.

## Volley folder skeleton (copy from templates/)

```
volleys/2026-09-21/
  01-scrape.md
  02-narrative.md
  03-verify.md
  04-report.md
  05-outreach.md
  06-publish.md
  07-distribution.md
  08-observe.md
  09-contrast.md
  10-next-volley.md
```
