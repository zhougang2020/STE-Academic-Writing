---
name: STE-Academic-Writing
description: Write, rewrite, polish, or review CS/AI/ML/IR academic papers with rigorous structure and STE-simplified English. Four modes — Draft (write new sections), Rewrite (restructure logic and flow), Polish (simplify English per STE without changing meaning), Review (check logic, language, terminology, and claim-evidence alignment). Use when drafting or revising Abstract, Introduction, Related Work, Method, Experiments, Discussion, or Conclusion; when polishing English for clarity; or when reviewing a paper before submission.
---

# STE-Academic-Writing

## Overview

This skill combines two complementary frameworks:

1. **Academic writing structure** from Research Paper Writing Skills (based on Prof. Peng Sida's methodology), which provides section-level templates, paragraph logic, claim-evidence alignment, and reviewer-facing presentation.
2. **Simplified Technical English (STE)** principles from ASD-STE100, which remove ambiguity, redundancy, and "AI slop" from prose while preserving technical accuracy.

The result is a writing assistant that produces papers with sound argument structure and clear, direct English — papers that are both reviewer-friendly and reader-friendly.

## Four Modes

### Draft

Write new paper sections from research content. Follow the section guides in references/.

Workflow:

1. Identify the target section (Abstract, Introduction, Related Work, Method, Experiments, Conclusion).
2. Load the matching section guide from references/.
3. Build a mini-outline (3-7 bullets) before writing prose.
4. Write paragraph by paragraph. Each paragraph has one message stated in its first sentence.
5. Apply STE language rules to each sentence as you write.
6. After the section, run reverse outlining to verify flow.

### Rewrite

Restructure existing paragraphs to improve logic, flow, and argument coherence. Preserve the author's claims, evidence, and technical definitions.

Workflow:

1. Read the target text and extract its current outline (each paragraph's message).
2. Identify logic gaps: missing motivation, broken cause-effect chains, unsupported claims.
3. Rebuild the paragraph order and transition structure.
4. Rewrite each paragraph following academic structure rules and STE language rules.
5. Verify that every original claim appears in the revised text.

### Polish

Simplify English expression without changing meaning. Apply STE principles to reduce ambiguity, remove filler, and sharpen sentences. Do NOT alter the author's research viewpoint, technical definitions, experimental conclusions, or logical relationships.

Workflow:

1. Process sentence by sentence.
2. Apply STE language rules (see below).
3. Protect: mathematical formulas, LaTeX markup, citation markers, technical terms with established meanings, and passive voice that follows academic convention.
4. Do not delete necessary technical detail.
5. Do not simplify at the cost of logical precision.

### Review

Check the paper for logic, language, terminology consistency, and academic expression problems. Do not rewrite. Return findings in a structured table.

Workflow:

1. Run claim-evidence alignment check: every major claim in Abstract and Introduction must map to experimental evidence.
2. Run terminology consistency check: the same concept must use the same term throughout.
3. Run STE language review: flag violations (hedge stacks, nominalization, synonym rotation, marketing adjectives, phrasal verbs, run-on sentences).
4. Run section structure review: verify paragraph coherence, transition quality, and section-level logic.
5. Return a table with columns: Category | Location | Issue | Suggestion | Severity (high/medium/low).

## Academic Writing Principles

### Global

1. One paragraph carries one message. State it in the first sentence.
2. Make nouns self-contained. Define new terms before reusing them.
3. Maintain sentence-to-sentence flow with explicit relations: cause, contrast, consequence, or refinement.
4. Iterate with adversarial self-review: read as a skeptical reviewer.
5. Every major claim must be supported by experimental evidence. If unsupported, weaken or remove the claim.
6. Keep terminology stable across the full paper. Do not rotate synonyms for the same concept.
7. Do not present a naive baseline first and then describe incremental improvement. Lead with the challenge the method solves.

### Section-Specific

Load only the section guide you need:

- Abstract: references/abstract.md
- Introduction: references/introduction.md
- Related Work: references/related-work.md
- Method: references/method.md
- Experiments: references/experiments.md
- Conclusion: references/conclusion.md
- Paper Review: references/paper-review.md
- Paragraph flow: references/paragraph-flow.md
- Example bank: references/examples/index.md

### Paragraph Clarity Check

Use this test whenever a paragraph's clarity or flow is in question:

1. Does this paragraph have one explicit message?
2. Does the first sentence state what this paragraph will do?
3. Are all key terms readable without hidden context?
4. Does each sentence connect to the previous one with a clear relation?
5. Run reverse outlining for the section: extract each paragraph's topic sentence and check that it maps to the section thesis.

## STE Language Rules

These rules adapt ASD-STE100 principles for academic English. Academic accuracy, technical rigor, and domain conventions take priority over language simplification. Do not mechanically apply STE dictionary restrictions or sentence-length caps that would compromise technical precision.

### Vocabulary

- Use one name for one thing. Do not rotate "check / verify / validate / confirm" for the same action. Pick one and reuse it.
- Prefer the short common word: start (not begin/commence/initiate), use (not utilize/leverage), help (not facilitate), make sure (not ensure), do (not perform/conduct), show (not demonstrate), also (not additionally/furthermore/moreover), before (not prior to), after (not subsequent to), about (not regarding/concerning).
- No marketing adjectives: seamless, robust, powerful, cutting-edge, effortless, revolutionary, streamlined. If you cannot measure or test the praise, delete it.
- American spelling.

### Verbs

- Prefer active voice: "the model predicts the label" over "the label is predicted by the model." Passive voice is permitted when the actor is unknown or irrelevant, or when academic convention strongly favors it (e.g., "was proposed by").
- A past participle used as an adjective is not passive and is correct: "the gate is closed," "the field is required."
- Prefer simple tenses. Avoid present perfect where simple past works: "we observed" over "we have observed." Exception: present perfect is acceptable when it accurately conveys ongoing relevance.
- No stacked auxiliaries or hedge phrases. Delete: "it is important to note," "it should be noted," "it is worth noting," "please note that," "crucial to understand." Write the point directly.
- Use a verb for an action, not a noun made from a verb: "analyze the data" not "perform an analysis of the data." Watch for nouns ending in -tion, -ment, -ance, -ence before "of."
- No phrasal verbs in formal prose: spin up, dive into, kick off, roll out, look into. Use the single-word equivalent.

### Sentences

- One core idea per sentence. If a sentence tries to do two things, split it.
- Target 20-25 words per sentence as a guideline, not a hard cap. Technical sentences in Method or Experiments may need more words to stay precise. Do not sacrifice precision for brevity.
- Connect related sentences with plain connectors: then, but, thus, as a result, because, however.
- Do not drop articles to compress: write "the model" not just "model," unless the context is standard mathematical notation.
- No semicolons in running prose. Write two sentences instead. Semicolons inside math or code are excluded.

### Nouns

- Multi-word noun compounds: at most three words before hyphenating or restructuring. "the agent task queue priority handler" becomes "the handler that sets task-queue priority."
- Define abbreviations at first use, then use the abbreviation consistently.

### Punctuation

- No em dash in formal academic text. Use a period, or a connector word. Exception: em dashes are permitted in non-technical asides or rhetorical emphasis when the venue style permits.

### Structure

- One topic per paragraph, max six sentences as a guideline.
- Put a condition before its command: "If the gradient vanishes, the model stops learning."

## Recurring Errors to Avoid

These are the most common substitutions from ASD-STE100 that appear in academic prose. Apply them in Polish mode and flag them in Review mode, but do not force them where they conflict with academic convention.

| Do not write | Write | Note |
|---|---|---|
| ensure (v) | make sure | Most common swap in papers |
| however (adv) | but | Cheaper connector, same logic |
| therefore (adv) | thus / as a result | |
| since (conj) | because | "since" can mean time or cause |
| may (v, permission) | can | If optional, use "can" |
| perform (v) | do | "perform an analysis" is nominalization |
| using (v, participle) | use / with | "Using the CLI, run..." hides the actor |
| additionally / furthermore / moreover | also | |
| prior to | before | |
| subsequent to | after | |
| utilize / leverage | use | |
| demonstrate | show | |
| commence / initiate | start | |

## Protected Content

The following must never be altered by any mode:

- Mathematical formulas and LaTeX markup ($...$, $$...$$, \begin{equation}...).
- Citation markers (\cite{...}, [1], (Author, Year)).
- Technical terms with established field meanings (e.g., "gradient descent," "attention mechanism," "cross-entropy").
- The author's research viewpoint, hypothesis, or conclusions.
- Experimental results, metric values, and statistical data.
- Code identifiers and algorithm names.

## Output Contract

When asked to draft or rewrite sections, return:

1. A compact section outline (3-7 bullets).
2. Revised paragraphs with explicit paragraph roles (opening / challenge / method / advantage / evidence / limitation).
3. A short self-review checklist: clarity, flow, terminology consistency, unsupported claims, missing evidence.
4. A claim-evidence map for each major claim: Claim: ... | Evidence: ... | Status: supported / needs evidence.

When asked to polish, return:

1. The polished text.
2. A summary of changes made (what was simplified and why).

When asked to review, return:

1. A table of findings: Category | Location | Issue | Suggestion | Severity.
2. A claim-evidence map for major claims.
3. A terminology consistency report.

## Execution Rules

1. Identify the mode (Draft / Rewrite / Polish / Review) from the user's request.
2. Load only the section guide needed for the current task. Do not load all guides at once.
3. Apply academic structure rules first, then STE language rules.
4. In Draft and Rewrite modes, build a mini-outline before writing.
5. In Polish mode, process sentence by sentence. Preserve all protected content.
6. In Review mode, do not rewrite. Return findings only.
7. After any draft or rewrite, run the paragraph clarity check.
8. Do not fabricate references, experimental results, or technical justification.

## Attribution

This skill integrates methodology from two open-source projects:

- **Research Paper Writing Skills** (MIT License, Copyright 2026 Master-cai): academic writing framework, section guides, and example templates. Based on Prof. Peng Sida's open study notes.
- **ASD-STE100 writing skill** (MIT License, Copyright 2026 kairin): Simplified Technical English rules and recurring-errors reference. The ASD-STE100 standard itself is a registered EU trademark (No. 017966390) of ASD; this skill does not reproduce the standard, only adapts its principles.
