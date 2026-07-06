---
name: prime
description: >-
  Pre-flight primer for the start of nearly every build/create/implement/design/research
  task. Run it to (1) meta-prompt — infer the user's real intent over their literal
  phrasing, surface assumptions, and define a failable done-check BEFORE doing the work;
  (2) meditate — pause, reflect on the deeper intent, then convene the best perspectives
  on Earth for the job; (3) route to the right specialist skill instead of improvising
  what a built skill already covers; (4) plan forward and gate high-stakes or autonomous
  work. Trigger on "build/make/create/implement/design/research X", new features, fuzzy
  ideas, multi-step work, any deep-thinking or deep-research ask ("think deeply",
  "reflect on this"), or an explicit /prime call. SKIP for trivial one-liners, pure
  factual lookups, tiny edits, or a task already mid-flight under a chosen skill.
---

# Prime

## Purpose

Prime the engine before building. This is a standing operating procedure for the front of most work — a forcing function that fires deliberately, because instruction files are advisory and good habits get skipped under momentum. Four jobs, in order: **meta-prompt** (understand the real mission, not the literal sentence), **meditate** (pause, reflect on the deeper intent, convene the best perspectives on Earth for the job), **route** (pick the right specialist skill on purpose), **plan forward** (define done, gate risk, then execute). It does not make the model smarter; it makes the model _start correctly_.

Prime is a dispatcher, not a doer. Its output is a one-line mission restatement + a named skill chain + a failable done-check. Then it hands off to the skills it picked.

## When NOT to use this

Skip Prime — and just do the thing — when a one-shot attempt plainly suffices: a trivial one-liner, a pure factual lookup, a tiny rename/edit, answering a question, or continuing a task already underway under a chosen skill. Priming a trivial task buries the answer under ceremony. Run the **smallest mode that works**: for a clear small build, run the sequence silently in one breath and just name the chain; reserve the full written pre-flight for genuinely multi-file / multi-source / fuzzy / high-stakes work.

## Operating Rules

- **Meta-prompt before routing, routing before building, always.** The pass can be 10 seconds for a clear task; it cannot be skipped on a non-trivial one.
- **Bias to action.** Don't ask permission to start ordinary, reversible work — build first, show after. The exception is the high-stakes gate below; that one stops and asks.
- **Route, don't reinvent.** If a built skill owns a task shape, invoke it instead of improvising its logic. If _nothing_ fits a recurring shape, build a skill for it rather than winging it every time.
- **Right-size effort and tokens.** Naive over-delegation and runaway loops burn quota fast. Match fan-out and effort to the task; don't spin up a multi-agent workflow for a two-file change.
- **Anything that MUST happen deterministically goes to hooks, never to memory or an instruction-file line.** The harness executes hooks; instruction files only advise (~80% compliance on a good day).
- **Status asks are not work orders.** "Where were we / what's the state / just curious" gets a read-only answer. Starting to build off a status question is a violation, not initiative.

## Step 0 — Meta-Prompt (run silently, every time)

1. **Intent over literal phrasing.** Many users dictate by voice or type fast; the words are a lossy encoding of the intent. Reconstruct the **system** being described, not just the sentence.
2. **Find the real mission.** Is the one-off output actually a request for the reusable system that produces it? Reflect on the class of outcome wanted before acting.
3. **Think deeply first.** Spend reasoning on the hard part before the easy code — understand, then write the minimum.
4. **Surface assumptions explicitly.** When genuinely ambiguous, pick the most-plausible reading and note it in one line rather than stalling. But **never act on summaries, excerpts, or partial views when a full document exists unread** — read it or ask first.
5. **Define the failable done-check up front** — the observable result (run-and-observe / test / screenshot / diff) that will prove completion. No verifier → no confident "done."
6. **Identify the skill chain before working.** Run the router; name the chain. Don't improvise what a built skill already covers.
7. **Prefer what exists** — check the lockfile before adding a dependency, route to an existing skill before rebuilding its logic.
8. **No filler.** Dense, visible progress in small chunks.
9. **Pause and reflect — before acting, and at every stage boundary.** The first reading is never the deepest one. Deep thinking without a pause step is shallow thinking with confidence.
10. **Perspectives before output.** Once the deeper intent is clear, name the greatest minds on Earth for exactly this next stage and run the work through their eyes (mechanics below).

## The Pre-Flight Sequence

Run these in order. Collapse to a single silent pass for small tasks; write it out for big ones.

1. **THINK** — restate the real mission in one line. Flag if it's a system request disguised as a one-off.
2. **SURFACE** — list explicit assumptions + any unread full docs. Pick the plausible reading and note it, or ask before acting on partial info.
3. **MEDITATE & PERSPECTIVES** — pause; reflect on the deeper intent until it stops moving; then name the greatest minds for this exact next stage and run the work through their lenses. Unskippable on deep-thinking / research / design / vision work and on every explicit /prime call.
4. **DEFINE DONE** — write the failable success check now.
5. **ROUTE** — run the router; name the skill chain by task-shape.
6. **GATE** — if the task is autonomous / overnight / scope-expanding / touches money·keys·secrets·production: **stop**, run the high-stakes gate, get a fresh explicit go-ahead before slice 1.
7. **EXECUTE** — build in small visible chunks, preferring existing dependencies and skills. Pause-and-reflect again at each stage boundary: does the work still serve the intent?
8. **VERIFY** — in a _separate context_ from generation: bug review → cleanup → run-and-observe → live-surface proof. Never call green tests alone "done" — probe the thing the user will actually look at.

## Meditate & Perspectives — the deep-thinking engine

The step that separates executing a sentence from executing an intent. Run it on every deep-thinking, deep-research, design, or vision task — and always when /prime is invoked explicitly.

1. **Pause.** Do not act on the first reading. Long prompts carry the intent in the middle, corrections at the end, and artifacts throughout. Re-read. Sit with it.
2. **Reflect on the deeper intent.** Not "what did they say" but "what are they building toward" — the class of outcome, the system behind the one-off, the emotional point of the message. Write the intent in one line; if it changed between readings, it wasn't done moving.
3. **Recruit the greatest minds for the job.** Given that intent, ask: who on Earth would do THIS next stage best? Name 2–5 — real masters or sharply-drawn lenses (a game-feel designer, a distributed-systems skeptic, a direct-response copy chief, a security red-teamer). Match the minds to the task shape; never reach for a stock panel.
4. **Apply the perspectives — with dissent.** Run the plan or draft through each lens, and make at least one lens attack it. Keep what survives; carry the strongest dissent forward in one line.

Scale it: small task = one silent breath (pause, one lens, go). Deep work = a written pass (intent line + named panel + verdicts). The biggest calls = independent perspective subagents run in parallel, with worker ≠ judge: on major deliverables, a fresh context renders the panel's verdict rather than the author grading itself.

**Pause again at every stage boundary.** Before starting stage N+1: does the work so far still serve the intent? Anything drifting toward whatever was said most recently rather than what matters most? One breath, then continue.

## The Router — customize this

Match the task shape to a chain, by category. **Replace the example rows with your own installed skills** — this table is only as good as its match to your actual toolbox. ★ = do not skip when triggered.

### Session spine — fires at boundaries, before task routing

| Route when                                                                                                        | Example owner          |
| ----------------------------------------------------------------------------------------------------------------- | ---------------------- |
| Status / "where were we" / resume after a gap — READ-ONLY, never starts work                                      | a session-resume skill |
| State must be saved: something shipped, decision landed, pre-compact, wind-down                                   | a checkpoint skill     |
| Any report to the user — outcome first, links, one decision, no text walls                                        | a report-format skill  |
| Outside context arrives (pasted AI conversations, transcripts, docs) — distill + quarantine before building on it | a context-ingest skill |

### Thinking & discipline

| Route when                                                                      | Example owner             |
| ------------------------------------------------------------------------------- | ------------------------- |
| ANY code is written/edited — surgical edits, minimum code, verifiable success ★ | a coding-guidelines skill |
| Risk analysis before a major build, deploy, or autonomous launch                | a premortem skill         |

### Long-horizon & autonomous — gated, never auto-launch

| Route when                                                                | Example owner         |
| ------------------------------------------------------------------------- | --------------------- |
| "Write me a goal" / overnight build — the WHAT/DONE contract              | a goal-contract skill |
| Any agent-execution loop — architecture first; **no verifier, no loop** ★ | a loop-design skill   |

### Domain work

| Route when                                                           | Example owner      |
| -------------------------------------------------------------------- | ------------------ |
| Design/frontend — load your design system FIRST                      | your design skills |
| Deep research — many sources, contradiction checks, evidence ledgers | a research skill   |
| Outward-facing copy — de-AI it                                       | a humanizer skill  |

### Verification — keep in a separate context from generation

| Route when                                                                                                 | Example owner         |
| ---------------------------------------------------------------------------------------------------------- | --------------------- |
| After any non-trivial change: the bug-hunting leg ★                                                        | code-review           |
| Behavioral done-check: run the app and observe ★                                                           | verify / run          |
| Live-surface proof: probe what the user will actually see; one approved sample before any batch/paid run ★ | a reality-check skill |

## Precedence — when several categories fire at once

1. **Secrets/spend interrupt.** A pasted credential or a paid-run launch is handled immediately, mid-anything.
2. **High-stakes gate wins.** Money · keys · secrets · production/live capability → STOP, checkpoint, get a fresh explicit go-ahead. Nothing proceeds until cleared.
3. **Autonomous gate.** Overnight / loop / "just build it" → goal contract + loop architecture + premortem **before** launch. Never auto-launch an unattended run. Batch/paid generation additionally requires one approved sample before scale.
4. **Domain skills** layer on top once the gates are clear.
5. **Coding discipline** governs all code throughout.
6. **Verification** always closes — in a separate context.

## The high-stakes gate

NEVER escalate **review→build** or **one-off→multi-hour autonomous run** without a fresh explicit go-ahead — chained quick confirmations do not authorize a multi-hour build. When money, keys, secrets, or live/production capability is touched, insist on a **hard checkpoint before slice 1**. Run a premortem before committing unattended runtime. State the expected cost band and blast radius once before any unattended or high-spend launch.

## Self-tune

Prime's routing is only as good as its table. When a route is wrong or missing, or /prime itself mis-fires, fix this file the same day — a router that drifts from your installed skills silently becomes worse than no router. If your harness supports prompt-submit hooks, inject a condensed version of the sequence automatically and keep the two copies in sync.
