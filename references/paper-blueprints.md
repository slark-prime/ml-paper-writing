# Part IV — Contribution-Specific Paper Blueprints

Use these blueprints to compile the **argument**, not to copy their wording.
Each blueprint supplies a default dependency chain, proof modules, artifact
choices, and research-completion triggers.

## Contents

1. Focused method or invariant fix
2. Anomaly–diagnose–repair
3. New paradigm, factorization, or capability
4. Scalable diagnosis, measurement, or evaluation
5. Mechanism or learning dynamics
6. Counter-belief or negative result
7. Trade-off decoupling or simplification
8. Unification or duality
9. Theory: lens, characterization, or separation
10. Theory: algorithmic primitive
11. Systems or infrastructure
12. Data, benchmark, evaluation, or human artifact
13. Security, watermarking, auditing, or verification
14. Use-inspired, domain, workflow, or agent paper
15. Position or agenda paper
16. Cross-domain adapters for LLM/agents, RL, and CV/multimodal

## 1. Focused Method / Constraint-or-Invariant Fix

### Use when

The method resolves a specific structural conflict, bottleneck, or requirement;
the insight is more important than a broad SOTA claim.

### Thesis form

> Existing methods cannot satisfy **A** without violating **B**. Enforcing or
> exploiting **invariant/constraint C** enables **A** while preserving **B**.

### Introduction moves

1. define the valuable operation/capability;
2. state the structural conflict, not a list of weak baselines;
3. introduce the invariant or requirement;
4. show the minimal operation that satisfies it;
5. preview the matched outcome, attribution, and scope;
6. state claim-shaped contributions.

### Body sequence

```text
problem and requirement
→ design contract
→ overview / geometry
→ operation or objective
→ guarantee or rationale
→ RQ1 decisive utility
→ RQ2 preservation/side effect
→ RQ3 attribution or representation
→ RQ4 transfer/modularity/boundary
```

### Default artifacts

- geometry or overview diagram;
- one defining equation;
- theorem/proposition only if it licenses preservation or correctness;
- matched main table;
- claim-critical intervention/representation analysis;
- boundary/cost figure.

### Missing-evidence triggers

- no matched condition for the two conflicting objectives;
- the proposed constraint is not actually active in experiments;
- deletion ablation cannot distinguish the claimed invariant from extra compute;
- preservation measured on proxies unrelated to the claim.

### Failure mode

A code-module tour followed by twelve ablations, with no explicit requirement
that explains why the design exists.

## 2. Anomaly–Diagnose–Repair

### Use when

The strongest contribution begins with an unexplained artifact, failure mode, or
pathology and ends with a targeted repair.

### Thesis form

> **Phenomenon X** is a systematic consequence of **mechanism/hypothesis Y**;
> introducing **repair Z** removes the predicted behavior and improves
> **consequence C**.

### Introduction moves

1. show the anomaly concretely;
2. establish why it matters beyond aesthetics;
3. characterize where and when it appears;
4. state the diagnosis;
5. introduce the minimal repair;
6. preview downstream consequences.

### Body sequence

```text
phenomenon visualization
→ prevalence and quantitative characterization
→ competing explanations
→ hypothesis-generating analysis
→ targeted intervention
→ downstream evaluation
→ qualitative confirmation and boundary
```

### Default artifacts

- before/after identity figure;
- distribution or localization plot;
- intervention schematic;
- downstream table;
- qualitative panel chosen by a declared rule.

### Missing-evidence triggers

- anomaly shown only in selected examples;
- repair changes multiple factors at once;
- no test where the diagnosis predicts a different outcome from alternatives;
- downstream improvement exists but anomaly removal is not measured.

### Failure mode

Leading with a benchmark improvement and revealing the actual anomaly only late,
which makes the repair look arbitrary.

## 3. New Paradigm / New Factorization / New Capability

### Use when

The paper changes the primitive, factorization, prediction order, supervision
source, or operational formulation and thereby unlocks a capability.

### Thesis form

> Replacing **dominant primitive A** with **primitive B** better matches
> **structure/constraint C**, enabling **capability bundle D**.

### Introduction moves

1. name the dominant formulation and why it was natural;
2. identify the limiting assumption;
3. introduce the alternative primitive in one sentence;
4. make the contrast visually or formally concrete;
5. preview implementation feasibility;
6. preview a coherent bundle: headline outcome, scaling, transfer, or new data
   regime.

### Body sequence

```text
old-vs-new formulation
→ conceptual primitive / factorization
→ implementable model or pipeline
→ headline capability
→ scaling or efficiency
→ transfer/zero-shot/new regime
→ attribution and boundary
```

### Default artifacts

- paradigm contrast diagram as identity anchor;
- formal factorization/definition;
- qualitative outputs when the capability is semantic;
- headline table or frontier;
- scaling/generalization curve;
- ablation on the paradigm-defining choice.

### Missing-evidence triggers

- new terminology but no substantive change in computation or assumptions;
- capability already available under a fair baseline;
- the bundle is a list of unrelated results;
- no evidence that the defining primitive, rather than scale/tuning, causes the
  gain.

### Failure mode

Selling a local architectural tweak as a paradigm without a crisp contrast or
newly unlocked behavior.

## 4. Scalable Diagnosis / Measurement / Evaluation

### Use when

The main product is a valid, scalable way to measure a deployment-relevant or
scientific phenomenon, followed by a consequential finding.

### Thesis form

> Existing evaluation misses **construct X** because **mismatch Y**. Our
> scalable protocol measures X and reveals **finding Z**, which changes
> **decision/implication C**.

### Introduction moves

1. state the deployment/scientific mismatch;
2. explain why existing evaluations cannot answer the question;
3. define the target construct;
4. introduce the scalable simulator/protocol;
5. preview validity and the surprising finding;
6. state who should change what.

### Body sequence

```text
construct and threat-to-validity analysis
→ protocol/simulator construction
→ task and metric selection
→ validation and controls
→ scale/parameter coverage
→ headline finding
→ gradual/intervention tests
→ stakeholder or research implications
```

### Default artifacts

- setting + protocol + finding identity figure;
- construct decomposition or metric table;
- validation/control experiments;
- broad aggregate plots;
- intervention or severity curve;
- implication table by stakeholder/decision when useful.

### Missing-evidence triggers

- proxy construct not linked to the deployment claim;
- simulator changes task difficulty together with interaction structure;
- metric artifacts could produce the finding;
- finding shown on too narrow a model/task sample for its scope;
- no actionable consequence after measurement.

### Failure mode

Presenting a large evaluation suite as contribution without construct validity
or a new conclusion.

## 5. Mechanism / Learning Dynamics / Explanation

### Use when

The paper explains a behavior, training dynamic, or empirical regularity and the
explanation generates testable predictions.

### Thesis form

> Behavior **X** follows from **mechanism/decomposition Y**, which predicts
> **P1–Pk** and enables **mitigation/design consequence Z**.

### Introduction moves

1. name the unexplained behavior;
2. explain why existing aggregate metrics cannot reveal it;
3. define the object of analysis;
4. state the mechanism and its distinguishing predictions;
5. preview formal derivation and empirical verification;
6. preview intervention or design implication.

### Body sequence

```text
definition / decomposition
→ derivation or causal account
→ competing explanations
→ prediction 1 test
→ prediction 2 test
→ intervention/mitigation
→ boundary and remaining hypotheses
```

### Default artifacts

- defining equations;
- mechanism/prediction diagram;
- trajectories or token/component-level diagnostics;
- controlled interventions;
- cross-setting replication;
- mitigation result.

### Missing-evidence triggers

- explanation is written after seeing results but makes no risky prediction;
- only one deletion ablation;
- diagnostics are correlational while language claims causation;
- mitigation works but not for the reason proposed;
- no boundary where the mechanism should weaken or disappear.

### Failure mode

Calling an intuitive story a mechanism because it is consistent with one curve.

## 6. Counter-Belief / Negative Result / Alternative Model

### Use when

The strongest value is correcting a credible field belief, showing a claimed
phenomenon is an artifact, or establishing that an expected benefit does not
hold under a stronger test.

### Thesis form

> The apparent/accepted conclusion **A** is better explained by **B**. B makes
> predictions **P**, which hold across complementary tests; the corrected view
> is **C**.

### Introduction moves

1. state the prior belief fairly and specifically;
2. explain why it is important;
3. identify the ambiguity or alternative model;
4. derive risky predictions;
5. preview complementary tests with independent failure modes;
6. state the corrected view, not merely “A is wrong.”

### Body sequence

```text
reproduce/define target phenomenon
→ alternative mathematical or measurement model
→ predictions
→ direct controlled test
→ broader meta-analysis or independent setting
→ deliberately constructed stress test
→ corrected scope and implication
```

### Default artifacts

- phenomenon figure;
- explanatory model/metric transformation;
- prediction table;
- complementary plots across settings;
- robustness to reasonable analysis choices;
- corrected conceptual diagram or recommendation.

### Missing-evidence triggers

- prior is a strawman;
- alternative can fit any outcome;
- tests share the same hidden confound;
- null result caused by low power or implementation weakness;
- paper stops at criticism and offers no corrected understanding.

### Failure mode

A collection of failed replications without a model that explains when and why
the claim fails.

## 7. Trade-off Decoupling / Simplification / Resurrected Baseline

### Use when

A standard technique couples two objectives, or accepted complexity/flexibility
is unnecessary under the meaningful operating condition.

### Thesis form

> Standard choice **A** improves **X** by sacrificing **Y**. Replacing it with
> simpler choice **B** preserves the useful effect while shifting the
> X–Y frontier.

### Introduction moves

1. establish the ubiquitous technique and benefit;
2. make its hidden cost concrete;
3. introduce the surprising simpler alternative;
4. give toy, geometric, or analytic intuition;
5. preview the frontier rather than one isolated score;
6. state conditions under which simplicity wins.

### Body sequence

```text
trade-off characterization
→ intuition/toy setting
→ simple alternative
→ matched frontier result
→ ablation on simplicity-defining factor
→ qualitative/human confirmation
→ failure regime
```

### Default artifacts

- trade-off or Pareto identity figure;
- toy model/diagram;
- complexity/component comparison table;
- frontier curves;
- qualitative grid when scalar metrics hide diversity/quality.

### Missing-evidence triggers

- baseline not tuned as carefully;
- “simple” method hides external data/compute;
- improvement appears only after selecting one metric;
- no matched-quality or matched-cost view;
- intuition does not predict observed frontier changes.

### Failure mode

Claiming “simple yet effective” without quantifying simplicity or identifying the
coupled cost it removes.

## 8. Unification / Framework / Duality

### Use when

A common abstraction faithfully relates fragmented methods and produces a new
algorithm, theorem, prediction, transfer, or design.

### Thesis form

> Methods **A–C** are instances of **abstraction U**. This view recovers their
> known forms and yields **new leverage L**.

### Introduction moves

1. show the fragmentation and its cost;
2. name the shared mathematical/computational structure;
3. state recoverability of known cases;
4. preview the new algorithm or prediction;
5. instantiate it in a concrete model/system;
6. preview formal and empirical payoff.

### Body sequence

```text
background objects
→ common abstraction
→ equivalence/duality theorem
→ recovered special cases
→ derived efficient algorithm or design rule
→ new instantiation
→ empirical/formal validation
```

### Default artifacts

- equivalence/duality identity map;
- definitions and transformation equations;
- theorem/propositions;
- algorithm derived from the abstraction;
- complexity/assumption comparison table;
- instantiation and benchmark evidence.

### Missing-evidence triggers

- mappings are informal analogies rather than faithful recoveries;
- abstraction adds notation but no leverage;
- new algorithm could have been derived without the framework;
- instantiation is not competitive or does not test the central consequence.

### Failure mode

A taxonomy presented as unification without a theorem, algorithm, prediction, or
transfer benefit.

## 9. Theory: Formal Lens / Characterization / Separation

### Use when

The contribution changes how a class of models/problems should be measured or
understood, often through a new definition, separation, characterization, or
matching bound.

### Thesis form

> Conventional measure **A** cannot distinguish **phenomenon X**. Under lens
> **B**, class **C** has property/bound **D**, while **E** requires **F**; this
> implies **G**.

### Introduction moves

1. state the conceptual question;
2. explain why conventional theory is insufficient;
3. introduce the new formal lens;
4. state the main lower/upper/characterization result in plain language;
5. state matching/tightness or comparison;
6. explain the complexity/scientific consequence and assumptions.

### Body sequence

```text
formal problem and definitions
→ headline theorem(s)
→ proof roadmap
→ lower/separation result
→ upper/matching construction
→ applications/consequences
→ tightness, assumptions, and open boundary
```

### Default artifacts

- theorem/result box as identity anchor;
- one running example if definitions are abstract;
- proof roadmap;
- propositions/lemmas only as interfaces;
- comparison table of assumptions/bounds if it clarifies novelty.

### Missing-evidence triggers

- theorem true but vacuous under realistic parameter ranges;
- assumptions silently stronger than prior work;
- lower and upper bounds incomparable;
- consequence is asserted but not formally derived;
- many named lemmas with no proof-architecture benefit.

### Failure mode

Burying the theorem behind pages of preliminaries or adding decorative
experiments unrelated to the formal claim.

## 10. Theory: Algorithmic Primitive / Procedure Licensed by Theory

### Use when

A new primitive, oracle reduction, estimator, sampler, or auditing procedure
settles an efficiency/statistical question or makes a practical procedure valid.

### Thesis form

> Procedure/primitive **P** achieves **target T** using **resource/query model R**
> with guarantee **G**, improving prior dependence **B** and enabling
> application **A**.

### Introduction moves

1. ask the formal or operational question directly;
2. state the prior barrier;
3. introduce the primitive/procedure at high level;
4. state the main guarantee and improvement;
5. identify the key technical idea;
6. preview refinements/applications or empirical validation.

### Body sequence

```text
question and procedure/primitive
→ just-in-time definitions
→ main theorem
→ proof architecture
→ refinements
→ application corollaries
→ empirical validation when the procedure is operational
```

### Default artifacts

- algorithm/procedure early;
- main theorem;
- query/complexity table;
- proof sketch;
- empirical power/sensitivity or runtime when implementation is claimed.

### Missing-evidence triggers

- resource/oracle model differs materially from practice but is hidden;
- asymptotic gain has no meaningful regime;
- procedure correctness depends on unstated calibration;
- application violates theorem assumptions;
- empirical section tests a different algorithm than the analyzed one.

### Failure mode

Making the reader wait through background before learning the simple operational
idea.

## 11. Systems / Efficiency / Infrastructure

### Use when

The main value is an implementation, runtime, serving/training system,
compiler, scheduler, memory plan, or infrastructure capability.

### Thesis form

> Under **operating point O**, bottleneck **B** prevents **capability C**. System
> insight **S** changes the dataflow/resource allocation and achieves **frontier
> F** at matched quality/correctness.

### Introduction moves

1. define workload and objective;
2. state hardware/software/resource constraints;
3. show the bottleneck with a quantitative example;
4. give the system insight and overview;
5. preview end-to-end frontier/capability;
6. preview attribution, scaling, and unfavorable regimes.

### Body sequence

```text
operating point and bottleneck
→ system overview/dataflow
→ optimizer/scheduler/placement/compression
→ correctness or quality preservation
→ implementation
→ end-to-end evaluation
→ attribution microbenchmarks
→ scaling/overhead/boundary
```

### Default artifacts

- operating-point/Pareto identity figure;
- memory/dataflow diagram;
- algorithm or optimization program when state/placement matters;
- end-to-end table/curve;
- profile/microbenchmark;
- scaling plot.

### Missing-evidence triggers

- hardware, precision, batch, or quality mismatch;
- synthetic microbenchmark but no promised workload outcome;
- end-to-end gain caused by omitted baseline optimization;
- no attribution to claimed dataflow;
- throughput win violates latency or memory target.

### Failure mode

A long component inventory before the reader knows the exact operating point or
end-to-end promise.

## 12. Data / Benchmark / Evaluation / Human Artifact

### Use when

The paper contributes a dataset, benchmark, evaluation protocol, metric,
annotation scheme, participant-linked artifact, or audit infrastructure.

### Thesis form

> Existing artifacts omit **construct/population X**. Artifact **D** captures it
> with **quality/coverage properties Q** and reveals **scientific findings F**
> that existing benchmarks cannot support.

### Introduction moves

1. name the missing construct, population, context, or decision;
2. show why existing artifacts cannot answer it;
3. define the artifact and intended use;
4. state scale, coverage, provenance, or participation design;
5. preview quality/validity safeguards;
6. preview baseline landscape and/or central case studies;
7. state what becomes newly knowable.

### Body sequence

```text
construct and intended use
→ collection/construction/provenance
→ sample/population/coverage
→ annotation/quality/validity/leakage/ethics
→ baseline or descriptive landscape
→ central scientific case study/module 1
→ module 2/3 when each answers a distinct question
→ appropriate use and boundary
```

### Default artifacts

- construct/population identity card;
- data pipeline/schema;
- coverage/composition tables;
- validation and leakage analyses;
- baseline landscape;
- central case studies, not merely examples;
- documentation/ethics table in appendix as appropriate.

### Missing-evidence triggers

- dataset scale without construct validity;
- sample unrepresentative of claimed population;
- leakage or contamination not tested;
- no baseline or scientific use demonstration;
- case studies selected for dramatic outcomes without a rule;
- artifact teaches nothing beyond a new leaderboard.

### Failure mode

Treating data collection as self-justifying and relegating the actual scientific
insight to an appendix.

## 13. Security / Watermarking / Auditing / Verification

### Use when

The paper inserts, detects, audits, certifies, or attacks a signal under an
explicit threat model.

### Thesis form

> Under threat/observation model **M**, procedure **P** creates or detects signal
> **S** with calibrated error **E** and useful power **W**, remaining effective
> under **transformations/attacks A**.

### Introduction moves

1. state the operational threat or audit decision;
2. define what the defender/auditor can observe;
3. give the intervention/procedure in plain language;
4. state the decision statistic or certificate;
5. preview formal calibration/power;
6. preview robustness/attack evaluation and practical implications.

### Body sequence

```text
threat and observation model
→ worked example / procedure
→ decision rule/statistic
→ theorem or statistical analysis
→ sensitivity and power
→ attacks/transformations/adaptive cases
→ operational boundary
```

### Default artifacts

- worked example identity anchor;
- algorithm/procedure;
- test-statistic equation;
- theorem/p-value or privacy guarantee;
- ROC/power/sensitivity plot;
- attack/transformation table.

### Missing-evidence triggers

- false-positive target absent;
- detector power reported without base rate/decision context;
- threat model changes across experiments;
- no adaptive or realistic transformation;
- theoretical signal not connected to implementation.

### Failure mode

Reporting average detectability without a calibrated decision rule or threat
model.

## 14. Use-Inspired / Domain / Workflow / Agent Paper

### Use when

The decisive contribution is tied to a real decision, workflow, stakeholder,
scientific instrument, deployment, or long-horizon process.

### Thesis form

> In workflow **W**, decision bottleneck **B** is not captured by standard task
> metrics. Method/system **M** improves **domain outcome D** under operational
> constraints **C**, as shown by aggregate and process-level evidence.

### Introduction moves

1. describe the authentic decision and cost of failure;
2. explain why standard ML formulation or metric misses it;
3. state domain requirements and current practice;
4. introduce the technical contribution;
5. preview aggregate domain outcome;
6. preview case/process/human evidence;
7. state operational scope and risks.

### Body sequence

```text
workflow and requirements
→ task/metric/decision validity
→ method or system
→ current-practice/non-ML baseline
→ aggregate technical/domain outcome
→ case study, trace, or human-process module
→ errors, constraints, and deployment implication
```

### Default artifacts

- workflow/decision pipeline;
- requirements table;
- aggregate domain metrics;
- time/trajectory/process plots;
- central case study or trace;
- failure taxonomy and operational boundary.

### Missing-evidence triggers

- synthetic task not connected to real workflow;
- no comparison with current practice;
- proxy metric improves but domain decision does not;
- cases are anecdotal and selection is unexplained;
- deployment constraints are assumed away.

### Failure mode

Adding a domain story around a conventional benchmark paper without validating
the actual decision.

---

## 15. Position / Agenda / Perspective Paper

### Use when

The main contribution is a consequential thesis about how the field should
understand, evaluate, prioritize, or build something, supported by evidence and
cases rather than a single new model or theorem.

### Thesis form

> Current practice **P** optimizes or assumes **A**, but evidence **E** shows
> that this misses **B**. The field should adopt **principle or agenda C**,
> beginning with **concrete actions D**.

### Introduction moves

1. state the consequential practice or unresolved decision;
2. identify the blind spot, contradiction, or neglected stakeholder;
3. state the thesis directly;
4. separate factual claims from value judgments;
5. preview the evidence or cases supporting the thesis;
6. preview the strongest counterargument and actionable agenda.

### Body sequence

```text
practice and stakes
→ evidence that the current framing is insufficient
→ proposed lens or principle
→ representative cases or synthesis
→ strongest counterarguments and boundary
→ concrete research/evaluation/design agenda
```

### Default artifacts

- thesis or causal map;
- evidence-synthesis table;
- case comparison selected by a declared rule;
- taxonomy only when categories change a decision;
- action matrix linking recommendations to stakeholders and evidence.

### Missing-evidence triggers

- the criticized position is a strawman;
- recommendations rely on anecdotes without a sampling or synthesis logic;
- factual and normative claims are mixed;
- counterarguments are omitted or represented weakly;
- the agenda is aspirational but not actionable or falsifiable.

### Failure mode

A broad opinion essay that markets urgency without a precise thesis, fair
counterarguments, evidence synthesis, or concrete decisions for the field.

---

## Cross-Domain Adapters

### LLM / Agent / Generative Systems

Check:

- model/version and inference API date;
- prompts, context, tool access, sampling, retries, and selection policy;
- inference budget and number of samples;
- contamination and judge-model dependence;
- task success versus recovery/reliability/process metrics;
- qualitative sample selection;
- cost/latency and safety implications;
- multi-turn or long-horizon state when deployment is interactive.

Agent papers often need trajectory or case evidence in addition to terminal
success, because the process is the claimed capability.

### Reinforcement Learning / Sequential Decision

Check:

- environment steps, wall-clock, seeds, evaluation episodes, and selection;
- training versus evaluation policy;
- reward definition and exploitability;
- performance curves and final summary;
- stability/variance;
- offline-data coverage or action-label assumptions;
- generalization across seeds, tasks, dynamics, or observation/action spaces;
- behavior diagnostics when the thesis concerns exploration or planning.

### Computer Vision / Multimodal

Check:

- qualitative panels have declared selection;
- image/video quality metrics match the semantic claim;
- data filtering and preprocessing are matched;
- compute and resolution are comparable;
- visual anomaly claims include prevalence/quantification;
- new generation paradigms show samples, aggregate quality, efficiency, and
  transfer/scaling when claimed.
