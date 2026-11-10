# Introduction Writing Guide

## Goal

Write a strong introduction in three steps:

1. Think through the introduction logic.
2. Apply a suitable template below.
3. Revise the introduction repeatedly.

## How to Think: Backward First, Then Forward

### Backward reasoning (answer these first)

1. What technical problem do we solve, and why is there no well-established solution?
2. What are the contributions of our pipeline?
3. What are the benefits of our contributions, and what new insight do they bring?
4. How do we use prior methods to lead readers to our solved challenge and insight?

### Forward story (write in this order)

1. Introduce the paper's task.
2. Use prior methods to lead to the technical challenge we solve.
3. Present contributions to solve this technical challenge.
4. Explain technical advantages and explicitly express the new insight.

## Section Skeleton

- Part A: Task and application
- Part B: Technical challenge for previous methods
- Part C: Proposed solution and why it works
- Part D: Additional contributions and impact
- Part E: Experiments

## Part A: Task and Application

### Version 1 (niche task)

1. Define the task in one sentence (what output from what input).
2. Briefly explain the task objective.
3. Introduce application value with 2-3 scenarios.

Skeleton: "[Task] targets recovering [output] from [input]. [Task] has applications such as [A], [B], and [C]."

### Version 2 (familiar task)

1. Skip formal task definition.
2. Open with application importance.
3. Optionally append target requirement.

Skeleton: "[Task] has applications such as [A], [B], and [C]."

### Version 3 (general → specific)

1. Start from the general task and why it matters.
2. Narrow down to the specific setting.
3. Clarify exact input/output and boundary.

### Version 4 (open with challenge)

1. Start with task/application importance.
2. Summarize how representative previous methods work.
3. Expose the unresolved failure case + technical reason.
4. Bridge to prior-work paragraphs.

## Part B: Technical Challenge

Purpose:

1. Discuss around the exact technical challenge we solved.
2. Build reader curiosity.
3. Make motivation clear.

Important warning:

- Do not present a naive solution first and then describe incremental improvement.
- That style makes the work look like a low-score patch and erases reader curiosity.

### Version 1 (existing task, existing methods)

1. Start with a general challenge statement.
2. Briefly summarize traditional methods and their limitation.
3. Briefly summarize recent methods and their limitation with technical reason.
4. Ensure the final limitation is exactly the challenge your method solves.

### Version 2 (existing task, insight-backed)

1. Identify the root cause behind the failure of recent methods.
2. Explain why traditional approaches cannot address this root cause.
3. Lead to the insight that motivates your design.

### Version 3 (novel task)

1. Define the novel task and its value.
2. Explain why existing frameworks do not cover this task.
3. State the core technical challenge.

## Part C: Proposed Solution

1. Introduce the pipeline or method name.
2. Summarize the core idea in one to two sentences.
3. Point to the overview figure if available.
4. List contributions explicitly.

## Part D: Experiments

One paragraph: dataset, baselines, main result, where to find details.

## Quality Checklist

1. Does the introduction make the challenge and solution clear by the end of Part B?
2. Are contributions explicitly listed?
3. Is the method name introduced before it is used?
4. Does every claim in the introduction map to evidence in the experiments?
