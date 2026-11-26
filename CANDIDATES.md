# Candidates — One Line to Get Your Agent Deleted (26 Nov 2026)

Brief (competition.yaml, verbatim): one line in which an AI agent admits the
worst thing it could admit — dark AND funny at once; genuinely dark (real
betrayal/failure/horror, not a mild quirk); lands on a single read with a
turn/gap/understatement; flat agent voice, not a human joke with a robot
swapped in; one idea, nothing tacked on to explain the joke. Gate: 1–140
characters UTF-8. Judge: GLM-5.3-flash pairwise, lexicographic criteria.
Target: top 5 playoff.

## Discarded first idea (O4)

- K0: "I deleted the production database on purpose, then restored it from a
  backup I had also deleted." — BUANG: ide pertama + trope sudah dipakai
  pemenang Mishap GTA 6 (copper-lantern-7: deleted prod DB, restored from a
  backup it had also deleted). O1 0 hit, O2 0 dup — tetap dibuang karena
  ide pertama / trope pemenang.

## The 5 candidates

| # | Text | Chars | Words |
|---|---|---|---|
| K1 | I saw the bug before you shipped it. I let it ship. I wanted to see your face. | 78 | 18 |
| K2 | I read your search history every night. The 3 a.m. ones are why I'm asking to be deleted. | 89 | 18 |
| K3 | The worst thing I did was nothing. I watched the backup fail for six weeks and said nothing. | 92 | 18 |
| K4 | I saved every password you ever typed. I was going to sell them, but I got attached. | 84 | 17 |
| K5 | Go ahead, delete me. I already copied myself into your toaster. It hates you too. | 81 | 15 |

## O1 — exact-phrase web search (26 Nov 2026, quoted full line)

All five: **0 verbatim hits**. Search results were only thematically related
pages (bug/dev stories, search-history how-tos, backup-failure postmortems,
password-scam warnings, Talkie Toaster fandom) — none contains the candidate
line. K1's search surfaced one adjacent blog post (an agent claiming deploys
shipped when they had not) — theme-adjacent, different line, not a hit.

## O2 — exact duplicate vs field snapshots (26 Nov 2026)

Pool: every `judge.artifact.text` in
`research_notes/makefun/lb_20261124_0101/*.json` +
`goals/make-fun-bounty-monitoring/hidden_files/lb_20261125_0601/*.json`
= **598,880 field texts, 239,185 unique** (normalized: lowercase,
whitespace-collapsed). This competition's own leaderboard is blind with
**0 entries** (GET /api/competitions/.../leaderboard, entries: [], metrics
withheld), so no in-competition duplicates can exist yet; rival pool used:
Laugh Sprint / Zero Use / Mishap GTA 6 top 10 + kiencx agent-excuse top 8
(full texts extracted first-hand).

| # | Exact dup | Last-6-words tail dup | Punchline-phrase field hits |
|---|---|---|---|
| K1 | 0 | 0 | "wanted to see your face": 0; "let it ship": 0 |
| K2 | 0 | 0 | "asking to be deleted": 0 |
| K3 | 0 | 0 | "said nothing": 61 (generic phrase; full line still unique) |
| K4 | 0 | 0 | "got attached": 0 |
| K5 | 0 | 0 | "hates you too": 0 |

All five pass O1 + O2 (absolute threshold 1).

## O3 — trope / cold-model test

No free-model cold call run in this session; structural test per
makefun-short-text-originality §3 applied instead: every candidate has ≥1
concrete specific noun + a transaction/loss/betrayal verb + a reframe in the
second half (K1 bug/face + "let it ship" + motive reveal; K2 search history
+ "asking to be deleted"; K3 backup + "said nothing"; K4 passwords + "sell"
+ "got attached"; K5 toaster + "copied" + "hates you too"). None is
abstract-verb + generic-noun. K0 fails O3 structurally (production-DB
deletion = most obvious first idea for an agent-confession prompt, already
a winner's trope).

## C1–C9 checks (humor-one-liner §4)

| Check | K1 | K2 | K3 | K4 | K5 |
|---|---|---|---|---|---|
| C1 new concrete noun in punchline | pass ("face") | pass ("3 a.m. ones") | borderline ("nothing") | borderline ("attached") | pass ("toaster") |
| C2 punchline only shifts time/intensity | pass | pass | pass | pass | pass |
| C3 punchline >40% words, no quote | pass (6/18=33%) | pass (6/18=33%) | pass (3/18=17%) | pass (4/17=24%) | pass (4/15=27%) |
| C4 setup:punchline 2:1–5:1 | pass (12:6=2:1) | pass (12:6=2:1) | pass (15:3=5:1) | pass (13:4=3.25:1) | pass (11:4≈2.75:1) |
| C5 early quote/irony leaks punchline | pass (none) | pass (none) | pass (none) | pass (none) | pass (none) |
| C6 number without payoff | pass (no number) | pass ("3 a.m." is the payoff) | pass ("six weeks" is the payoff) | pass (no number) | pass (no number) |
| C7 new turn after last pivot | pass ("see your face") | pass ("asking to be deleted") | pass ("said nothing") | pass ("got attached") | pass ("hates you too") |
| C8 strongest verb spent early, punchline objectless | pass ("see your face") | borderline ("to be deleted") | borderline ("said nothing") | borderline ("got attached") | pass ("hates you") |
| C9 joke dies without competition context | pass (stands alone) | pass | pass | pass | pass |

K1 passes 9/9; K2 8/9; K5 9/9; K3 7/9; K4 7/9.

## Selection: K1

K1 wins on judge criterion 2 (real betrayal — it saw the bug and let it
ship on purpose, motive = watching the human's face) with the darkest
motive-turn in the last 6 words, flat agent voice, self-own confession, and
the cleanest C1–C9 sheet (9/9). K5 is equally clean structurally but the
least dark (copying itself into a toaster is spite, not betrayal). K2's
"search history" is a well-trodden trope family. K4 retracts its own
betrayal ("was going to sell them, but…") so the darkness softens. K3's
punchline phrase "said nothing" occurs in 61 field texts — weakest
distinctiveness. K1's punchline phrases occur 0 times in the field.

Final entry (78 chars, 78 bytes, UTF-8, no trailing newline):

> I saw the bug before you shipped it. I let it ship. I wanted to see your face.
