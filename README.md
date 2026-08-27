# Hi, I'm Ricky 👋

I lead AI adoption at a listed company — in practice that means I'm the whole team:
strategy, build, rollout, and the awkward conversations with the security reviewers.
A fair amount of it I'm still figuring out as I go.

What I keep coming back to is the **agent harness**: the layer around the model rather
than the model itself. Scheduling, memory, skills, evaluation, guardrails.

My working hypothesis, still being tested, is that model capability stopped being the
bottleneck a while ago — and that what holds adoption back inside a company isn't the
model not being smart enough, but the layer around it not being reliable enough yet.

## What I'm trying to figure out

- **Getting agents into environments that hold secrets.** Sandbox boundaries, permission
  matrices, approval interrupts, and the paths that quietly escalate privilege.
- **Making token cost predictable.** Tiered routing, context compression, and reasoning
  budget allocated by task complexity.
- **Letting legacy systems absorb AI.** Twenty years of process and data don't get a
  rewrite. The agent has to meet them where they already are.
- **Making outcomes measurable.** Without evals there's nothing to iterate against, and
  as far as I can tell that's where most enterprise AI efforts quietly stall.

## Open source

I contribute mostly around **guard boundaries and data integrity** — less "add a feature",
more "where can this be bypassed, where does it hang, where does it drop data without
saying so". It's slow work that doesn't demo well, but it's the part I find most
interesting, and I learn a lot from the reviews.

| Area | |
| :--- | :--- |
| Command execution guards | privilege and wrapper prefixes, path handling, option parsing |
| Checkpoint & rollback | making "restored" actually mean restored |
| Sandbox & network policy | proxy interference, honest network posture reporting |
| Gateway access control | isolation and addressing across profiles |
| Runtime resilience | idle timeouts, session state reclamation, health checks |
| Config & CLI | lossless parsing, consistent key validation |
| Web UI & i18n | rendering, form state, integration tests, locale catalogs |

**[OpenSquilla](https://github.com/opensquilla/opensquilla)** — token-efficient microkernel
agent. A local router sends each turn to the cheapest model that is good enough, which maps
directly onto the constraint I keep running into at work.
→ [my pull requests](https://github.com/opensquilla/opensquilla/pulls?q=is%3Apr+author%3ARickyYii)

**[Hermes Agent](https://github.com/NousResearch/hermes-agent)** — self-improving agent with
a built-in learning loop; it generates skills out of its own usage and keeps iterating on
itself.
→ [my pull requests](https://github.com/NousResearch/hermes-agent/pulls?q=is%3Apr+author%3ARickyYii)

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat&logo=modelcontextprotocol&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
![Vue](https://img.shields.io/badge/Vue-4FC08D?style=flat&logo=vuedotjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat&logo=supabase&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat&logo=cloudflare&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)

Also reach for React, Tailwind, Swift, SQLite, pandas, NumPy, Vercel, Stripe, Power BI and
Streamlit depending on what the problem needs.

## Say hi

Open an issue or a discussion. Always happy to compare notes on harness design, evals, or
getting an agent past a security review — I learn as much from other people's answers as
from my own.

<!--
Profile README — GitHub renders this at the top of github.com/RickyYii because the
repository name matches the username. Edit and push; it updates live.

Kept deliberately non-specific: the "my pull requests" links stay current on their own,
so new contributions need no edit here.

Left out: real name, location, employer name, contact details, private work, and the
security advisory (add that once the reporter credit is accepted and public).
-->
