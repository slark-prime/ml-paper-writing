# Part II — Empirical Paper Architecture and Argument Templates

## Contents

1. Separate venue format, argument archetype, paper blueprint, and section rendering
2. Architecture laws for high-signal ML papers
3. Argument-archetype router and kill test
4. Results-ordering router
5. Reusable argument sequences

## What “Template” Means

Keep four layers separate:

1. **Venue format** — page limit, anonymity, checklist, LaTeX style.
2. **Argument archetype** — the global sequence of propositions the contribution
   must establish.
3. **Paper blueprint** — the selected proof modules, artifacts, order, and
   missing evidence for this research project.
4. **Section rendering** — the local rhetorical moves used to write each part.

A useful template specifies proof obligations and reader transitions. It does
not require a fixed number of paragraphs, contributions, experiments, or
figures.

---

## High-Signal Paper Architecture Laws

Use these recurring architecture patterns as heuristics, not venue rules. Match
them to the contribution and evidence instead of forcing every paper into one
layout.

### Law A — Strong papers have a promise stack

The title, abstract, introduction, first memorable artifact, and conclusion
express the same paper identity at different resolutions. They do not each
introduce a different contribution list.

### Law B — The opening gap is often a contradiction

Effective openings make a reader feel that an accepted lens, practice, or
assumption cannot accommodate an observed requirement. Generic field importance
is rarely enough.

### Law C — One thesis can support a coherent capability bundle

A new paradigm may establish quality, scaling, efficiency, and transfer; a
benchmark may establish construction quality and several scientific findings.
The bundle is legitimate when all modules are consequences of the same thesis.

### Law D — Every paper needs an identity anchor, not necessarily Figure 1

Common anchors:

| Paper kind | Typical identity anchor |
|---|---|
| empirical method | problem–idea–payoff Figure 1 |
| anomaly/diagnosis | before/after or phenomenon figure |
| theory | direct formal question plus main theorem/result box |
| systems | operating-point/Pareto figure or dataflow |
| data/benchmark | construct, sample, and coverage card |
| security/auditing | worked example plus decision statistic/procedure |
| human/use-inspired | workflow, population, or case-study triptych |
| unification | equivalence/duality diagram plus formal statement |

### Law E — Result order follows the largest early doubt

A new metric needs validation before a surprising result. A repair needs an
anomaly before a fix. A theory paper states the theorem before technical proof
machinery. A systems paper fixes the operating point before a throughput claim.

### Law F — Artifact diversity is useful only when interfaces differ

A diagram, equation, algorithm, table, plot, theorem, and case should not repeat
the same information. Each should answer a different cognitive question.

### Law G — Central case studies are legitimate

Dataset, human-feedback, workflow, deployment, and agent papers may use one or
more case studies as primary proof modules. The case requires a question,
selection rule, analysis protocol, and clear scope; it is not merely a colorful
example.

### Law H — Mechanisms need risky predictions

Strong mechanism and counter-belief papers specify an alternative explanation
that predicts what should change under a metric, intervention, scale, or domain,
then test those predictions in complementary ways.

### Law I — Systems papers sell an operating point

The claim is not “fast” in the abstract. It is a frontier or capability under a
workload, hardware, latency/throughput target, precision, memory, and output-
quality constraint.

### Law J — Theory papers sell a question, theorem, and consequence

They may contain no empirical figure or table. The agent must not add decorative
experiments or lemmas merely to imitate empirical papers.

### Law K — Simplicity works best when it resolves a diagnosed coupling

The strongest “simple method” papers first establish why existing complexity or
flexibility creates an unnecessary trade-off, then show that the simpler choice
preserves the valuable capability.

### Law L — The paper stops when the belief update closes

Outstanding papers can be extensive, but their main text still has a finite
argument spine. Additional evidence goes to the appendix when it no longer
creates a first-pass belief update.

---

## Argument-Template Router

Select one primary archetype. Add one supporting archetype only when it is a
proof module of the same thesis.

| Primary archetype | Core argument chain | Typical identity anchor | Required closure |
|---|---|---|---|
| Focused Method / Constraint Fix | structural failure → requirement/invariant → operation → result → attribution/scope | geometry or method overview | failure is real; design targets it; matched result; claimed choice matters |
| Anomaly–Diagnose–Repair | visible/surprising anomaly → characterization → hypothesis → minimal repair → downstream consequence | before/after phenomenon figure | anomaly systematic; diagnosis plausible; repair changes predicted behavior |
| New Paradigm / Factorization | dominant formulation → limiting assumption → new primitive/order → implementation → newly unlocked bundle | conceptual paradigm diagram | contrast substantive; implementation viable; capability follows from new formulation |
| Scalable Diagnosis / Measurement | deployment/scientific blind spot → measurable construct → valid scalable protocol → finding → intervention/implication | setting + metric + headline finding | construct valid; protocol controlled; finding not measurement artifact; useful consequence |
| Mechanism / Learning Dynamics | unexplained behavior → formal/causal hypothesis → predictions → diagnostics/interventions → mitigation or boundary | equation + trajectory/causal diagram | predictions distinguish alternatives; evidence reaches claimed mechanism level |
| Counter-Belief / Negative Result | credible prior → alternative model → risky predictions → complementary tests → corrected view | phenomenon + explanatory model | prior is real; tests decisive; trivial artifacts ruled out; replacement understanding offered |
| Trade-off Decoupling / Simplification | ubiquitous method/feature → coupled cost or unnecessary complexity → surprising simpler choice → explanation → improved frontier | contrast or frontier figure | cost is real; comparison fair; simplicity genuine; trade-off changes |
| Unification / Framework | fragmented families → common abstraction → recover special cases → derive algorithm/prediction → instantiate → payoff | duality/equivalence map | mappings faithful; abstraction nontrivial; produces leverage beyond relabeling |
| Theory: Formal Lens / Characterization | conventional lens insufficient → new definition → lower/upper bound or characterization → consequence/tightness | main theorem/result stack | assumptions precise; proof complete; result non-vacuous; consequence clear |
| Theory: Algorithmic Primitive | open complexity/statistical question → new primitive/meta-algorithm → theorem chain → refinements → applications | direct question + algorithm/theorem | closes stated gap; query/model assumptions explicit; applications are valid corollaries |
| Systems / Infrastructure | target operating point → bottleneck → dataflow/system insight → optimizer/scheduler/implementation → end-to-end frontier → attribution/scaling | Pareto or dataflow figure | matched environment; equivalent correctness/quality; end-to-end win; source explained |
| Data / Benchmark / Human Artifact | missing construct/population → construction → quality/coverage → baseline landscape or case modules → new insight | construct/sample card | validity, provenance, coverage, leakage/ethics, and scientific utility |
| Security / Auditing / Verification | threat or audit target → intervention/procedure → decision rule → theory/calibration → attack/sensitivity evaluation | worked example + statistic/procedure | false-positive control; power; threat model; operational interpretation |
| Use-Inspired / Domain Decision | authentic workflow → decision bottleneck → method/measurement → domain-valid evaluation → aggregate and process payoff | workflow or decision pipeline | use case real; current-practice baseline; domain metric; constraints and risks |
| Position / Agenda | neglected or contested practice → thesis → evidence/cases → strongest counterarguments → action agenda | thesis map or evidence synthesis | fair representation; factual/value claims separated; recommendations actionable |

### Archetype selection rules

Choose the archetype whose proof obligations best match the **strongest existing
evidence**, not the original project label.

- A method can become a discovery paper when the diagnostic finding is stronger
  than the intervention.
- A benchmark can become a counter-belief paper when its main value is a finding
  that changes field understanding.
- A complex method can become a simplification paper when the strongest result
  is that one principle makes most machinery unnecessary.
- A systems paper can become a capability paper when the operational change
  unlocks a previously impossible scale rather than merely improving speed.
- A theory-plus-experiment paper should choose whether the theorem explains the
  phenomenon or the phenomenon motivates the theorem; do not maintain two
  competing centers.

### Archetype kill test

Reject an archetype when any central obligation cannot be met without invented
or weak evidence. Either:

1. narrow the thesis;
2. demote a claim to a hypothesis;
3. run the decisive missing work;
4. select a different archetype.

Do not use prose to simulate closure.

---

## Results-Ordering Router

Select the first module by asking what would most block belief.

### Impact-first

Use when the task, metric, protocol, and comparison are standard.

```text
headline result
    -> attribution/design validation
    -> regimes/generalization
    -> cost/trade-off/boundary
```

### Validity-first

Use when a simulator, metric, label process, human protocol, or proxy is new.

```text
construct and protocol
    -> validity / controls
    -> headline finding
    -> interventions / robustness
    -> implication
```

### Diagnosis-first

Use when the contribution repairs an unexplained failure.

```text
phenomenon
    -> prevalence/characterization
    -> hypothesis
    -> intervention
    -> downstream consequence
```

### Mechanism-first

Use when explaining behavior is the contribution.

```text
definition or decomposition
    -> alternative hypotheses
    -> risky predictions
    -> identifying tests
    -> intervention/mitigation/boundary
```

### Theorem-first

Use when the formal statement is the product.

```text
formal question
    -> main theorem and consequence
    -> proof roadmap
    -> key interfaces/lemmas
    -> refinements, tightness, applications
```

### Construct-first

Use for datasets, benchmarks, and population-linked human artifacts.

```text
missing construct/population
    -> construction/provenance
    -> quality, coverage, ethics, leakage
    -> baseline landscape or scientific case modules
    -> newly visible conclusion
```

### Operating-point-first

Use for systems and efficiency.

```text
workload and objective
    -> bottleneck
    -> system/dataflow/design
    -> end-to-end frontier
    -> attribution/microbenchmarks
    -> scaling, overhead, failure boundary
```

### Procedure-first

Use when stating a simple operational procedure early removes more uncertainty
than a long background section.

```text
practical question
    -> procedure at a high level
    -> just-in-time background
    -> theory/correctness
    -> empirical validation
```

---

## Reusable Argument Sequences

Use these as dependency patterns, not mandatory section names.

```text
Anomaly → Characterization → Hypothesis → Repair → Consequence
```

```text
Prior Belief → Alternative Model → Risky Predictions
→ Complementary Tests → Corrected Belief
```

```text
Conventional Lens Fails → New Definition → Lower Bound
→ Matching Upper Bound → Complexity/Scientific Consequence
```

```text
Fragmented Families → Common Abstraction → Equivalence
→ Efficient Algorithm → New Instantiation → Empirical Payoff
```

```text
Open Gap → Primitive/Meta-Algorithm → Theorem Chain
→ Refinements → Application Corollaries
```

```text
Structural Conflict → Invariant/Constraint → Minimal Operation
→ Guarantee → RQ-Based Evaluation
```

```text
Operating Point → Bottleneck → Dataflow/System Design
→ Optimizer/Scheduler → End-to-End Frontier → Attribution → Scaling
```

```text
Missing Construct/Population → Construction → Quality/Coverage
→ Case Studies or Landscape → New Scientific Insight
```

```text
Deployment Mismatch → Scalable Simulator/Measurement
→ Validity → Finding → Intervention → Stakeholder Implication
```

```text
Wrong Factorization → New Primitive → Conceptual Anchor
→ Implementation → Headline Result → Scaling/Transfer/Capability
```

```text
Coupled Trade-off → Surprising Alternative → Toy/Analytic Intuition
→ Frontier Evidence → Qualitative or Human Confirmation
```

```text
Audit/Decision Target → Procedure → Statistical/Formal License
→ Attack/Sensitivity Tests → Operational Interpretation
```
