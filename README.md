# Prime

A pre-flight skill for [Claude Code](https://claude.com/claude-code) that makes your AI stop and understand what you actually want — _before_ it starts building.

## The problem

You say something quick and half-formed. The agent runs with your literal words and builds the wrong thing. Or it improvises something one of your other skills already does better. Or it says "done!" because the tests are green, and the feature doesn't actually work when you click it. Or a casual "sure" turns into an hour of unsupervised changes you didn't sign up for.

None of that is a model problem. It's a _starting_ problem. Prime fixes the start.

## What it does

When real work is about to begin, Prime forces four moves:

1. **Understand the real mission.** Intent over literal phrasing. Assumptions said out loud. A concrete "here's how we'll know it worked" check written _before_ any work happens.
2. **Meditate & Perspectives.** Pause — don't act on the first reading. Reflect on what you're actually building toward. Then recruit 2–5 of the best minds on Earth for exactly this task ("how would a game-feel designer see this? a security red-teamer? a direct-response copy chief?") and let at least one of them attack the plan.
3. **Route.** Send the work to the right specialist skill instead of reinventing it mid-conversation.
4. **Gate and verify.** Money, keys, production, overnight autonomous runs → hard stop, explicit go-ahead first. And at the end: verify by probing the real thing the user will look at — never by trusting green tests alone.

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

- **Router table** → your installed skills, your categories. A router that doesn't match your toolbox is worse than none.
- **Trigger phrases** → the things you actually say, in the frontmatter description.
- **High-stakes gate** → define what counts as money/keys/production _for you_.
- **Optional power move**: add a `UserPromptSubmit` hook that injects a condensed version of the sequence on build-shaped prompts, so the discipline fires even when nobody invokes the skill. Keep the hook copy and the SKILL.md in sync.

## Philosophy

- Instruction files are advisory — under momentum, agents comply maybe 80% of the time. A deliberately-fired pre-flight is how good habits survive a fast session.
- The first reading of a prompt is never the deepest one. A pause costs seconds and changes what gets built.
- "Who on Earth would do this next stage best?" produces sharper work than "try harder."
- No verifier, no confident "done."
- Never escalate from review to build, or from one-off to autonomous run, without a fresh explicit go-ahead.

## License

MIT. Attribution appreciated, not required.
