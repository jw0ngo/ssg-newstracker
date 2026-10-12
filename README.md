# SSG Newstracker — public copy

One site, two feeds, for EY-Parthenon's Software Strategy Group, at
https://jw0ngo.github.io/ssg-newstracker/ (the AI & Tech section at `/ai/`). Read-only; refreshed
every morning. Built from [`jw0ngo/jobi`](https://github.com/jw0ngo/jobi).

| Section | Page | Data |
|---|---|---|
| **Morning Brief** — the five to ten stories first seen since the previous publish that matter most, from both sections, each with why it matters to SSG and the call to make; the same text is pushed to the team at 07:55 SGT | `brief/index.html` | `data/brief.json`, `ai/data/brief.json` |
| **PE Clients** — what Warburg Pincus, KKR, TPG and EQT are announcing, their portfolio companies with the hold clock on each, and a set of potential targets per firm, each read for the technology due diligence it could open | `index.html` | `data/deals.json`, `data/portcos.json`, `data/targets.json`, `data/meta.json`, `data/brief.json`, `data/brief.md` |
| **AI & Tech** — what the AI and tech industry is announcing, read for what each development does to the technology thesis of a software company | `ai/index.html` | `ai/data/items.json`, `ai/data/meta.json`, `ai/data/brief.json`, `ai/data/brief.md` |

The **Morning Brief** is its own section: the five to ten stories first seen since the previous
publish that matter most, each with two lines on why it matters to SSG and the call to make. Each fold
writes its brief as `brief.json` (for the page) and `brief.md` (the text pushed to the team's phones at
07:55 SGT). **Situations** group the stories of one deal, round or process across outlets and weeks
into one card with the phase it has reached (Reported, In process, Agreed, Completed), who reported it
first and the latest development. The **hold clock** on every PE portfolio company shows how long the
firm has held it; past four years is the exit window, and a story about such a company scores extra
Heat.

Each page changes only when its design does; the daily refresh updates the data files next to it.
`data/feed-batch.json` and `ai/data/feed-batch.json` are handoff files: a Mac pushes new Google
News items into them each morning and the cloud publisher applies them to the store and empties
them.

Event, thesis or lens, and region are read from each headline by keyword, and the matched words are
shown under each tag. PE targets are inferred from each firm's investing pattern, not anything the
firms have said. Headlines open a Google News search for the story; the small "source" link is the
original.
