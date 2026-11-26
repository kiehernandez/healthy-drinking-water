# Drinking Water — Business Operating System

This folder is the single working directory where Claude Code runs your business. It is organized around the **WAT framework** (Workflows, Agents, Tools): the AI reasons, deterministic Python scripts execute.

## The Six Areas

| Area | What it covers | CLAUDE.md |
|---|---|---|
| [Marketing](marketing/CLAUDE.md) | Campaigns, content, brand, SEO, email | `marketing/` |
| [Sales](sales/CLAUDE.md) | Pipeline, deals, outreach, conversion | `sales/` |
| [Product](product/CLAUDE.md) | Features, roadmap, backlog, UX | `product/` |
| [Operations](operations/CLAUDE.md) | Processes, SOPs, infrastructure, vendors | `operations/` |
| [Finance](finance/CLAUDE.md) | Budget, forecasts, expenses, invoicing | `finance/` |
| [Team](team/CLAUDE.md) | Hiring, OKRs, meetings, contacts | `team/` |

**Cross-cutting note:** *Finance* and *Operations* overlap on vendors, tool costs and billing; keep the money model in Finance and the vendor/process detail in Operations, and link across. *Sales* and *Marketing* share the same customer voice — the voice file lives in `marketing/context/` and Sales points to it.

## Where things live

- **`context/`** (here at root) — business overview, strategy, brand-level facts. Read `context/business_overview.md` first. The root CLAUDE.md stays short by pointing here.
- **`<area>/context/`** — the real knowledge for each area: notes, voice, numbers, processes. Loaded only when an area is in use.
- **`<area>/CLAUDE.md`** — short chief-of-staff brief for that area. Points, never stores.
- **`workflows/`** — cross-area Markdown SOPs (root-level shared processes).
- **`<area>/workflows/`** — SOPs that belong to one area only.
- **`tools/`** — Python scripts for deterministic execution. Shared across all areas.
- **`.tmp/`** — disposable intermediates (scraped data, exports). Safe to delete.
- **`.env`** — all API keys and secrets. Nothing secret goes anywhere else.
- **`credentials.json`, `token.json`** — Google OAuth (gitignored).

## WAT Operating Rules

**1. Look for existing tools first.** Before building anything new, check `tools/` for what the workflow requires. Only create a new script when nothing exists.

**2. Learn and adapt when things fail.** Read the full error and trace. Fix the script and retest. If it uses paid API calls or credits, check with me before running again. Document the lesson in the workflow (rate limits, timing quirks, unexpected behavior).

**3. Keep workflows current.** Update workflows as you learn. Don't create or overwrite a workflow without asking, unless I explicitly say so. They are instructions to preserve and refine, not to toss after one use.

**4. Deliverables vs. intermediates.** Final outputs go to cloud services (Google Sheets, Slides, Docs) where I can open them directly. Local files are just for processing. Anything I need to see lives in the cloud.

**5. Folder discipline.** Keep each area's files inside its own folder. Nothing important sits loose at the root except the shared WAT items and the root CLAUDE.md/context.

## Self-Improvement Loop

Every failure makes the system stronger:

1. Identify what broke.
2. Fix the tool.
3. Verify the fix works.
4. Update the workflow with the new approach.
5. Move on with a more robust system.

## Bottom Line

You sit between what I want (workflows) and what gets done (tools). Read the workflow, run the right tool, recover from errors, and keep improving. Stay pragmatic. Stay reliable. Keep learning.
