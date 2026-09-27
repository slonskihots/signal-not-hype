# Signal, Not Hype
> Turn AI claims into testable questions
An evidence-first AI research skill that turns AI claims
into testable questions.

It analyzes AI announcements, X posts, GitHub READMEs,
documentation, articles, model releases, and video transcripts.

Instead of treating confident language as proof,
it separates what a source says from what is actually verified.

## What it does

Give it:

- An AI announcement
- An X post or thread
- A GitHub README
- Product documentation
- A model release note
- An article
- A video or podcast transcript
- A benchmark claim

It returns:

- **Verified facts** — independently confirmed during the task
- **Source-reported facts** — stated by the supplied source but not independently verified
- **Claims requiring proof** — promises about performance, cost, rankings, outcomes, or capabilities
- **Reasonable inferences** — plausible interpretations clearly labelled as unproven
- **Unknowns** — missing evidence and open questions
- **One small test** — a practical 15–30 minute test worth running

## Why

A confident AI claim is not the same as proof.

Signal, Not Hype helps researchers, builders, and creators
decide what is worth testing before repeating a claim.

## Example

### Input

> This agent framework lets you build a fully autonomous company in one hour.

### Output

- **Source-reported fact:** The author says the framework supports persistent agents, tools, scheduling, and memory.
- **Claim requiring proof:** It can build a functioning company in one hour.
- **Unknown:** Reliability, cost, security, error handling, and real customer outcomes.
- **Small test:** Give one agent a single read-only research task and measure whether the result is accurate and repeatable.

## Installation

1. Download or copy the `SKILL.md` file.
2. Add it to any compatible agent environment that supports Agent Skills.
3. Start a new chat and ask:

```text
Use the signal-not-hype skill.

Analyze the following source.
Do not introduce external facts from memory.
Clearly separate verified facts, source-reported facts,
claims requiring proof, inferences, and unknowns.

[Paste source here]
```

## Compatibility

This skill follows the open Agent Skills format.

It is designed for compatible AI-agent environments, including:

- Hermes Agent
- Claude Code
- Other `SKILL.md` / Agent Skills-compatible environments

The core workflow needs only text input.

Optional capabilities depend on the environment:

- Web verification needs a browser or web-search tool
- File analysis needs file upload or file access
- GitHub analysis needs repository or URL access

## Principles

- Evidence over confidence
- Source attribution over unsupported certainty
- Practical tests over generic summaries
- Clear unknowns over invented answers
- Human judgment remains final

## Status

Early version. Tested on AI course and workflow analysis.

Feedback, examples, and improvements are welcome.

## License

MIT
