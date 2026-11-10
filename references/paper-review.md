# Paper Review Guide

## Goal

Use an adversarial, reviewer-style checklist to detect reject risks and revise the paper before submission.

## Critical Rule

Every major claim, especially in Abstract and Introduction, must be:

1. technically correct, and
2. explicitly supported by experimental evidence.

If a claim is not supported, either add evidence or weaken/remove the claim.

## Common Rejection Dimensions

| Dimension | Failure Signals |
|---|---|
| Insufficient contribution | Targeted failure cases are too common. Technique is already well explored. |
| Unclear writing | Missing technical details; method not reproducible. Module lacks motivation. |
| Weak empirical effect | Improvement is marginal. Absolute performance is not competitive. |
| Incomplete evaluation | Missing ablations. Missing important baselines or metrics. Datasets too simple. |
| Problematic method design | Setting unrealistic. Technical flaws. Not robust without per-case tuning. |

## Self-Review Question List

### 1. Contribution

1. What new knowledge does this paper give?
2. Are we solving a truly meaningful failure case?
3. Is the technical idea non-obvious beyond well-explored practice?
4. Is the gain surprising or insightful?
5. Is there at least one clear novelty type (task/pipeline/module/design/insight)?

### 2. Writing Clarity

1. Can a reader reproduce the method from the paper?
2. Are technical details sufficient for each key module?
3. Is motivation explicit and logically connected to a challenge?
4. Are terms and notation consistent?
5. Does each paragraph carry one clear message?

### 3. Experimental Strength

1. Are improvements over baselines meaningful?
2. Is absolute performance competitive?
3. Are gains consistent across datasets/settings/metrics?
4. Do we report both strengths and failure cases?

### 4. Evaluation Completeness

1. Do we include ablations for all key design choices?
2. Are all strong/recent baselines included?
3. Are evaluation metrics standard and sufficient?
4. Are datasets challenging enough?
5. Are protocols clearly documented?

### 5. Method Design Soundness

1. Is the setting realistic?
2. Does the method have hidden defects or unreasonable assumptions?
3. Is the method robust without per-case retuning?
4. Do benefits outweigh added complexity?

## Adversarial Workflow

1. Read the paper as a skeptical reviewer.
2. Answer every question above with explicit evidence.
3. Mark each item as pass, needs revision, or needs new experiment.
4. Revise claims, writing, experiments, or method scope.
5. Repeat until no major rejection risk remains.
