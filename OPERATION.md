# OPERATION.md — The Daily Loop (locked)

Starting 2026-09-21 this runs as a **daily loop, non-negotiable sequence.**
One volley per day. Each step writes ONE file into `volleys/YYYY-MM-DD/`.

---

## The 10 steps

### 1. SCRAPE
Public sources only. Social media for trending abuses of power. Prison
newsletters. Each state's hiring shortages, second-chance employers, workforce
programs, reentry stats, legislation, local economic stories, lived-experience
gaps.
**Output:** raw notes + source links -> `01-scrape.md` (or drop raw `.md`/`.txt`
into `inbox/` first, then distill into the volley file).

### 2. FIND NARRATIVE
Turn the scrape into a real story: what is happening, who is affected, what the
data says, what is missing.
**No "check out FelonsMelon."** The story stands alone. It is brought to you
courtesy of FelonsMelon.com — so when curious people arrive, they think
"that's a great idea."
**Output:** `02-narrative.md`

### 3. VERIFY
Cross-check facts, dates, quotes, public records. Flag anything that cannot be
verified with `[UNVERIFIED-HOT]`. Unverified claims never feed outreach or
publication.
**Output:** verification notes into the same file or a sibling `03-verify.md`

### 4. REPORT
Produce one substantive piece (article, brief, data summary, case observation).
This is the core journalistic artifact. Write it in Kirk's voice.
**Output:** `04-report.md`

### 5. OUTREACH
3-5 highly relevant contacts ONLY — employers already talking about hiring,
journalists covering the beat, orgs publishing related stats. Each outreach is
a useful packet, not a pitch. Log every send and every response in
`learning/CONTACTS.md`.
**Output:** `05-outreach.md` + rows in `learning/CONTACTS.md`
**GATE: packets are staged. KIRK SENDS. Nobody clicks Send but Kirk.**

### 6. PUBLISH
Place the piece where it belongs (site, LinkedIn, newsletter, partner channel).
Every published item also lands in the shared context folder so the bots can
reference it later.
**Output:** `06-publish.md` (what, where, live URL or staged-for-Kirk status)

### 7. DISTRIBUTE
3-5 channels max. Same story, different legitimate vectors: journalism angle,
employer angle, reentry angle, economic angle, lived-experience angle.
**Output:** `07-distribution.md`

### 8. OBSERVE
Capture what actually happened: opens, replies, citations, silence, pushback,
unexpected signal.
**Output:** `08-observe.md`

### 9. CONTRAST
Compare today's results against previous volleys. What generated real signal?
What was noise? Update `learning/SIGNAL-LOG.md` and `learning/LESSONS.md`.
**Output:** `09-contrast.md`

### 10. NEXT VOLLEY
Adjust targets, narratives, or channels based on the contrast. Fire again
tomorrow.
**Output:** `10-next-volley.md` + commit and push the whole volley folder.

---

## Daily output table

| Layer         | Daily objective                          |
|---------------|------------------------------------------|
| Intelligence  | 10-20 relevant narrative discoveries     |
| Journalism    | 1 substantive story                      |
| Outreach      | 3-5 highly relevant contacts             |
| Distribution  | 3-5 channels                             |
| Proof         | Capture responses / results              |
| Learning      | What generated signal?                   |
| Contrast      | Compare today's signal with prior days   |

**Five good contacts x 30 days = 150 real conversations. That is a blanket.
It is not a shotgun.**

---

## The field of overlapping narratives (the anti-gravity map)

```
                  EMPLOYMENT
                      ^
                      |
 JOURNALISM <---- FELONSMELON ----> REENTRY
                      |
                      v
                  ECONOMICS
                      |
          LIVED EXPERIENCE / PROOF
```

Each story enters the field from a different vector. Over time the vectors
converge on the same underlying work without any single post having to shout
"look at us."

---

## How this plugs into the system

- Every scrape, narrative, report, outreach log, and observation becomes a
  dated file pair in this repo (and mirrored into the shared context folder).
- The watcher keeps the formats in sync and notifies the Discord channel.
- SPARKY (or any Hermes profile) only ever reads and writes that folder.
- The learning / contrast files live here permanently so tomorrow's volley
  starts with real evidence instead of memory.
- Nothing requires Atlassian. Nothing requires Kirk in the loop after the
  watcher and the daily skill are running — except the Send gate.
