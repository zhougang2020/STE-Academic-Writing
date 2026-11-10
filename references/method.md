# Method Writing Guide

## Goal

Write the Method section clearly by following this sequence:

1. Answer key method-design questions.
2. Draw a pipeline figure sketch.
3. Write the method section step by step.

## Pre-Writing Questions

Before writing Method, answer: (1) what modules exist, and (2) for each module, what is the workflow, why it is needed, and why it works.

## Method Writing Steps

1. Draw the pipeline figure sketch.
2. Use the sketch to organize Method subsection structure.
3. For each subsection, plan three parts: motivation, module design, and technical advantages.
4. Write module design first to build a concrete backbone.
5. Add motivation and technical advantages afterward.

## Three Elements of a Pipeline Module

### 1) Module Design

- Describe representation/network/data-structure details.
- Describe the forward process: given input → step 1 → step 2 → output.

### 2) Motivation

- Explain why this module is needed.
- Use problem-driven logic: because problem X exists, we design module Y.

Typical openings:

- "A remaining problem is ..."
- "Previous methods have difficulty in ..."
- "However, existing approaches fail to ..."

### 3) Technical Advantages

- Explain why this module has advantage over alternatives.
- Tie advantage to measurable behavior when possible.

## How to Write Module Design

1. Define key structures first (representation, network, data structure).
2. Write forward process in strict execution order.
3. End with output interpretation or purpose.

Skeleton: "We represent ... with ... Given [input], we first ... then ... finally ... This produces [output], which is used for ..."

## Overview Subsection

1. One to two sentences for task setting.
2. One to two sentences for core contribution.
3. If pipeline is novel, point to overview figure.
4. Tell readers what each subsection covers.

## Clarity Check

### Logic-level

After finishing, summarize the Method logic. Check whether it is smooth and easy to follow.

### Paragraph-level

The first sentence of each paragraph should make readers immediately understand what this paragraph is about. One paragraph delivers one message.

### Sentence-level

1. Check whether the motivation of each sentence is explicit.
2. Check sentence-to-sentence flow.
3. Check term consistency.

## Section Skeleton

- Overview
- Section 3.1: [Module 1]
- Section 3.2: [Module 2]
- Section 3.3: [Module 3]
- Implementation Details (optional)

## Checklist

1. Is the forward process of each module clearly described?
2. Does every module have explicit motivation?
3. Are technical advantages stated where applicable?
4. Are all symbols defined before first use?
5. Is notation consistent across subsections?
