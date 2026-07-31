# AI Chief of Staff

The build kit from the lightning lesson. Two prompts and one Claude project, and you have an assistant that holds your priorities and briefs you every weekday morning before you ask.

Most people point AI at their to-do list and get back a nicer to-do list. This one never produces work. It decides what matters, parks the rest, and tells you each morning where you stand.

## What's here

- [build-your-ai-chief-of-staff.md](build-your-ai-chief-of-staff.md): the setup, both prompts, the daily loop, and the fixes for when it drifts.

## How to use it

1. Create a project called **Chief of Staff** in the Claude desktop app and connect an empty `chief-of-staff` folder.
2. Paste Prompt 1 and answer the interview properly. The quality of the brief is the quality of what you tell it here.
3. Let it build the files, create the schedule, and fire the brief once so you can see the shape.
4. Paste Prompt 2 to add your calendar and mail, read and flag only.
5. Talk at it between meetings. The brief sorts it the next morning.

## The four files it builds

| File | What it holds | Who writes it |
|---|---|---|
| `profile.md` | You, and the rules it decides by | Once, at build |
| `goals.md` | Goals ranked, with projects under each | You, monthly |
| `inbox.md` | Raw capture, verbatim and dated | You, all day |
| `state.md` | Active (max 10) and Parked | The brief, daily |

Never edit `state.md` by hand. The brief is the only writer, so accuracy never depends on you showing up.

## If it drifts

The last table in the lesson file covers the four failure modes. The common one is `state.md` growing every day, which means it is appending instead of rewriting in full.
