# Operation SnowStrike

**Goal: 100 active users on felonsmelons.com by December 25, 2026.**

**Hard date: October 1, 2026** — narratives solid, Stripe solid. We harden until then.

**Tagline (locked):**
> Don't chase attention. Create enough legitimate signal that attention has somewhere to land.

**Daily principle (locked):**
One story. Several legitimate vectors. No spam. Measure everything. Fire again tomorrow.

---

## What this repo is

The strike team's operations base. Every day runs the same 10-step loop (see
`OPERATION.md`). Every scrape, narrative, report, outreach log, and observation
becomes a dated file in `volleys/YYYY-MM-DD/`. The learning files in `learning/`
are permanent — tomorrow's volley starts with real evidence, not memory.

Nothing here requires Atlassian. Nothing requires Kirk in the loop except the
one human gate: **nobody sends outreach except Kirk.** We stage the packets; he
clicks Send.

## Repo map

```
OPERATION.md        <- the locked 10-step daily loop + output table
TEAM.md             <- the five seats and who owns what
docs/FILE-SCHEMA.md <- file naming + metadata for every volley
docs/DAILY-SKILL-PROMPT.md  <- the exact prompt any Hermes profile runs daily
docs/CHANNELS.md    <- the 5 legitimate distribution vectors
docs/FUNNEL.md      <- the math: 100 users by Dec 25
templates/          <- copy-paste starters for every volley step
inbox/              <- raw scrapes land here first (.md or .txt)
volleys/            <- one dated folder per day, 10 files each
learning/           <- SIGNAL-LOG.md, CONTACTS.md, LESSONS.md (permanent)
```

## The rules that never bend

1. Public sources only in scrapes. Source links always included.
2. Stories stand alone. No "check out FelonsMelon." The byline is
   "Brought to you courtesy of FelonsMelon.com" — curiosity does the rest.
3. Unverifiable claims get flagged `[UNVERIFIED-HOT]` and never feed outreach.
4. Open-case content NEVER enters this repo. Local-only, per the intake landmine rule.
5. No PII. No secrets. No tokens. This repo is public-safe.
6. Outreach is a useful packet, never a pitch. 3-5 contacts max per day.
7. 3-5 channels max per story. Same story, different legitimate vectors.
8. Kirk sends. We stage.
