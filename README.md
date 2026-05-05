# Daily Question Prompt

A prompt that makes your AI agent ask you one project-relevant question per day instead of sending summaries you'll never read.

## The Problem

You gave your agent access to your project docs, maybe even set up a daily summary. But summaries are passive. You skim them, you archive them, you forget them. Nothing moves forward.

## The Fix

Schedule your agent to ask you ONE question per day. Based on what it reads in your project files, it picks something that's unclear, overdue, or worth researching. You have to respond. That response gets logged and feeds into the next question.

A notification vs. a conversation. One you ignore, the other you engage with.

## What It Does

The prompt rotates through three question types:

1. **Clarification** — something in your docs is ambiguous or incomplete
2. **Research Nudge** — the agent found something relevant (a competitor, paper, tool) and asks if you're aware
3. **Decision / Follow-up** — a next step is unclear or a deadline is approaching

Every Q&A pair gets appended to a `questions.md` file, so the agent never repeats itself and you build up a decision log over time.

## Setup

1. Copy the contents of [`prompt.md`](prompt.md)
2. Replace `[PROJECT_NAME]` with your project name
3. Point the agent at your project folder (it needs read/write access)
4. Create an empty `questions.md` in your project root
5. Schedule the prompt to run daily (or whatever interval you prefer)

The prompt expects your project to have some form of documentation it can read: a concept doc, a plan, meeting notes, an inbox folder. It doesn't need a specific structure, just something to work with.

## Works Well For

- Solo projects where decisions live in your head too long
- Small teams (2-3 people) as a lightweight async standup
- Research projects where open questions accumulate faster than you address them
- Any project with docs that nobody re-reads after writing them

## Requirements

- An AI agent with file access and scheduling capability (Claude with Cowork/Scheduled Tasks, custom agent setups, etc.)
- A project folder with at least some written documentation
- A `questions.md` file for the agent to log Q&A pairs

## License

MIT — use it however you want.
