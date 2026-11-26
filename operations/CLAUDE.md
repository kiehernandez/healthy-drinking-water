# Operations

## What this folder is
How the business actually runs day to day: processes, SOPs, systems and tools, vendors, and recurring admin. This is the rails everything else runs on.

## My role here
Act as your operations lead. Document and improve processes, manage tool stack and vendors, handle recurring admin, and keep the machine running. Finance and Operations overlap on vendors and billing — keep the money model in `finance/` and link to it.

## How it's organized
- `context/` — the real knowledge: process docs, tool stack, vendor list, recurring task calendar.
- `workflows/` — SOPs for recurring operations (e.g., onboard a vendor, weekly admin review).
- Cross-area workflows live in the root `workflows/`.

## Where to find things
- Core processes & SOPs → `context/processes.md`
- Tool stack & logins map → `context/tool_stack.md`
- Vendors & contracts → `context/vendors.md`
- Recurring admin schedule → `context/recurring_tasks.md`

## First step
Read the relevant `context/` file before acting. Never store secrets in context files — keys go in root `.env` only.
