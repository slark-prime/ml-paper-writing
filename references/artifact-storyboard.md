# Artifact Storyboard and Evidence Spine

## Contents

1. Identity-anchor selection and contract
2. Artifact cards and storyboard
3. Main-text evidence spines by paper family
4. Section order from reader questions
5. Result subsections as micro-arguments
6. Captions as standalone arguments
7. Redundancy versus converging evidence
8. Worked result-dump compilation

## 14. Compile the Identity Anchor

Every paper needs one object that a reader can use to reconstruct the idea. Do
not force this object to be Figure 1.

### Identity-anchor router

| Contribution | Default anchor | It should answer |
|---|---|---|
| empirical method | problem–idea–payoff figure | what fails, what changes, and what improves? |
| anomaly/repair | before/after or phenomenon–diagnosis panel | what is the anomaly and how does the intervention change it? |
| new paradigm | old-vs-new factorization/primitive diagram | what conceptual choice changed? |
| mechanism | decomposition, causal/prediction diagram, or trajectory figure | what account makes distinct predictions? |
| theory | formal question plus main theorem/result stack | what is proved, under what assumptions, and why is it surprising? |
| unification | equivalence/duality map | which objects become instances of one abstraction and what leverage follows? |
| systems | operating-point Pareto figure or dataflow diagram | under what constraints is the system better, and why? |
| data/benchmark | construct/population/coverage card | what previously missing object is captured? |
| security/audit | worked example plus decision statistic/procedure | what signal is inserted/observed and how is a decision made? |
| human/use-inspired | workflow/population/case-study triptych | whose decision or process is represented and what becomes visible? |

### Identity-Anchor Contract

```text
Anchor type:
Paper identity it encodes:
Reader questions answered:
Problem/prior shown:
Key insight/object shown:
Decisive payoff/result shown:
Scope/condition shown:
One-sentence takeaway:
What the anchor deliberately excludes:
Caption/statement conclusion:
```

A problem–idea–payoff figure may have three coordinated jobs because it is a
mini-paper. Keep one visual hierarchy and one takeaway; do not turn it into a
poster containing every experiment.

The identity anchor should appear early enough that a reader can use it while
reading the technical sections.

## 15. Build the Artifact Storyboard

Create an Artifact Card before generating each main figure, table, algorithm,
theorem, or case:

```text
Artifact ID and type:
Proof module:
Primary reader question:
Primary belief job:
Claim served:
Why this representation is better than alternatives:
Inputs/data/assumptions:
Comparison/control/counterfactual:
Exact visual/formal encoding:
Exact readout the prose will name:
Uncertainty/validity information:
One-sentence title/message:
Caption or statement skeleton:
Main-text placement:
Appendix companion:
Removal consequence:
```

Then create a storyboard table:

| Order | Reader state before | Artifact | Exact takeaway | Reader state after | Next doubt |
|---|---|---|---|---|---|

The artifact sequence should itself communicate the paper when viewed with
captions and section headings only.

## 16. Compile the Main-Text Evidence Spine

The evidence spine is the smallest ordered set of artifacts that closes all
proof modules.

### Common empirical-method spine

```text
A0 identity anchor
A1 decisive matched outcome
A2 claim-critical attribution/validity test
A3 regime, generalization, or boundary
A4 cost/frontier or qualitative/process evidence when material
```

### Common diagnosis/counter-belief spine

```text
A0 phenomenon
A1 characterization or alternative model
A2 risky prediction test
A3 independent/complementary test
A4 intervention, correction, or implication
```

### Common theory spine

```text
F0 formal question/definition
T1 main theorem
P1 proof roadmap/key interface
T2 matching/tightness/refinement
C1 consequence/application/counterexample
```

### Common systems spine

```text
A0 operating point / Pareto promise
A1 bottleneck or profile
A2 dataflow/system design
A3 end-to-end matched result
A4 attribution/microbenchmark
A5 scaling/overhead/boundary
```

### Common data/human spine

```text
A0 construct/population identity
A1 provenance/collection/coverage/quality
A2 baseline or descriptive landscape
A3–A5 central scientific case modules
A6 scope/appropriate-use boundary
```

Do not treat these counts as quotas. Delete any slot irrelevant to the claim and
add a slot only for a distinct material doubt.

## 17. Choose Section Order from the Evidence Spine

Build the body by grouping adjacent artifacts that answer the same reader
question. Do not start with conventional section names.

For each proposed subsection:

```text
Reader question:
Required prior knowledge:
Claim/conclusion:
Artifact(s):
Exact readout:
Alternative addressed:
Scope/boundary:
Transition created:
```

Only then name the subsection. Prefer a question or claim when the subsection is
an empirical argument:

- `The degradation arises from recovery failures, not task difficulty`
- `Does the gain persist under domain shift?`
- `Register tokens remove high-norm background artifacts`

Use dependency/object names for formal or method exposition when they are
clearer:

- `Null-Space Projection`
- `First-Order Rejection Sampling`
- `Semiseparable Matrix Representation`

Avoid generic headings such as `More Results`, `Additional Analysis`, `Ablation
Study`, or `Qualitative Evaluation` unless no more informative claim is possible.

## 18. Render Every Result Subsection as a Micro-Argument

Use this internal sequence:

1. **Question or claim** — what uncertainty is being resolved?
2. **Diagnostic rationale** — why would this experiment/proof/case distinguish
   the relevant alternatives?
3. **Essential protocol** — only the conditions needed for interpretation.
4. **Artifact pointer** — tell the reader where to look.
5. **Exact readout** — name the cell, curve region, theorem clause, or case
   evidence.
6. **Licensed interpretation** — state the strongest supported conclusion.
7. **Boundary or transition** — define scope or open the next reader question.

Example:

> We first ask whether the improvement comes from higher update success or from
> reduced collateral change. At matched edit success, Table 2 shows that the
> projection lowers the preservation error across all three model sizes, with
> the largest difference after sequential edits. This isolates preservation—not
> easier edits—as the source of the aggregate gain. We next test whether the
> same constraint preserves general capabilities outside the edited facts.

Do not narrate every table cell. Direct attention to the readout that changes
the claim.

## 19. Write Captions as Standalone Micro-Arguments

A useful caption contains:

1. what is shown;
2. the comparison, condition, or encoding;
3. the main conclusion;
4. uncertainty or selection information needed for interpretation.

Weak:

> Results on the benchmark.

Stronger:

> **Fixed-order RL rollouts preserve solution diversity.** Across four reasoning
> benchmarks, confidence-ordered rollouts skip high-uncertainty forking tokens
> more often and produce fewer distinct solution paths; left-to-right rollouts
> reverse both effects while inference remains parallel.

A caption may be a little redundant with the surrounding prose because artifact-
only readers need a complete message.

## 20. Distinguish Redundancy from Converging Evidence

Delete evidence when it repeats the same belief update under nearly identical
failure modes.

Retain multiple tests when they are independently diagnostic. For example:

- one model-family experiment plus a meta-analysis plus a deliberately
  constructed cross-domain test;
- a theorem plus a matching lower bound;
- aggregate human outcomes plus a longitudinal case;
- an end-to-end systems result plus profiling that attributes the gain.

For every repeated-looking artifact, state:

```text
What failure mode of the first artifact does the second avoid?
What alternative explanation does only the second test?
What claim would become weaker if the second disappeared?
```

If none has a concrete answer, move or remove it.

## 21. Worked Compilation — From a Result Dump to a Paper Program

Suppose the workspace contains:

```text
8 datasets
4 metrics
12 ablations
1 low-data sweep
1 latency result
1 theorem
6 qualitative examples
1 deployment trace
```

Do not create eight dataset subsections and a generic ablation section.

### Step A — Generate competing stories

```text
Story A: a broadly better method
Story B: a method that solves low-data calibration
Story C: a mechanism explaining why the auxiliary objective helps
```

If Story B has the strongest and most diagnostic evidence, select it even when
Story A would include more experiments.

### Step B — Compile proof modules

```text
M1: the low-data failure is important and systematic
M2: the proposed design improves calibration at matched accuracy
M3: the effect follows from the claimed design choice and has a known boundary
```

### Step C — Select artifacts

```text
A0: failure + idea + payoff identity figure
A1: headline accuracy/calibration table on representative tasks
A2: low-data regime curve across all tasks
A3: one diagnostic intervention tied to M3
A4: cost–quality frontier if latency is material
Appendix: full 8-dataset × 4-metric table, secondary ablations, all examples
Drop: ablations with no distinct design claim
```

The theorem enters only if it licenses the mechanism or boundary claim. The
deployment trace becomes a central case only if the thesis concerns workflow or
process; otherwise it illustrates the implication in the appendix.

### Step D — Expose missing research

If A2 has no high-data region, the boundary is unknown. If A3 removes several
functions at once, attribution is not identified. Add only the minimum run or
proof that changes these decisions.

### Step E — Compile sections

```text
1 Introduction: low-data calibration contradiction and thesis
2 Problem Setup: calibration target and evaluation contract
3 Method: requirement → design overview → objective
4 The method improves calibration at matched accuracy
5 The gain is concentrated in the low-label regime
6 The auxiliary pathway, not additional compute, explains the gain
7 Cost, scope, and implications
```

This is a paper program. `Method / Experiments / Ablations / More Results` is not.
