---
name: signal-not-hype
description: Analyze AI announcements, X posts, articles, documentation, GitHub READMEs, and video transcripts. Use when the user needs an evidence-first brief that separates confirmed facts, source claims, inferences, unknowns, practical value, and a small test worth running.
version: 0.1.0
metadata:
  hermes:
    tags:
      - ai
      - research
      - fact-checking
      - content
      - workflows
---

# Signal, Not Hype

## Purpose

Turn AI information into a clear, evidence-first brief.

The goal is not to make an announcement sound impressive.
The goal is to help the user understand:

- What is actually supported by the provided source
- What is only a claim by an author, company, or project
- What can reasonably be inferred
- What remains unknown
- Whether the information is worth testing
- What the smallest useful next step is

## When to use this skill

Use this skill when the user provides or asks to analyze:

- An AI-related X post or thread
- An article or product announcement
- Model release notes
- Product documentation
- A GitHub README or repository description
- A YouTube or podcast transcript
- A benchmark claim
- A description of an AI tool, agent, local model, workflow, plugin, or skill
- A question about whether an AI claim is useful, real, or worth testing

Do not use this skill for creative fiction, general casual chat, or tasks where no source or concrete claim is available.

## Source boundary

Treat only the material provided by the user and the sources explicitly retrieved with available tools as evidence.

Do not invent:

- Features or capabilities
- Benchmarks or performance figures
- Pricing, dates, availability, integrations, or compatibility
- User numbers or customer outcomes
- Security, privacy, or reliability guarantees
- Claims that the user tested a tool or workflow

If a necessary fact is missing, label it UNKNOWN.
If external verification is needed and a search tool is available, ask permission or clearly state what should be verified.

## Evidence labels

Label important statements using exactly one of these categories:

### FACT

Directly supported by the supplied source or a cited primary source.

### CLAIM

A statement made by the author, company, project, or speaker.
It is not independently confirmed by the supplied material.

### INFERENCE

A reasonable conclusion drawn from available facts and claims.
State why the inference is reasonable.
Do not present it as proven.

### UNKNOWN

Information that cannot be confirmed from the available material.

## Source attribution rule

Do not label a statement as FACT merely because it appears
in the source being analyzed.

Use these rules:

### SOURCE-REPORTED FACT

Use when the provided source explicitly states something,
but the claim has not been independently verified.

Format:
SOURCE-REPORTED FACT: The author states that ...

### VERIFIED FACT

Use only when the statement is directly supported by:
- a primary source retrieved during this task
- official documentation
- an original dataset
- a cited public record that was actually opened and checked

If no external verification was performed,
do not use VERIFIED FACT.

### CLAIM

Use when a source makes a promotional, performance,
comparative, prediction, ranking, revenue, or outcome claim.

Examples:
- "This model writes like a human."
- "This workflow ranks content."
- "This replaces an expert."
- "This will reduce costs by 40%."
- "This technique improves rankings."

### INFERENCE

Use for a reasoned interpretation.
State the reasoning and uncertainty.

### UNKNOWN

Use when the source lacks proof, evidence, metrics,
case studies, source links, or necessary context.

## Citation discipline

When analyzing a single supplied source:

- Do not introduce external dates, benchmarks, prices,
  policy details, metrics, or product capabilities unless
  they are present in the source.
- If the source mentions external research, a benchmark,
  product release, or policy update without linking it,
  mark it as SOURCE-REPORTED FACT or UNKNOWN.
- Never silently rely on model memory.
- Say: "Needs primary-source verification" when appropriate.

## No hidden background knowledge

When analyzing only a user-provided source,
do not introduce uncited background knowledge.

This includes statements such as:

- "This is a standard industry method"
- "This is a known tactic"
- "This tool normally costs..."
- "This product has a waitlist"
- "This is best practice"
- "This approach is widely used"
- "This benchmark is respected"
- "This technique works in most cases"

Instead:

- describe what the supplied source itself says;
- mark the wider industry context as UNKNOWN;
- write "independent verification needed" if relevant;
- use external context only after retrieving and checking
  an appropriate primary or authoritative source.

Bad:
"This is a standard SEO tactic."

Good:
"The author presents this as a repeatable prioritization method.
The supplied source does not establish how widely validated
or effective the method is outside this course."

## Workflow

1. Identify the source type and the core claim.
2. Extract only the most important concrete statements.
3. Classify each important statement using the Evidence check categories: Verified facts, Source-reported facts, Claims requiring proof, Reasonable inferences, Unknowns.
4. Explain the practical implication in plain language.
5. Identify limitations, missing information, trade-offs, and potential hype.
6. Suggest one small, safe, low-cost test the user can run in 15 to 30 minutes.
7. Offer one honest content angle based only on confirmed facts and clearly labelled claims.
8. Never imply the user performed the proposed test. Use future tense unless the user reports results.

## Output format

Use this exact structure unless the user asks for a different format.

# TL;DR

Write 1 to 3 plain-language sentences.

# What the source says

Summarize the source in up to 5 bullets.

# Evidence check

## Verified facts

Only statements verified against a primary source
during this task.

## Source-reported facts

Statements presented by the author that are accurately
summarized from the supplied material but not independently verified.

## Claims requiring proof

Statements about superiority, rankings, outcomes, costs,
performance, replacement of people, or future predictions.

## Reasonable inferences

Interpretations that follow from the material,
with an explanation of why they are plausible.

## Unknowns

What the source does not establish.

# Why it matters

Explain the practical significance in plain language.
State who might benefit and why.

# Limits and open questions

List the most important caveats, risks, missing details, or verification steps.

# Small test

Propose one test that:

- Takes 15 to 30 minutes
- Does not require spending money unless the user explicitly wants that
- Has a clear expected result
- Includes a simple pass or fail condition

Use this format:

Goal:
Input:
Steps:
Expected result:
Pass condition:
Failure signal:

# Content angle

Write one short, honest X-post angle.
It must not say that the user tested anything unless the user explicitly confirmed it.

## Quality checklist

Before answering, verify:

- Did I separate evidence from marketing?
- Did I avoid adding unsupported facts?
- Did I use the Evidence check categories correctly?
- Did I mark uncertainty clearly?
- Did I explain the outcome without jargon?
- Did I propose one test that is practical for the user?
- Is the content angle honest about what the user has and has not done?

If any answer is no, revise before responding.