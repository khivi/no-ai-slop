# No AI slop

This skill removes 20+ patterns of AI slop from your writing and it can also help you detect slop as well.

## What it catches

The patterns it detects include:

| Pattern | Smells like |
|---------|-------------|
| Binary contrasts | "It's not X. It's Y." |
| Throat-clearing openers | "Here's the thing..." |
| Faux-insight setups | "What nobody tells you..." |
| Colon reveals | "The best part: it learns." |
| Superficial analysis | "...highlighting the team's commitment" |
| Importance puffery | "marks a pivotal moment" |
| Weasel attribution | "experts agree," "studies show" |
| Fake-strong verbs | "serves as a centralized hub" |
| Synonym cycling | the agent, then the assistant, then the tool |
| Negative listing | "Not a X. Not a Y. A Z." |
| Dramatic fragmentation | "That's it. That's the whole thing." |

It also enforces the fundamentals that make writing good: Lead with the point when it helps, use active voice, untangle hard-to-follow sentences, and prefer concrete numbers over abstractions.

## Install

**Claude Code plugin (recommended).** Installs the skill and keeps it updatable:

```
/plugin marketplace add khivi/no-ai-slop
/plugin install no-ai-slop@no-ai-slop
```

**Manual clone.** Copy the skill into your personal skills directory:

```
git clone https://github.com/khivi/no-ai-slop /tmp/no-ai-slop
cp -r /tmp/no-ai-slop/skills/no-ai-slop ~/.claude/skills/no-ai-slop
```

Either way, `/no-ai-slop` is then available in Claude Code.

## Use

**1. Edit a draft.** Paste it and invoke the skill:

```
/no-ai-slop

[your draft]
```

You get back the edited draft plus a short What changed section. The skill makes the minimum effective edit, then checks its own work against [eval.md](eval.md).

**2. Detect slop.** Ask whether a piece reads as AI:

```
/no-ai-slop is this AI slop?

[the text]
```

You get every pattern it found each with the quoted line.

## Files

1. `skills/no-ai-slop/SKILL.md`: The editing rules and workflow.
2. `skills/no-ai-slop/eval.md`: Pass/fail checks the skill runs on its own edits.

## Credits

Forked from [petergyang/no-ai-slop](https://github.com/petergyang/no-ai-slop), one skill from Peter Yang's personal AI operating system; the full library lives at [Behind the Craft](https://behindthecraft.com). This fork repackages it as an installable Claude Code plugin.

## License

MIT
