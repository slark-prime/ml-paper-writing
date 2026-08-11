# Part VII — Strategic Selection, Mixed Results, and Writing Quality

## Contents

1. Editorial selection license
2. Unfavorable-result routing
3. Comparison reframing and fairness
4. Claim-calibration ladder
5. Non-defensive writing
6. Explicit advantages and strong scientific wording
7. Generic AI-prose removal
8. Compression order
9. Reviewer-objection repair layers

## 1. Editorial Selection License

The agent should be assertive about what the paper is.

### In the main text, it is acceptable to

- lead with the strongest supported regime and result;
- select representative datasets/tasks when the full grid is redundant;
- aggregate secondary settings while exposing meaningful heterogeneity;
- choose examples that best teach the idea, with the selection rule stated;
- center a meaningful non-SOTA axis such as cost, assumptions, calibration,
  coverage, workflow, or corrected understanding;
- omit unsuccessful explorations and abandoned design chronology;
- compress results that do not change a central claim;
- place full tables and secondary checks in the appendix;
- use a memorable title, contrast, and direct positive framing.

### The main-text selection should leave an audit trail

When only a subset is shown, state the organizing rule and provide material full
results in the appendix or repository. Examples:

- `We show four representative task families in the main text and report all 23
  tasks in Appendix B.`
- `Figure 5 uses a stratified sample of successful and failed trajectories; the
  aggregate failure rates appear in Table 3.`
- `The main plot reports the quality–latency frontier; exact per-model values are
  tabulated in Appendix D.`

Do not make the paper look comprehensive by placing every result in the main
text. Make it complete with respect to the thesis.

## 2. Unfavorable-Result Router

### Class A — Material to the headline claim

Examples:

- a protocol-matched standard baseline defeats the method on the claimed axis;
- a mechanism experiment contradicts the mechanism claim;
- the theorem assumption fails in the stated application;
- a deployment cost reverses practical superiority;
- a subgroup result changes a population-level conclusion.

Action: report it, then revise the claim, proof module, comparison class, or
paper story. Do not bury it.

### Class B — Meaningful trade-off or scope boundary

Examples:

- higher accuracy with increased latency;
- gains concentrated in low-data settings;
- a guarantee under a restricted assumption;
- failure at a particular scale, severity, population, or domain.

Action: make the trade-off or regime the precise claim. A scoped win is often a
stronger paper than a universal claim contradicted by data.

### Class C — Informative secondary diagnostic

Examples:

- ordinary sensitivity checks;
- secondary metrics that do not change the conclusion;
- a null result on an out-of-scope application;
- an additional baseline with the same pattern.

Action: mention briefly or place in the appendix.

### Class D — Exploration history without scientific value

Examples:

- debugging failures;
- superseded implementations;
- arbitrary early trials;
- uncalibrated cases with no claim role.

Action: omit.

## 3. Do Not Say “We Lose”; Rewrite the Comparison Logic

When a result is not favorable, determine first:

1. Is it material to the headline claim?
2. Is the paper competing on the correct axis and under the intended constraint?
3. Is the result a rational trade-off?
4. Can the claim be narrowed without losing its value?
5. Should the result become a boundary rather than a verdict?
6. Should the paper select a different stronger story?

Prefer precise comparison:

> At unrestricted inference budgets, Method X attains the highest exact-match
> accuracy. Under the single-sample budget targeted here, our method improves
> calibration and reduces latency while matching X within the confidence
> interval.

Avoid self-defeating global language:

> Unfortunately, our method still performs worse than X and has limited
> effectiveness.

The first version discloses the fact and identifies the paper’s contest. The
second writes the rejection for the reviewer.

## 4. Comparison Fairness

For every comparison, check:

- same data access and preprocessing;
- same external pretraining, retrieval, tools, or privileged labels;
- same tuning budget and model/checkpoint selection rule;
- same inference budget, number of samples, context, prompts, and retries;
- same environment steps and evaluation policy for RL;
- same hardware, software, precision, batch, workload, and quality target for
  systems;
- same assumptions and problem class for theory;
- same participant/sample population and aggregation for human studies;
- uncertainty and missing-value handling;
- whether copied literature values are genuinely comparable.

Visibly separate unmatched comparisons. An unmatched high number can provide
context but cannot establish a rank.

## 5. Claim Calibration Ladder

Use the strongest licensed level:

```text
measured instance
→ recurring empirical pattern in specified settings
→ robust association under specified variations
→ explanation supported by diagnostics
→ identified mechanism under explicit assumptions
→ formal/general principle within a defined class
```

Examples:

- `The component contributes to the result` may follow from a deletion ablation.
- `The component works through mechanism M` requires evidence distinguishing M
  from alternatives.
- `The method generalizes` requires independently motivated settings, not four
  favorable datasets selected from a larger pool.
- `The system is faster` requires an operating point; `achieves higher
  throughput at matched latency and quality on hardware H` is interpretable.

## 6. Remove Defensive Writing

Delete language that supplies a global negative judgment:

- `Unfortunately, ...`
- `our method only ...`
- `still falls far behind ...`
- `the improvement is limited ...`
- `this serious weakness ...`
- `despite these shortcomings ...`

Replace it with:

```text
fact
→ condition
→ trade-off or boundary
→ consequence for the claim
```

Do not add disclaimers before claims merely to sound cautious. Put scope in the
claim itself:

> Across the evaluated encoder-only models, ...

rather than:

> Although our study is limited and may not generalize, we tentatively observe...

## 7. Make the Advantage Explicit

Do not expect the reviewer to infer contribution from a table. For every
favorable artifact, state:

1. under what condition the paper is strongest;
2. the exact comparison/readout;
3. why the advantage occurs or what evidence attributes it;
4. which practical or scientific problem it solves;
5. why that problem is worth the chosen trade-off.

Useful sentence form:

> Under **[condition]**, **[method/result]** improves **[metric/property]** by
> **[amount]** relative to **[matched comparator]**. **[Diagnostic/theoretical
> evidence]** shows that the difference comes from **[source]**, which matters
> because **[consequence]**.

## 8. Strong Scientific Wording

### Prefer concrete verbs

`show`, `establish`, `identify`, `characterize`, `derive`, `recover`, `separate`,
`resolve`, `enable`, `reduce`, `remove`, `preserve`, `scale`, `attribute`,
`expose`, `settle`, `rule out`, `match`, `surpass`.

### Attach claims to objects and conditions

Weak:

> Our approach achieves significant improvements.

Strong:

> At matched edit success, the projection cuts preservation error by 31% after
> 1,000 sequential edits.

Weak:

> The method is robust across different settings.

Strong:

> The ordering effect appears in all four reasoning benchmarks and at each of
> the three evaluated model scales.

### Use contrast productively

Contrast is often the shortest route to novelty:

- `Unlike X, which requires ..., Y ...`
- `Whereas prior methods remove A or B, the estimator removes both costs.`
- `The apparent transition disappears when the metric is continuous.`
- `The system targets throughput rather than interactive latency.`

Make the comparison factual and structural, not dismissive.

### Scope in noun phrases and conditions

Prefer:

- `for 7B–70B decoder-only models under 4-bit inference`;
- `on label-limited domain shifts`;
- `for log-concave targets with Lipschitz score`;
- `among the sampled participants from 75 countries`.

This is clearer than adding hedges to every verb.

## 9. Remove Generic AI-Like Prose

Rewrite or delete:

- generic field-opening paragraphs;
- repeated `Moreover`, `Furthermore`, `Additionally` chains;
- empty novelty, effectiveness, robustness, or significance claims;
- paragraph-final restatements with no implication;
- mandatory three-item lists unrelated to the evidence;
- `This highlights the importance of...` without a concrete decision;
- excessive abstract nouns such as `the utilization of the facilitation of`;
- uniform sentence cadence;
- smooth but paper-interchangeable prose;
- repeated summaries of the same result in Introduction, Method, Results, and
  Discussion without a new rhetorical job.

Specificity test:

> Could this sentence be pasted unchanged into a paper about another method,
> dataset, and result?

If yes, rewrite or remove it.

## 10. Compression Order

When over page budget, remove in this order:

1. project chronology and generic motivation;
2. repeated definitions and restatements;
3. non-claim-changing ablations and sensitivity grids;
4. duplicate main-text table/figure views;
5. distant related work;
6. exhaustive implementation detail already in appendix/code;
7. secondary datasets/metrics after the pattern is established;
8. ornamental lemmas, examples, and diagrams;
9. optional supporting claims.

Do **not** remove:

- the contradiction and key insight;
- decisive evidence;
- material comparison conditions;
- the strongest alternative-elimination test;
- theorem assumptions and consequence;
- material scope/trade-off;
- the transition that makes the argument understandable.

## 11. Reviewer-Objection Rewrite Rule

Do not answer a reviewer objection by adding a paragraph of defensive prose
unless the issue is truly about explanation. Repair at the correct layer:

| Objection | Correct repair |
|---|---|
| novelty unclear | sharpen contrast and closest-work mapping |
| claim unsupported | add/repair evidence or narrow claim |
| result may be artifact | add validity/control or alternative test |
| mechanism speculative | demote wording or run identifying intervention |
| comparison unfair | match protocol or separate comparison classes |
| paper feels incremental | change story/winning axis or make structural insight explicit |
| too many results | select proof modules and cut duplicates |
| hard to follow | redesign identity anchor, ordering, and transitions |
| limitations concerning | state exact scope and show what remains established |
