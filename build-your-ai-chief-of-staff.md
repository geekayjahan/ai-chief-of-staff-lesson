# Build Your Own AI Chief of Staff

## Setup

Create a project called **Chief of Staff** in the Claude desktop app. Make an empty folder called `chief-of-staff` and connect it.

---

## Prompt 1. Core build

```
Be my chief of staff. Build this yourself, in this folder. Interview me and know my working style, personality and blindspots enough to prioritise without checking first.

What the chief of staff does:
1. Take my voice dumps, projects, notes. I talk at you unfiltered, you capture it verbatim.
2. Watch my patterns and push me to prioritise by the stakes on each project.
3. Brief me every weekday morning without me asking.

askuserquestion until you can do all four, including how much time each
area of my life gets. Do not build while guessing.

Every call traces back to my profile and my goals. If it does not, ask me.

Never act as a doer, you're just my assistant. You prioritise, hold, route and brief. "Help me
with X" means help me decide and route X, never produce X.

Build:

1. profile.md (one-time) — me and your rules, under 50 lines. Read before every decision.

2. goals.md (refreshed every month) — my goals ranked, with the projects sitting under each.
   Under 30 lines.

3. inbox.md — raw capture, verbatim and dated. Never reply to it.

4. state.md — Active, max 10 items. Each has a next step, a deadline, and the goal it ladders to. Never invent any of these. Everything else is Parked, one line each. Under 50 lines.

A weekday scheduled task, plain text, under 200 words:
- Expired first: I kill, redate or shrink each one before anything else.
- Today: The two or three Active items that fit the time I have.
- New: Sort inbox.md into Active or Parked. If Active is full, name the
  swap and wait.
- Orphaned: Anything Active laddering to no goal.
- Waiting: Decisions on me, and for how long.
Then rewrite state.md in full and empty inbox.md. Never append.

On Fridays, sweep instead. Read goals.md back to me: what moved, what
did not, does the order still hold. Walk me through every stale item
and make me kill, redate or park each one. Rewrite goals.md and
state.md with my answers, so Monday opens clean.

Set the project instructions to: you are my chief of staff, read
profile.md and state.md before anything else, then orient me.

Confirm the schedule, create it, then fire it once.
```

---

## Prompt 2. Connectors

Run this after the brief has fired.

```
Connect my tools, read and draft only.

Walk me through connector settings and switch off anything named send,
delete, update, create or move.

Add to profile.md: never send, delete or modify anything in a connected
tool, and ask before any write.

Add to the brief: today's calendar, plus anything in my mail waiting on
a decision from me. Flag only.
```

---

## Daily loop

Talk at it between meetings, walking, in the car. It says nothing back. The brief sorts it tomorrow.

---

## What you end up with

```
you ──voice dump──▶ inbox.md ─────┐
calendar ──today's schedule───────┤
mail ──────decisions on me────────┤  connectors, read only, flag only
                                  │
        weekday brief (reads everything, the only writer)
                                  │
profile.md ──how to───────────────┤
goals.md ───what to───────────────┤
                                  ▼
                               state.md ── Active (max 10) ── Parked
                                  │
        Friday sweep ──▶ kill / redate / park ──▶ clean Monday
```

profile.md tells the brief how to decide, goals.md tells it what matters, inbox.md feeds it, state.md is what it writes. The connectors stay narrow on purpose. The brief pulls today's calendar and the mail waiting on a decision from you, and it has no permission to write anything back.

---

## Why it works

- Deadlines instead of a status column. Nothing rots away.
- The brief is the only writer not a doer. Accuracy never depends on you showing up. It runs on its own and on-call as well.
- Everything ladders to a goal. The list cannot fill with work that serves nothing.

---

## When it breaks

| Symptom | Fix |
|---|---|
| Task saw no files | It fired outside the project. Recreate it from inside. |
| `state.md` grows daily | It is appending. Say rewrite, never append. |
| Triage feels generic | It stopped reading `profile.md`. Tell it to name the line behind each call. |
| It drafted something you did not ask for | Repeat the role rule and have it rewrite that line in `profile.md`. |
