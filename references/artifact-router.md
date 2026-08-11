# Artifact Routing

## Contents

1. Representation router by reader task
2. Pairing rules for complementary artifacts
3. Main-text, appendix, rerun, or drop decisions

## 11. Artifact Router — Choose the Representation by Reader Task

The research object does not dictate the artifact. The reader task does.

### 11.1 Prose-only result

Use prose when:

- the result is one simple fact or one to two numbers;
- no comparison pattern, distribution, sequence, or geometry must be inspected;
- a visual would cost more attention than it saves.

Do not create a one-row table or decorative chart merely to make the paper look
empirical.

### 11.2 Equation

Use an equation when it compactly defines:

- an objective, estimator, update, invariant, probabilistic model, or relation;
- a quantity repeatedly referenced later;
- a relationship whose structure matters more than a procedural sequence.

Do not use decorative formalism to make an intuitive heuristic look deeper.
Every displayed equation must be interpreted and used.

### 11.3 Definition

Use a formal definition when a new construct:

- is central to the contribution;
- will be used repeatedly;
- has boundary cases that prose would leave ambiguous;
- determines what is measured or proved.

A standard term used once usually needs a sentence, not a numbered definition.

### 11.4 Architecture, workflow, or conceptual diagram

Use a diagram when the reader must understand:

- components and information flow;
- system boundaries or interfaces;
- temporal or causal sequence at a conceptual level;
- a paradigm contrast;
- a measurement model or hypothesis that produces predictions.

A diagram answers **what connects to what**. It does not replace an algorithm
when exact operational order, branching, or state updates matter.

### 11.5 Data figure

Use a figure when the reader must see a relationship rather than look up values:

- trend, scaling law, learning curve, or sensitivity;
- distribution, variability, or heterogeneity;
- interaction between factors;
- calibration or error structure;
- quality–cost or accuracy–latency frontier;
- spatial, temporal, or geometric pattern;
- qualitative output structure;
- a failure region or phase transition.

Choose the plot family by the question:

| Question | Usually suitable representation |
|---|---|
| How does an outcome change along an ordered variable? | line curve with uncertainty |
| What is the trade-off among methods? | scatter/Pareto plot |
| How variable or heterogeneous are outcomes? | ECDF, interval plot, box/violin with raw points when feasible |
| Do two factors interact? | faceted curves or heatmap; use a table if exact cells dominate |
| How are errors distributed across classes/types? | confusion/error matrix or categorized bars |
| Does confidence match accuracy? | reliability/calibration plot |
| What semantic behaviors occur? | qualitative grid with declared selection policy |
| Where does a method fail? | boundary map, stratified error plot, or failure taxonomy |

A figure must have one sentence that states its main message. If exact numerical
lookup is important, provide labels or a table elsewhere.

### 11.6 Table

Use a table when the reader must compare or retrieve exact discrete values:

- methods × datasets/tasks × metrics;
- ablation variants with exact deltas;
- assumptions, guarantees, and complexity across methods;
- dataset composition or protocol differences;
- fitted coefficients, hyperparameters, or projections;
- category counts and exact rates.

Do not use a giant table as a substitute for deciding the paper's claim. Group
rows by comparison class, visually prioritize the claim-relevant cells, and move
exhaustive secondary metrics to the appendix.

### 11.7 Figure versus table decision

Use this decision:

```text
Need exact lookup across discrete cells?                 -> table
Need pattern, shape, trend, distribution, or trade-off? -> figure
Need both for distinct reader tasks?                    -> figure in main,
                                                          full exact table in appendix
Need only one or two values?                            -> prose
```

Do not duplicate a figure and table in the main text unless each performs a
separate job.

### 11.8 Algorithm / pseudocode

Include an algorithm only when all of the following are true:

1. the operational procedure is scientifically relevant, not merely an
   implementation detail;
2. order, state, iteration, branching, or update timing affects the method;
3. equations, prose, and a diagram would leave the procedure ambiguous;
4. the algorithm improves understanding, reproducibility, or the statement of a
   guarantee.

An algorithm should expose:

- inputs and outputs;
- maintained state;
- novel or decision-critical steps;
- stopping or branching conditions;
- links to the equations it executes;
- relevant complexity or invariants.

Do not include pseudocode for a standard training loop with only a changed loss;
an objective equation and one paragraph are usually better. Put low-level
engineering pseudocode in the appendix or code unless it is a systems
contribution.

### 11.9 Theorem

Use a theorem when the formal statement is a top-level scientific promise:

- a guarantee, characterization, impossibility, bound, equivalence, convergence
  result, or formal explanation central to the paper;
- assumptions are explicit and meaningful;
- the conclusion changes understanding, design, or what can be claimed;
- a complete proof exists.

State the main theorem early enough to orient the paper. Give intuition and a
proof roadmap in the main text when the theorem is central. The full proof may
move to the appendix when venue constraints require it, but the main text must
still make the result intelligible.

Do not call an empirically observed regularity a theorem. Do not elevate a
technically true but vacuous statement to manufacture theoretical weight.

### 11.10 Proposition

Use a proposition for a nontrivial standalone formal result that supports the
main theorem or establishes a secondary guarantee. Promote a long, important
technical fact to a proposition when doing so lets the reader treat it as a
stable interface.

Move a standard or orthogonal proposition and its proof to the appendix when its
proof would interrupt the main argument.

### 11.11 Lemma

Use a lemma when it:

- isolates a reusable fact used in one or more later proofs;
- localizes technical complexity so the reader can forget its internals after
  accepting the statement;
- names an invariant or reduction that clarifies the proof architecture;
- shortens the reader's active dependency state.

Keep a lemma close to its use when it is local. Merge routine single-use steps
into the surrounding proof. Move a cluster of standard technical lemmas to the
appendix. A lemma is a proof interface, not decoration.

### 11.12 Corollary

Use a corollary only for a direct consequence of an established theorem that is
important enough to surface separately—often because it connects the formal
result to a familiar setting, design rule, or empirical implication.

### 11.13 Proof sketch

Use a proof sketch in the main text when:

- the formal result is central;
- the proof reveals the key insight or dependency structure;
- the full proof is too long for the main argument.

A proof sketch must identify the real steps and where assumptions enter. It is
not a vague assertion that details are routine. Pair it with a complete proof in
the main paper or appendix.

### 11.14 Example

Use an example to:

- make a definition concrete;
- show how an algorithm operates;
- build intuition for a theorem or failure mode;
- orient the reader before abstraction.

An example may be deliberately simple or illustrative, but label it accordingly.
It does not establish prevalence, average performance, or generalization.

### 11.15 Qualitative example panel

Use a qualitative panel when semantic or structured behavior is central and a
scalar metric is insufficient. Declare how examples were selected:

- random;
- stratified by a pre-specified factor;
- representative under a stated criterion;
- critical or boundary cases;
- successes and failures under a balanced rule.

Do not present only aesthetically pleasing outputs. For a broad performance
claim, pair the panel with aggregate evidence.

### 11.16 Error analysis

Use systematic error analysis when the paper needs to establish:

- which failure types dominate;
- whether errors support or contradict the proposed explanation;
- where deployment or generalization breaks;
- what future method should target.

Define the sampling frame, coding scheme, and denominators. A handful of
memorable failures is an illustration, not an error analysis.

### 11.17 Case study

Use a case study when the central reader question is **how, why, or under what
context a complex behavior unfolds**, and aggregate metrics erase the relevant
process or context.

A credible case study card contains:

```text
Case-study question:
Unit of analysis:
Selection policy: random / stratified / typical / critical / extreme / failure
Why this policy matches the question:
Context and timeline:
Evidence sources:
Analysis or annotation procedure:
Triangulation or independent judgment:
Finding:
Claim it can support:
Claim it cannot support:
```

Use:

- random cases to understand typical realized behavior without author selection;
- stratified cases to cover pre-specified regimes;
- critical or failure cases to expose a boundary or mechanism;
- extreme cases to study process, not prevalence;
- longitudinal cases when sequence and adaptation matter.

A case study should complement aggregate evidence when the paper makes a
population-level frequency or superiority claim. It may serve as a **central
proof module**—rather than supplementary color—when the thesis concerns a
construct, heterogeneous human preference, workflow, longitudinal process,
agent trajectory, deployment decision, critical mechanism path, or existence/
feasibility claim. In those cases, credibility comes from the case question,
selection logic, complete evidence trail, and analysis protocol.

### 11.18 Ablation

Include an ablation when a component, data source, loss term, or design choice is
part of the paper's causal or design claim. Ask:

- What alternative explanation does this ablation distinguish?
- Is removal a meaningful intervention, or does it break the system in many
  uncontrolled ways?
- Is a replacement control more diagnostic than deletion?
- Does the main text need the result to understand the source of the gain?

Keep only claim-critical ablations in the main text. Move knob-by-knob inventory
to the appendix. Do not infer a mechanism from one deletion result.

### 11.19 Sensitivity and robustness analysis

Put sensitivity in the main text when the central claim includes:

- stability across a disputed or operationally important parameter;
- low tuning burden;
- robustness to scale, noise, shift, or severity;
- a threshold, phase transition, or boundary that changes interpretation.

Move ordinary hyperparameter sweeps to the appendix when they only document
implementation choices.

### 11.20 Failure or boundary analysis

Put failure evidence in the main text when it:

- materially changes the scope of a central claim;
- reveals the source of success or failure;
- affects deployment or scientific interpretation;
- supplies a counterexample to an overbroad theorem or intuition.

Put an exhaustive failure catalogue in the appendix. Drop trivial or
uninterpretable failures that do not change a claim.

## 12. Artifact Pairing Rules

Pairs are useful only when their jobs differ:

| Pair | Distinct jobs |
|---|---|
| Architecture diagram + algorithm | what connects to what + exact operational procedure |
| Equation + algorithm | objective/relationship + execution order/state |
| Algorithm + theorem | procedure + guarantee or complexity |
| Figure + table | pattern/trend + exact lookup |
| Main comparison + ablation | outcome + source of outcome |
| Aggregate result + case study | breadth/prevalence + contextual depth/process |
| Theorem + counterexample/lower bound | guarantee + boundary/tightness |
| Benchmark landscape + qualitative cases | population-level capability + semantic interpretation |

Do not pair artifacts merely because a conventional paper often contains both.

## 13. Main Text, Appendix, or Drop Router

### Main text

Place an item in the main text when at least one is true:

- removing it breaks understanding of the central object or claim;
- it is the decisive evidence or main theorem;
- it establishes comparison fairness or measurement validity;
- it rules out the strongest plausible alternative explanation;
- it materially changes claim scope, cost, or risk;
- it is the minimum protocol detail needed to interpret the result.

### Appendix or supplement

Place an item in the appendix when it is needed for:

- full reproducibility or audit;
- complete proofs after an intelligible main-text statement/sketch;
- exhaustive per-dataset, per-class, per-prompt, or per-seed values after the
  main pattern is established;
- secondary baselines and metrics;
- non-claim-changing sensitivity checks;
- additional qualitative examples;
- standard technical derivations;
- implementation, prompt, data, or annotation detail too long for the main
  argument.

### Drop

Drop an item when:

- it has no claim role;
- it repeats a stronger artifact;
- its protocol is too weak for any useful interpretation;
- it is post-hoc noise without a declared analysis purpose;
- it is exploration history with no scientific lesson;
- the reader's belief, confidence, scope, or decision would not change if it
  vanished.

Use the deletion test:

> If this artifact disappears, which claim becomes harder to understand,
> believe, scope, reproduce, or act on?

If the answer is “none,” remove it.
