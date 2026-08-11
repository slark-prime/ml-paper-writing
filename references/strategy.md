# Part I — Guideline

## Contents

1. Academic launch rather than project report
2. Editorial selection versus evidentiary manipulation
3. Strongest defensible story and dominant thesis
4. Reader-belief update and contradiction-led framing
5. Contest, winning axis, and claims before prose
6. Reader-doubt ordering and promise stack
7. Idea-before-implementation and claim-specific evidence
8. Minimum closed argument and artifact jobs
9. Main-text/appendix routing and blueprint-driven research
10. Scope, working memory, calibrated verbs, and five-minute memory
11. Scientific-integrity floor

## 1. Treat the Paper as an Academic Launch, Not a Project Report

The paper's job is not to distribute attention fairly across the project. Its
job is to make the most valuable supported idea easy to notice, understand,
remember, and believe.

Ask:

> If a target reader remembers only one sentence, one artifact, one result, and
> one implication, what should they be?

Everything in the first-pass paper should reinforce that memory.

Do not organize around:

- the order experiments were run;
- the amount of engineering invested in each component;
- every dataset or metric available;
- every failed attempt;
- equal page allocation across collaborators or workstreams.

Organize around the final intellectual route:

```text
important prior or practice
    -> contradiction, blind spot, or bottleneck
    -> key insight
    -> contribution object
    -> decisive evidence
    -> consequence
```

## 2. Editorial Selection Is Mandatory; Evidentiary Manipulation Is Forbidden

A strong paper must be selective. Distinguish two very different meanings of
“cherry-picking.”

### Allowed and usually desirable: narrative selection

- select the strongest scientifically meaningful contribution;
- lead with the regime, metric, or use case that best expresses that value;
- choose the most diagnostic experiments for the main text;
- show representative or teaching examples rather than every example;
- omit debugging history, superseded implementations, and redundant results;
- move exhaustive grids, secondary datasets, and reproducibility detail to the
  appendix;
- frame the work around the comparison class and constraints it was designed to
  address;
- choose a title and opening that market the idea directly.

### Forbidden: evidentiary manipulation

- select seeds, splits, prompts, checkpoints, baselines, metrics, time windows,
  or cases after seeing the outcome in order to conceal the true pattern;
- omit a protocol-matched comparison or counterexample that would materially
  change the headline claim;
- mix unmatched literature numbers into a ranking without marking the mismatch;
- present a hand-picked case as population evidence;
- redefine the task or metric post hoc solely because the original result lost;
- claim a mechanism from a non-identifying ablation;
- hide a claim-changing trade-off in a footnote or appendix.

Use the **materiality test**:

> Would a reasonable reviewer substantially change their interpretation, scope,
> or confidence in the headline claim after seeing the omitted fact?

If yes, disclose it. If no, it need not occupy the main narrative.

## 3. Select the Strongest Defensible Story, Not the Largest Story

Generate candidate stories before drafting. The strongest story optimizes:

- **importance** — the question or consequence matters;
- **contrast** — it changes a prior, resolves a contradiction, or unlocks a
  capability;
- **evidence strength** — the decisive claim is well supported;
- **diagnostic clarity** — the evidence distinguishes the claim from credible
  alternatives;
- **compressibility** — the contribution can be understood and remembered;
- **audience relevance** — the target community recognizes the stakes;
- **closure** — the main proof obligations can be completed;
- **risk** — the story does not depend on a fragile or unfair comparison.

Do not choose a story because it accommodates the largest number of results.
Many good results can belong to a weak paper; a few decisive results can belong
to a strong one.

## 4. One Dominant Thesis, One Coherent Result Bundle

A paper should normally have one dominant thesis and one to three proof modules.
This does **not** mean one result.

A coherent bundle may include, for example:

- a new paradigm, its scaling behavior, and a new capability;
- an anomaly, its diagnosis, and a minimal repair;
- a formal abstraction, an efficient algorithm derived from it, and a new
  architecture;
- a dataset, its coverage/quality evidence, and several scientific case
  studies;
- a theorem, a matching bound, and an application consequence.

Admit a supporting module only when:

1. it follows from or is necessary for the same thesis;
2. it answers a distinct reader question;
3. removing it makes the thesis less credible, less important, or less clear.

Do not package unrelated publishable findings into one paper merely because they
share code or data.

## 5. State the Reader-Belief Update

Complete:

> A reasonable target reader currently believes or practices **[prior]**. This
> paper establishes **[new claim]** under **[scope/assumptions]**, using
> **[decisive evidence]**. The update matters because **[consequence]**.

The prior should be concrete enough to contradict. Useful priors include:

- a dominant technical assumption;
- a standard evaluation practice;
- an accepted complexity barrier;
- a deployment workflow;
- a common explanation for a phenomenon;
- a belief that a resource or capability is unavailable.

A paper that cannot specify the belief update usually reports activity rather
than an argument.

## 6. Prefer a Contradiction to Generic Importance

Many strong ML introductions do not begin with “Machine learning has made rapid
progress.” They begin with a tension that makes the paper necessary.

Useful contradiction forms:

```text
X is the dominant paradigm, but Y exposes a property it cannot explain.
Models are trained/evaluated in X, but deployed in Y.
Feature X is sold as an advantage, but under condition Y it causes failure Z.
Existing methods solve bottleneck A or B, but not both.
The field measures construct X with metric Y, but Y changes the phenomenon.
Resource X is abundant, yet current methods cannot use it because Y is missing.
A method is accurate in aggregate, but fails on the decision that matters in practice.
```

The contradiction should be real, specific, and resolved by the contribution.
Do not manufacture a strawman gap.

## 7. Name the Contest and the Winning Axis

Do not implicitly enter every possible competition. State:

- the target setting;
- the comparison class;
- the controlled resources or assumptions;
- the winning axis;
- why that axis is scientifically or practically meaningful.

Valid winning axes include:

- capability under a previously unusable data regime;
- accuracy at matched compute, latency, memory, or labels;
- throughput at a defined operating point;
- preservation at matched edit success;
- calibration or robustness under a specific shift;
- a better quality–diversity or cost–quality frontier;
- weaker assumptions or a tighter formal bound;
- a scalable measurement previously unavailable;
- a simpler procedure with comparable outcomes;
- a corrected understanding or negative result;
- a dataset that exposes heterogeneity hidden by existing artifacts.

A paper need not win every metric. It must make clear which meaningful contest
it wins and support that claim fairly.

## 8. Build Claims Before Prose

Use:

```text
claim
    -> proof obligation
    -> decisive evidence
    -> alternative explanations
    -> scope
    -> wording ceiling
```

Never use:

```text
impressive sentence
    -> nearby result
    -> retrofitted explanation
```

Every central claim must point to a concrete artifact or formal statement.
Every main-text artifact must discharge a named proof obligation.

## 9. Order the Paper by the Reader’s Largest Current Doubt

“Dependency order” is not specific enough. At each point ask:

> What is the most important reason a skeptical reader would not yet accept the
> next claim?

Choose the paper’s dominant ordering mode:

- **impact-first** — the setup is standard; show the headline outcome early;
- **validity-first** — the measurement, simulator, metric, or human protocol is
  unfamiliar; establish that it measures the claimed construct first;
- **diagnosis-first** — a repair only matters after the anomaly/failure is shown
  and characterized;
- **mechanism-first** — the main value is an explanation that generates
  predictions;
- **theorem-first** — the formal statement is the contribution; state it before
  proof machinery;
- **construct-first** — a dataset/benchmark must establish population,
  provenance, quality, and coverage before analyses;
- **operating-point-first** — a systems claim is meaningless until workload,
  latency/throughput objective, hardware, precision, and quality constraints are
  fixed.

The paper may switch modes between proof modules, but each switch should resolve
a real reader doubt.

## 10. Use a Promise Stack, Not Accidental Repetition

The title, abstract, introduction, identity anchor, and conclusion should repeat
the same thesis at increasing resolution:

```text
Title          = identity or contrast
Abstract       = complete compressed promise plus decisive evidence
Introduction   = why the promise is necessary and plausible
Identity anchor= visual/formal memory object
Conclusion     = implication after the evidence is accepted
```

Strategic redundancy is useful. Verbatim repetition and repeated result lists
are not. Each layer should answer a different reader question while preserving
the same central claim.

## 11. Give the Idea Before the Implementation

Before implementation details, give the reader:

1. the exact requirement or obstacle;
2. the one-sentence insight;
3. the input/output or formal object;
4. the invariant, decomposition, factorization, dataflow, or causal intuition;
5. the reason the contribution should work or be true.

Then introduce components, equations, algorithms, and engineering details in
conceptual dependency order.

Do not make the reader infer the idea from code-shaped subsections.

## 12. Match Evidence to Claim Type

Use claim-specific proof obligations:

- **performance** — matched baselines, uncertainty, meaningful regimes, and
  resource parity when relevant;
- **efficiency/systems** — fixed operating point, controlled environment,
  equivalent output quality/correctness, end-to-end result, attribution, and
  scaling/overhead;
- **mechanism** — precise hypothesis, credible alternatives, risky predictions,
  identifying interventions or formal analysis, and a boundary;
- **generalization** — independently motivated environments or shifts,
  heterogeneity, and no post-hoc cherry-picking of favorable domains;
- **theory** — precise assumptions, headline theorem, proof roadmap, complete
  proof, prior-bound comparison, consequence, and tightness/counterexample when
  central;
- **dataset/benchmark/evaluation** — construct validity, provenance,
  construction quality, coverage, leakage/contamination checks, baseline
  landscape, and new scientific information;
- **human/qualitative** — sampling frame, protocol, rater/process validity,
  aggregation, uncertainty/disagreement, and the claim a case can and cannot
  support;
- **security/auditing** — threat/observation model, decision rule, false-positive
  calibration, power/sensitivity, attacks or transformations, and operational
  interpretation;
- **negative/counter-belief** — credible prior, alternative model, risky
  predictions, complementary tests with different failure modes, ruled-out
  trivial artifacts, and corrected view;
- **use-inspired** — authentic workflow, domain requirements, relevant current
  practice or non-ML baseline, domain metric, aggregate outcome, process/case
  evidence, and operational constraints.

## 13. Design the Minimum Closed Argument

For each central claim, build the smallest evidence pack that closes it. A
common pack contains:

1. **decisive evidence** — the main result, theorem, or finding;
2. **credibility evidence** — validity, matched control, proof interface, or
   alternative-elimination test;
3. **scope evidence** — generalization, boundary, trade-off, tightness, or
   failure regime.

More evidence is justified only when it addresses a distinct material doubt.
Ten datasets that produce the same belief update are not ten proof modules.

## 14. Every Artifact Must Change a Belief

A prose statement, equation, diagram, plot, table, algorithm, theorem, lemma,
example, case study, qualitative panel, or error analysis enters the main text
only when it has a named cognitive job.

Ordinary artifacts should have one primary job. The **identity anchor** is the
exception: it may coordinate problem, idea, and payoff as one designed mini-
paper, provided the message remains legible.

If an artifact has no job, drop it. If two artifacts perform the same job, keep
the clearer one unless the second is an independent test with different failure
modes.

## 15. Main Text Is a First-Pass Argument; Appendix Is an Audit Interface

The main text contains everything a skeptical first-pass reader needs to:

- understand the thesis;
- assess the decisive evidence;
- verify material comparison conditions;
- know the claim’s scope and main trade-off.

The appendix contains random-access substantiation:

- exhaustive grids and secondary datasets;
- full proofs and routine lemmas;
- complete protocols, prompts, hyperparameters, and implementation detail;
- additional robustness and qualitative examples;
- complete per-group or per-task tables;
- reproducibility and audit material.

Do not place the only support for a headline claim, a claim-changing negative
result, or a material fairness condition only in the appendix.

## 16. Use the Blueprint as a Research Instrument

Create empty artifacts and claim cards before the research is “finished.” An
empty table cell, missing curve region, unproved theorem clause, absent control,
or incomplete case-study field should become a concrete research task.

Every proposed new experiment must have a decision contract:

```text
Question:
Competing outcomes:
If outcome A, change claim/story in this way:
If outcome B, change claim/story in this way:
If null/ambiguous, change claim/story in this way:
Minimum protocol needed:
Target artifact and exact cell/curve/statement:
```

Do not run experiments merely because reviewers “expect more.” Run them because
the outcome can change a claim, close a proof obligation, or remove a specific
acceptance risk.

## 17. Scope Precisely; Do Not Write the Reviewer’s Rejection Summary

A limitation states where a claim stops. It should not convert a local boundary
into a global negative verdict.

Prefer:

> The evidence covers encoder-only models under label-limited domain shift;
> autoregressive transfer remains untested.

Avoid:

> Unfortunately, our method is severely limited and may not generalize.

Do not use “only,” “still far behind,” “limited improvement,” “serious weakness,”
or similar global self-judgments unless the exact wording is scientifically
necessary. Report material facts, conditions, trade-offs, and claim consequences
directly.

## 18. Write for the Reader’s Working Memory

Reduce cognitive load by:

- stable terminology;
- explicit referents and contrast words;
- overview before detail;
- short proof and dependency interfaces;
- informative section and subsection headings;
- notation introduced just before use;
- captions that state the conclusion and condition;
- one paragraph with one dominant rhetorical job.

Do not optimize for uniform sentence length, mandatory passive voice, or other
mechanical style rules.

## 19. Use Direct, Calibrated Scientific Verbs

Use the strongest verb licensed by evidence:

- `we observe` for a measured instance;
- `we find` for a recurring empirical pattern;
- `we show` for a supported conclusion;
- `we identify` for a characterized object or failure mode;
- `we establish` or `we prove` for a formal result;
- `we recover` for a faithful special case;
- `we enable` for a demonstrated capability;
- `we reduce` or `we improve` with an object, condition, and number;
- `we attribute` only with identifying evidence;
- `we suggest` or `we hypothesize` when evidence is preliminary.

Avoid empty adjectives such as `novel`, `robust`, `significant`, `comprehensive`,
and `promising` unless the sentence names the object and evidence.

## 20. Pass the Five-Minute Memory Test

After a simulated first read, a target reader should be able to recall:

1. **one sentence** — the central thesis;
2. **one visual or formal object** — the identity anchor;
3. **one number, theorem, or finding** — the decisive evidence;
4. **one reason it matters** — the scientific/practical implication.

If the reader instead remembers a list of datasets, modules, and ablations, the
paper is still a result dump.

---

## Scientific-Integrity Floor

Narrative optimization never licenses factual distortion.

1. Never invent a result, theorem, proof, citation, number, dataset property,
   implementation detail, quotation, statistical test, or human judgment.
2. Never suppress evidence that is material under the materiality test.
3. Never claim state of the art without a genuinely protocol-matched comparison.
4. Never present post-hoc selection as pre-specified when the distinction is
   material.
5. Never convert association into mechanism without identification, formal
   reasoning, or converging diagnostic evidence.
6. Never claim population behavior from a teaching example or selected case.
7. Never call a theorem consequential without explaining assumptions and what
   it changes.
8. Never remove correctness qualifiers during compression.
9. When a central claim is contradicted, change the claim, proof module, or paper
   story. Do not rhetorically relabel the contradiction as support.
