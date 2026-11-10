# Experiments Writing Guide

## Goal

Convince reviewers with complete evidence on effectiveness, causality, and practical value.

## Three Core Questions

1. Is the method better than strong baselines?
   - Compare against strong and recent baselines.
   - Report standard metrics on the main benchmarks.
   - Include SOTA or strongest public methods.
   - Keep protocol fair (same data split, preprocessing, evaluation settings).

2. Which modules/design choices make the gain?
   - Run ablation studies for each key module.
   - Use remove/replace/disable variants.
   - Include component interaction ablations when modules are coupled.

3. How far can the method generalize?
   - Run evaluations on harder or out-of-distribution settings.
   - Add stress-test scenarios.
   - Report both gains and failure modes.

## Section Structure

1. Experimental Setup
2. Main Results (comparison with baselines)
3. Ablation Studies
4. Qualitative Results / Analysis (optional)

## Figure and Table Rules

### Hard rules

1. Put caption above the table.
2. Avoid vertical lines in tabular columns.
3. Use booktabs style (\toprule, \midrule, \bottomrule).
4. Use as few horizontal rules as possible.
5. Highlight key numbers with subtle emphasis.

### Readability rules

1. Label metric direction in column headers (e.g., PSNR ↑, LPIPS ↓).
2. Add units when needed.
3. Align text columns left; numeric columns consistently aligned.
4. Keep numeric precision consistent within a metric column.
5. Group multi-dataset results using \multicolumn + \cmidrule.
6. One table, one message.
7. Keep caption focused on setting/protocol/notation, not long discussion.

## Experimental Rigor Checklist

1. Are baselines recent and relevant?
2. Are metrics sufficient and standard for this task?
3. Is ablation tied to every key design claim?
4. Are claims in Abstract/Introduction supported by reported numbers?
5. Are limitations of evaluation scope explicitly stated?
