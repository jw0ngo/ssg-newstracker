# SSG Newstracker — public copy

One site, four sections, for EY-Parthenon's Software Strategy Group (SSG), Singapore, at
https://jw0ngo.github.io/ssg-newstracker/. Read-only; refreshed every morning. Built from
[`jw0ngo/jobi`](https://github.com/jw0ngo/jobi), whose `docs/ssg-newstracker/` playbooks describe
how each section is produced and changed.

| Section | Page | Data |
|---|---|---|
| **AI Impact** — a force map of the tracked sponsors, the sectors they are buying into and the companies on the roster, with an AI-impact read (tailwind, mixed, headwind) and diligence questions per sector | `impact/index.html` | `impact/data/impact.json` |
| **Morning Brief** — the Monday weekly brief for the SSG APAC team, then the day's five to ten stories from both feeds, each with why it matters and the call to make; the daily text is pushed to the team at 07:55 SGT | `brief/index.html` | `brief/data/weekly.json`, `data/brief.json`, `ai/data/brief.json` |
| **Exit Readiness Tracker** — nine sponsors' portfolio companies in Asia-Pacific (outside India and mainland China) on sector boards, a column per country, ordered by time held with the hold shown block by block from grey to red, stake and exit status tagged, and each company's latest headlines a tap away | `index.html` | `data/portcos.json`, `data/deals.json`, `data/targets.json`, `data/meta.json`, `data/brief.json`, `data/brief.md` |
| **AI & Tech** — the transactions side of AI and software: M&A, companies in play, sponsor moves, listings that set comps and the platform shifts that change what a target is worth, APAC first | `ai/index.html` | `ai/data/items.json`, `ai/data/meta.json`, `ai/data/brief.json`, `ai/data/brief.md` |

Sponsors tracked: Warburg Pincus, KKR, TPG, EQT, Navis Capital, TA Associates, Macquarie Capital,
Affinity Partners, Affinity Equity Partners.

The **Morning Brief** is its own section: the five to ten stories first seen since the previous
publish that matter most, each with two lines on why it matters to SSG and the call to make. Each fold
writes its brief as `brief.json` (for the page) and `brief.md` (the text pushed to the team's phones at
07:55 SGT). **Situations** group the stories of one deal, round or process across outlets and weeks
into one card with the phase it has reached (Reported, In process, Agreed, Completed), who reported it
first and the latest development. The **hold clock** on every PE portfolio company shows how long the
firm has held it; past four years is the exit window, and a story about such a company scores extra
Heat.

Each page changes only when its design does; the daily refresh updates the data files next to it.
`data/feed-batch.json` and `ai/data/feed-batch.json` are empty handoff files kept for compatibility;
the feeds are pulled by the cloud publisher itself.

Event, thesis or lens, and region are read from each headline by keyword, and the matched words are
shown under each tag. PE targets are inferred from each firm's investing pattern, not anything the
firms have said. Headlines open a Google News search for the story; the small "source" link is the
original.
