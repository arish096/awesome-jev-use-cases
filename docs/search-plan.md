# Search plan: how people will find this repo

Built 2026-09-20 from treg keyword data, Google autocomplete, live results pages and YouTube and X activity. See [keyword-research.md](keyword-research.md) for the numbers.

## The main problem

"Jev" alone is a poor search term. Google's autocomplete for "jev" suggests Jevons paradox, Jevil from Deltarune and Japanese encephalitis. Searchers who mean the AI model will add a word, or land through a video, an X post or a link. So the repo title, description and first paragraph must say "TypeSafe" and "AI model" next to "Jev".

## Predicted searches, by stage

| Stage | Likely query | Where this repo answers it |
| --- | --- | --- |
| Now (launch) | typesafe jev, jev ai model, what is jev typesafe | FAQ and What Jev is |
| Now | awesome jev, jev github, jev projects, jev repos | Open source, Long tail, data/repos.csv |
| Now | jev demos, jev examples, jev use cases, what can you build with jev | Top 30 demos, Browse by area |
| Next 1 to 2 weeks | how to use jev, jev tutorial, jev api example, jev curl | docs/api-quickstart.md |
| After Sept 25 | jev pricing, jev free, jev cost | Reported cost and latency |
| Later | jev vs llm, jev limitations, jev accuracy | FAQ, Limits of Jev 1.13 |
| Later | claude code router jev, llm router jev, llm as a judge jev | Open source (routers), Patterns |

Google's autocomplete has no suggestions yet for "awesome jev" or "jev examples" (checked 2026-09-20). Phrases with no suggestions are open ground.

## What is set in this repo

| Element | What it does |
| --- | --- |
| Repository name | Contains "awesome", "jev" and "use-cases", which match the three most likely words. |
| H1 in README | Names TypeSafe AI, Jev, demos, repos, limits and examples. |
| GitHub description | Written to read well in a search result and to include the exact phrases above. |
| Topics | 20 topics: jev, typesafe, typesafe-ai, system-one, llm, llm-router, ai-router, llm-as-a-judge, ai-guardrails, claude-code, mcp, awesome, awesome-list and others. |
| FAQ section | Question and answer pairs with sources. Search engines and AI assistants quote this format. |
| docs/api-quickstart.md | Targets "jev api", "jev curl" and "how to call jev". |
| llms.txt | A plain index for AI crawlers and assistants. |
| CITATION.cff | Lets GitHub show a "Cite this repository" button. |
| Data CSVs | Other people link to and reuse data, which brings links back. |

## Ways to grow beyond this

1. Stars and links matter most for GitHub ranking. Get listed in other awesome-Jev lists. An issue is open with one of them: https://github.com/sontakey/awesome-jev/issues/3.
2. Post the numbers on X and Hacker News, with the repo link. Draft: "74 Jev demos ranked by likes: the median builder has 6.6k followers."
3. Publish one tutorial for "claude code router" on a blog or dev.to, and link to the repo.
4. Add a GitHub social preview image in repository settings, since it cannot be set from the command line. Use `assets/banner-v3.png`.
5. Turn on GitHub Pages for the docs folder if you want a page that ranks outside GitHub.
6. Refresh the numbers weekly so the "snapshot" dates stay current. Old snapshots lose trust.
7. Reply with the repo link when someone on X or YouTube asks "what can I build with Jev".

## What not to do

- Do not stuff keywords. GitHub and Google both demote it, and readers notice.
- Do not claim the list is official or that Jev beats other models. Keep the limits section prominent.
