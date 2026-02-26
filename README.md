# Vantage Point Ma

A methodology for when iteration makes things worse instead of better.

## The Problem

You asked Claude to improve something. It got longer. You tried again—more elaborate, still not right. You added detail, gave examples, rephrased. Each pass drifted further from what you wanted.

You've tried better prompts. This isn't a prompting problem.

## What This Is

A Claude Skill for the iteration process itself. Not how to write prompts, but what to do *between* prompts when you're refining output.

Most advice assumes iteration is neutral—just "keep trying until good." But iteration has methodology, and bad methodology compounds with each pass.

This skill creates intentional gaps between generation and analysis using tool-enforced file separation. The gap is where seeing happens.

## When To Use This

- Output gets longer but not clearer with each revision
- "Improve this" produces different but not better
- Self-analysis sounds right but nothing changes
- You can explain why it's good but it doesn't feel good
- Iteration feels like spinning, not progress

## How It Works

Writing "let me stop and analyze" while continuing to generate is like miming a pause—the words describe stopping, but the stream continues.

Using file operations to separate phases creates actual cognitive breaks where different patterns can emerge.

**The Loop:**
```
ANCHOR      →  Genuine question or constraint
GENERATE    →  First pass to file (no self-editing)
DISTANCE    →  Read back with view tool
ANALYZE     →  Feedback to separate file
READ        →  View analysis before next pass
REFINE      →  Generate new version
REPEAT/STOP →  From internal sense, not quota
PACKAGE     →  Archive for pattern tracking
```

## Requirements

This skill requires **computer use / file creation** to be enabled in Claude.

Required tools:
- `create_file` — writing outputs and analyses to separate files
- `view` — reading back files to create distance
- `bash_tool` — packaging and timestamps
- `web_search` — filling knowledge gaps during analysis (when available)

## Installation

1. Download [`SKILL.md`](./SKILL.md) from this repo
2. Go to [claude.ai/settings/capabilities](https://claude.ai/settings/capabilities)
3. Under Skills, click "Upload skill"
4. Upload the SKILL.md file (or zip it in a folder first)

## Why It Works

Research on LLM self-correction finds that self-generated feedback alone often doesn't improve output—and can make it worse. External feedback is what reliably helps.

This skill addresses that in two ways:
1. Tool separation creates actual distance, not performed reflection
2. The skill is scaffolding for user feedback, not a self-contained engine

## Signs It's Working

- Later passes are shorter, not longer
- You're removing more than adding
- Assumptions surface that were invisible before
- Surprise happens—you didn't plan what emerged

## Signs It's Not Working

- Passes get more elaborate
- Structure becomes clever
- It wraps up neatly
- Questions feel decorative

## The Name

**Vantage Point** — a position that gives perspective.

**Ma (間)** — Japanese concept of meaningful pause. The space between notes that lets music breathe. Musicians call this "the pocket."

## Related

This skill focuses on iteration methodology. For prompting techniques:
- [Anthropic Prompt Engineering Docs](https://docs.anthropic.com/claude/docs/intro-to-prompting)
- [Prompt Engineering Guide](https://github.com/dair-ai/Prompt-Engineering-Guide)

## License

[MIT](./LICENSE)

---

*This skill was developed through its own methodology—using VPM to refine VPM.*
