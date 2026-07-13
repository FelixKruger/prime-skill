# Prime

A skill for [Claude Code](https://claude.com/claude-code) that changes how AI agents think about your work — not just what they build, but whether they understood what you actually meant before they started.

## What people are saying

> "This saved me literally three months of work. I had a plan for a project that was going to take that long — and with Prime, it got it right on the first try. The difference was that the AI actually understood what I was building before it started coding."
> — _Engineer, early adopter_

> "This skill let me push Frontier models beyond the usual limits. For the first time it felt like a senior co-worker rather than an agent I was prompting. It felt like sending off a team lead to solve what I set it out to do rather than having to check back every few minutes."
> — _[Andreas Wissel](https://linkedin.com/in/andreaswissel), CTO @ Willidrop_

These aren't cherry-picked marketing quotes. These are people who installed a single file and watched the way their AI agent works fundamentally change.

## Why it matters

Most people's experience with AI coding agents follows the same pattern: you say something, the agent runs with your literal words, and you spend the next hour fixing what it built — or worse, you don't notice it missed the point until much later.

The problem isn't the model. The model is brilliant. The problem is that nobody taught it to _stop and think_ before it starts building. To ask: what are you actually trying to accomplish here? Is the thing you asked for actually the thing you need? Who on Earth would be the best mind to approach this specific problem?

That's what Prime does. It's a cognitive framework — a structured way of thinking that fires before every significant task and transforms how an AI agent approaches your work.

## How it works

When real work begins, Prime forces the agent through four moves:

### 1. Understand the real mission

Not your words — your _intent_. Voice-to-text garbles things. Quick messages leave out context. Everyone says "build X" when they mean "build the system that produces X." Prime reconstructs what you're actually after, says its assumptions out loud, and defines a concrete "here's how we'll know it worked" check — all before a single line of code.

### 2. Meditate & Perspectives

This is the move that changes everything. The agent pauses. It doesn't act on its first reading. It reflects on what you're actually building toward — the deeper intent behind the request. Then it asks: _who on Earth would do this next stage best?_

It recruits 2–5 of the sharpest minds for exactly this problem — a distributed-systems architect, a game-feel designer, a security red-teamer, a direct-response copy chief — whatever the task demands. Real masters matched to the real shape of the work. And at least one of them attacks the plan.

This isn't a gimmick. It's the difference between an agent that executes your sentence and an agent that executes your vision.

### 3. Route

If you've built other skills, Prime sends work to the right specialist instead of reinventing it mid-conversation. A coding-guidelines skill for code, a design skill for UI, a research skill for deep dives. It's the dispatcher that makes your whole skill ecosystem work as one system.

### 4. Gate and verify

Money, API keys, production deploys, overnight autonomous runs — hard stop, explicit go-ahead required. And when the work is done: verify by probing the real thing you'll look at, not by trusting green tests alone.

## The deeper pattern

The reason Prime produces results like "saved three months" isn't any single move. It's the compound effect:

- **The pause prevents the wrong start.** Most wasted time in AI-assisted work comes from the agent confidently building the wrong thing. One moment of reflection eliminates hours of correction.
- **Perspectives catch what you'd miss alone.** Your prompt carries your blind spots. Running the work through multiple expert lenses — with at least one skeptic — surfaces problems before they become expensive.
- **The stage-boundary re-pause prevents drift.** Even when the start is right, agents drift toward whatever was said most recently rather than what matters most. Prime re-checks intent at every stage boundary.
- **Verification closes the loop.** "Tests pass" and "the feature works" are different statements. Prime insists on probing the real surface — what the user will actually see and touch.

## Setup — just let your AI do it

Paste this into Claude Code (or any coding agent with file access):

```text
Install the "Prime" pre-flight skill:
1. Download https://raw.githubusercontent.com/FelixKruger/prime-skill/main/SKILL.md
   and save it to ~/.claude/skills/prime/SKILL.md (create the folder if needed).
2. Confirm the skill is registered.
3. Then customize it for me: look at the skills I actually have installed, replace
   the example rows in the "The Router" section with them, and add trigger phrases
   I actually use to the frontmatter description.
```

That's the whole install. Step 3 is where it gets good — Prime ships as a template, and it starts earning its keep the day the router names _your_ skills.

<details>
<summary>Manual install</summary>

```bash
mkdir -p ~/.claude/skills/prime
curl -o ~/.claude/skills/prime/SKILL.md \
  https://raw.githubusercontent.com/FelixKruger/prime-skill/main/SKILL.md
```

Then edit the router table and description to match your setup.

</details>

## Using it

- **`/prime <task>`** — run the pre-flight explicitly on anything.
- **Auto-fire** — the skill's description triggers on build/create/design/research phrasing and deep-thinking asks ("think deeply", "reflect on this").
- **Small tasks stay fast** — Prime runs silently in one breath for clear small work and writes out the full pre-flight only for big, fuzzy, or high-stakes tasks. Trivial one-liners skip it entirely.

## Make it yours

Prime is a framework, not a prescription. Customize it:

- **Router table** — your installed skills, your categories. A router that doesn't match your toolbox is worse than none.
- **Trigger phrases** — the things you actually say, in the frontmatter description.
- **High-stakes gate** — define what counts as money/keys/production _for you_.
- **Optional power move** — add a `UserPromptSubmit` hook that injects a condensed version of the sequence on build-shaped prompts, so the discipline fires even when nobody invokes the skill. Keep the hook copy and the SKILL.md in sync.

## Philosophy

- Instruction files are advisory — under momentum, agents comply maybe 80% of the time. A deliberately-fired pre-flight is how good habits survive a fast session.
- The first reading of a prompt is never the deepest one. A pause costs seconds and changes what gets built.
- "Who on Earth would do this next stage best?" produces sharper work than "try harder."
- No verifier, no confident "done."
- Never escalate from review to build, or from one-off to autonomous run, without a fresh explicit go-ahead.

## Try it, break it, make it better

Don't take anyone's word for it — install it, run it on your next real task, and see what happens. If it changes your workflow the way it changed theirs, great. If it doesn't, that's useful too.

**Share what happened.** Open an [issue](https://github.com/FelixKruger/prime-skill/issues) or start a [discussion](https://github.com/FelixKruger/prime-skill/discussions) — what worked, what didn't, what you changed. The best improvements to Prime have come from real people hitting real problems with it. A skill like this gets better every time someone runs it on a task shape the original author never imagined.

Pull requests welcome — especially router patterns for skill ecosystems different from mine, trigger phrases that catch real intent better, or refinements to the Meditate step from domains where I have no expertise.

## License

MIT. Attribution appreciated, not required.
