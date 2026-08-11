# Part III — Paper Blueprint Compiler

## Contents

1. Inspect and normalize the research workspace
2. Generate candidate stories
3. Compile the positioning card
4. Compile proof modules
5. Build the reader-belief graph
6. Build the claim–evidence ledger
7. Prioritize missing evidence
8. Assign evidence jobs
9. Admit, reroute, or drop results
10. Build claim-specific evidence packs

## 1. Inspect and Normalize the Research Workspace

Before story selection, inventory:

```text
Questions and original hypotheses
Literature and accepted priors
Datasets / populations / environments
Models / methods / systems / formal objects
Experiment protocols and logs
Results, including null and contrary results
Plots and tables already produced
Proofs, propositions, lemmas, counterexamples
Qualitative examples and case traces
Human/domain feedback
Costs, failures, assumptions, and unresolved decisions
```

Convert each potentially useful item into an Evidence Record:

```text
Evidence ID:
Verified finding:
Source: [file / table / log / proof / annotation / citation]
Object and setting:
Protocol or assumptions:
Comparison or counterfactual:
Estimate / formal statement / uncertainty:
Selection process: [seeds / prompts / cases / subsets / assumptions]
Candidate claim(s) supported:
Candidate claim(s) weakened or contradicted:
Primary evidence role:
Plausible alternative explanations:
Scope licensed:
Credibility risks:
Candidate representation(s):
Status: verified / partial / disputed / missing
```

Separate four levels:

- **observation** — what was measured, witnessed, or proved;
- **interpretation** — what it suggests;
- **claim** — what the paper asks the reader to accept;
- **implication** — what follows after acceptance.

An observation does not enter the paper merely because it exists.

## 2. Generate a Candidate Story Portfolio

Produce two to five candidate stories when the material supports alternatives.
Each Story Card contains:

```text
Story ID and working title:
Target reader:
Prior belief/practice:
Contradiction or bottleneck:
Dominant thesis:
Winning axis and comparison class:
Primary archetype:
Proof module 1:
Proof module 2:
Proof module 3, if essential:
Decisive existing evidence:
Identity-anchor candidate:
Main unresolved doubt:
Evidence that would kill this story:
Evidence still needed:
What would be dropped from the paper:
```

Score stories qualitatively from 1–5 on:

| Criterion | Question |
|---|---|
| Importance | Does the update matter to the target community? |
| Contrast | Is there a crisp prior, contradiction, or unlocked capability? |
| Evidence strength | Is the headline already supported? |
| Diagnosticity | Does the evidence distinguish this account from alternatives? |
| Compressibility | Can the idea be remembered and visualized/formalized? |
| Audience fit | Will the intended venue recognize the contest? |
| Closure | Can the proof obligations be completed? |
| Risk | How much depends on fragile comparisons or unsupported interpretation? |

Select the highest-value closed story, not mechanically the highest average
score. A slightly narrower story with decisive evidence usually beats a broader
story with several weak modules.

## 3. Compile the Paper Positioning Card

After choosing the story, lock:

```text
Paper identity in one sentence:
Target reader:
Reader's prior:
Contradiction/gap:
Key insight:
Contribution object:
Winning axis:
Comparison class:
Operating conditions / assumptions:
Strongest decisive result or theorem:
Why the win matters:
Claims explicitly not made:
Material boundaries:
Five-minute memory sentence:
Five-minute memory artifact:
Five-minute memory number/theorem:
```

Use the one-sentence identity form:

> For **[task/setting]**, we show that **[insight or design]** enables/establishes
> **[capability or conclusion]** under **[conditions]**, supported by
> **[decisive evidence]**.

This is a contract, not final prose. Every section must remain consistent with
it.

## 4. Compile the Dominant Thesis into Proof Modules

A proof module is a reader question whose resolution is necessary for the
paper's identity.

```text
Module ID:
Reader question:
Module claim:
Why this module is necessary:
Exit condition: what the reader must accept before moving on
Decisive artifact:
Credibility/control artifact:
Scope/boundary artifact:
Prerequisite modules:
Alternative explanation addressed:
Current closure: closed / partial / open / contradicted
```

Use one to three modules. Examples:

- **New paradigm:** formulation is substantively different; it works; it unlocks
  scaling/capability.
- **Anomaly repair:** anomaly is real; diagnosis explains it; intervention fixes
  the predicted behavior.
- **Theory:** main separation/bound holds; matching/tightness clarifies it;
  consequence changes understanding or practice.
- **Dataset:** construct/population is missing; artifact captures it credibly;
  analyses reveal information unavailable before.

A result that cannot be assigned to a proof module, a material scope qualifier,
or reproducibility belongs outside the paper.

## 5. Build the Reader-Belief Ladder and Question Graph

Use universal questions, deleting irrelevant ones:

| ID | Reader question | Typical exit condition |
|---|---|---|
| Q0 | Why should I care? | concrete scientific/practical stake |
| Q1 | What prior, practice, or assumption is insufficient? | crisp contradiction or bottleneck |
| Q2 | What exactly is the thesis? | scoped, refutable statement |
| Q3 | Is the problem, construct, population, or measurement real? | validity evidence or accepted setup |
| Q4 | What is the proposed object, idea, procedure, theorem, or study? | understandable overview/definition |
| Q5 | Why should it work or be true? | invariant, intuition, derivation, dataflow, prediction, or proof roadmap |
| Q6 | What is the decisive result? | fair comparison, main theorem, or central finding |
| Q7 | Why attribute the result to the claimed idea? | intervention, diagnostic, key proof interface, or microbenchmark |
| Q8 | Where does it hold? | settings, populations, scales, or assumptions |
| Q9 | What does it cost, trade off, or fail on? | frontier, boundary, counterexample, or failure structure |
| Q10 | What changes for research or practice? | specific implication or decision |

Create edges:

- `prerequisite` — needed for comprehension;
- `support` — raises confidence in a claim;
- `rebuttal` — rules out a credible alternative;
- `scope` — narrows or extends a claim;
- `consequence` — follows after a claim is accepted.

The body should follow a readable topological order. The Abstract and
Introduction preview the payoff before walking the complete dependency chain.

## 6. Build the Claim–Evidence Ledger

For every claim:

```text
Claim ID:
Exact claim:
Claim type:
Central / supporting / boundary / implication:
Required evidence:
Available evidence IDs:
Strongest credible alternative:
Wording ceiling:
Status: supported / partial / missing / contradicted
Main-text artifact:
Appendix support:
Required action:
```

A contribution bullet must correspond to a central or supporting claim in this
ledger. A result paragraph must name which claim it updates.

## 7. Compile the Missing-Evidence Matrix

Do not output an unprioritized wish list. Classify every gap:

| Priority | Meaning | Default action |
|---|---|---|
| Claim-breaking | Without it, the headline is not licensed | run/prove/collect or change thesis |
| Review-blocking | A strong reviewer objection remains unanswered | prioritize before submission |
| Strengthening | Improves importance, attribution, scope, or confidence | run if cost-effective and decision-changing |
| Appendix completeness | Needed for audit/reproduction, not first-pass belief | complete or document in appendix |
| Optional decoration | Adds volume but no material belief update | do not run |

For every proposed experiment/proof/case, write:

```text
Gap addressed:
Claim affected:
Competing hypotheses/outcomes:
Minimal diagnostic protocol:
Expected artifact and exact readout:
Decision if positive:
Decision if negative:
Decision if null/ambiguous:
Cost and priority:
```

If no possible outcome would change the paper, do not run it.

## 8. Assign Every Evidence Item a Reader-Belief Job

Use one primary job and at most one secondary job:

| Job | Reader-belief change |
|---|---|
| ORIENT | establishes object, workflow, notation, setting, or operating point |
| MOTIVATE | shows gap, anomaly, failure, cost, or bottleneck |
| DEFINE | operationalizes construct, metric, target, or formal problem |
| EXPLAIN | supplies intuition, geometry, causal hypothesis, or rationale |
| VALIDATE | establishes measurement, dataset, protocol, proof premise, or implementation trust |
| DEMONSTRATE | supplies the decisive empirical or formal outcome |
| COMPARE | locates the contribution against alternatives under matched conditions |
| ATTRIBUTE | identifies the design, mechanism, or assumption producing the effect |
| GENERALIZE | establishes behavior across tasks, domains, scales, users, or assumptions |
| TRADEOFF | shows cost, latency, memory, sample use, risk, or frontier |
| BOUND | exposes failure regime, counterexample, null regime, or scope limit |
| ILLUSTRATE | makes an abstract object concrete without establishing prevalence |
| REPRODUCE | provides detail needed to repeat or audit |
| IMPLY | connects the evidence to a scientific, design, or policy consequence |

## 9. Result Admission Gate

For each candidate result, ask:

1. **Claim linkage** — which claim or material qualifier does it support?
2. **Discriminative value** — does it distinguish the paper's account from a
   credible baseline, alternative, or null?
3. **Credibility** — is the protocol strong enough for the intended conclusion?
4. **Distinctness** — does it create a new belief update?
5. **First-pass necessity** — must a skeptical reader see it now?

Route:

- **Main text** — 1–4 yes and 5 yes;
- **Appendix** — 1–4 yes and 5 no;
- **Re-run/revise** — the claim matters, but credibility or diagnosticity is
  insufficient;
- **Drop** — no material claim changes, evidence is redundant, or no reliable
  interpretation exists.

When space is scarce, compare:

```text
argument value
  = centrality + diagnosticity + credibility + scope impact + memorability
    - redundancy - reader cost
```

Use this as a qualitative tie-breaker, not fabricated quantitative science.

## 10. Compile Claim-Specific Evidence Packs

### Comparative performance pack

- protocol-matched strong baselines;
- task-aligned decisive metric;
- uncertainty or repeated evaluation where applicable;
- exact comparison conditions;
- meaningful regime heterogeneity when averages conceal behavior;
- compute/data/latency/quality parity when the claim depends on it.

### Efficiency or systems pack

- workload, objective, and bottleneck;
- equivalent output quality or correctness;
- matched hardware/software/precision/batch conditions;
- end-to-end latency, throughput, memory, energy, or cost;
- attribution by profiling, microbenchmark, or analysis;
- scaling or Pareto behavior;
- overhead and unfavorable regimes.

### Mechanism or explanation pack

- phenomenon to explain;
- precise hypothesis and credible alternatives;
- risky predictions that differ across explanations;
- intervention, formal identification, or complementary diagnostics;
- mitigation or transfer predicted by the account;
- boundary and calibrated wording.

A deletion ablation usually supports component contribution, not a complete
mechanism.

### Generalization pack

- independently motivated settings, shifts, scales, or populations;
- per-setting results, not only an aggregate;
- uncertainty and heterogeneity;
- evidence that favorable settings were not selected post hoc;
- boundary where transfer stops, when known.

### Theory pack

- formal problem and assumptions;
- main theorem early;
- intuitive interpretation and proof roadmap;
- key proposition/lemma interfaces;
- complete proof;
- relation to prior results;
- consequence, matching result, lower bound, tightness, or counterexample when
  it is central.

### Data / benchmark / evaluation pack

- missing construct, population, or measurement need;
- intended use and construct definition;
- provenance, collection, annotation, or generation process;
- quality, coverage, leakage/contamination, ethics, and validity;
- baseline landscape under a clear protocol;
- scientific analyses or cases enabled by the artifact;
- limitations and appropriate use.

### Human / qualitative pack

- construct and rubric;
- sampling frame and selection process;
- annotator qualifications or participant context;
- blinding/randomization and aggregation;
- agreement, uncertainty, and disagreement structure;
- aggregate outcome;
- case or qualitative evidence selected by a declared rule.

### Security / auditing pack

- threat and observation model;
- procedure/intervention and decision rule;
- false-positive or Type-I calibration;
- power/sensitivity and sample complexity;
- attack, adaptive transformation, or robustness evaluation;
- operational interpretation and failure boundary.

### Use-inspired pack

- authentic workflow and stakeholder need;
- domain constraints and failure costs;
- valid target and domain-relevant metric;
- current-practice, heuristic, or non-ML baseline;
- aggregate technical/domain outcome;
- process or case evidence where context matters;
- deployment, data, governance, and resource constraints.

### Negative or counter-belief pack

- documented and consequential prior belief;
- precise alternative account;
- predictions that differ from the prior;
- complementary tests with different failure modes;
- robustness to reasonable analysis choices;
- corrected view, boundary, or actionable implication.
