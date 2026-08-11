# Part VI — Section Renderers

Render only after the blueprint is stable. The renderer must preserve the Paper
Contract, proof modules, ordering mode, and wording ceilings.

## Contents

1. Title
2. Abstract by paper family
3. Introduction and contradiction-led openings
4. Related Work
5. Background and Problem Setup
6. Method, Model, or Procedure
7. Systems and Infrastructure
8. Dataset, Benchmark, or Human-Artifact Construction
9. Theory
10. Experiments and Results
11. Discussion and Implications
12. Limitations and Scope
13. Conclusion
14. Paragraph and Sentence Architecture

## 1. Title

The title should identify the contribution or encode the central contrast. It
may market the idea strongly when every word is supportable.

### Useful title functions

- **Name the object and payoff** — `[Method/System]: [capability] under [condition]`
- **State the thesis** — `[Object] [does/is/needs] [surprising conclusion]`
- **Encode the contrast** — `[Old assumption] vs. [new view]`
- **Ask and answer** — `[Question]? [Scoped answer]`
- **Name the formal result** — `[Bound/characterization] for [problem/class]`
- **Name the artifact and discovery** — `[Dataset/Benchmark]: What [construct] reveals about [question]`

### Title tests

- Can a reader infer the paper’s contest?
- Does the memorable noun refer to the real contribution?
- Does an adjective such as `scalable`, `efficient`, `robust`, `general`, or
  `optimal` have a defined condition?
- Is the title stronger than the evidence?
- Would deleting the acronym make the idea clearer?

Avoid `A Novel Approach to...`, `Towards...` when the result is already
established, and titles that name only the application domain while hiding the
technical or scientific thesis.

## 2. Abstract

The abstract is a compressed argument, not a table of contents. It should let a
reader recover:

```text
prior or task
→ contradiction/gap
→ insight or alternative
→ contribution object
→ decisive evidence
→ consequence and scope
```

Use the most decision-relevant number, bound, scale, or finding. Do not list all
datasets, components, or ablations. Do not spend sentences on generic related
work.

### Method / constraint-fix abstract

1. **Task and conflict** — name the valuable capability and the structural
   requirement existing methods violate.
2. **Insight** — state the invariant, decomposition, or design principle.
3. **Method** — name the minimal operation or model at a useful level.
4. **Headline result** — report the matched outcome with condition and number.
5. **Attribution/scope** — say what evidence identifies the source or where the
   result holds.
6. **Consequence** — what capability or design choice changes.

Skeleton:

> **[Capability]** requires **[A]** without sacrificing **[B]**, but existing
> **[class]** couple the two through **[structural reason]**. We show that
> **[insight/invariant]** permits **[operation]**, yielding **[method]**. Under
> **[matched conditions]**, it **[headline result]**. **[Diagnostic/formal
> evidence]** attributes the gain to **[claim]**, and **[scope result]** shows
> **[boundary/generalization]**. These results enable **[implication]**.

### Diagnosis / discovery abstract

1. deployment/scientific mismatch;
2. construct or phenomenon;
3. scalable/valid measurement or characterization;
4. main finding;
5. mechanism/intervention or complementary confirmation;
6. implication for a named stakeholder or research belief.

Do not lead with the proposed fix when the anomaly is the contribution.

### Counter-belief / negative-result abstract

1. state the accepted belief;
2. identify the ambiguity or alternative model;
3. state predictions that distinguish it;
4. summarize complementary tests;
5. state the corrected view;
6. explain why the correction matters.

Avoid a triumphant “prior work is wrong” tone. Make the alternative model and
scope more memorable than the criticism.

### Theory abstract

1. ask the formal question or state the unresolved bound;
2. name the model, assumptions, and prior dependence;
3. state the main theorem in plain language and notation only when essential;
4. identify the key construction/technical idea;
5. state matching/tightness/refinements or applications;
6. state the conceptual or algorithmic consequence.

The main theorem should be recognizable without reading the paper.

### Systems abstract

1. define the operating point and workload;
2. quantify or name the bottleneck;
3. state the system/dataflow insight;
4. name the implementation/optimizer/scheduler;
5. report end-to-end performance at matched quality/correctness and hardware;
6. state the capability/frontier and relevant boundary.

Do not report throughput without the latency, batch, quality, precision, and
hardware context required to interpret it.

### Data / benchmark / human-artifact abstract

1. identify the missing construct, population, or interaction context;
2. state why existing data cannot answer the question;
3. describe the artifact, scale, population, and collection design;
4. state quality/coverage/validity features;
5. preview baseline landscape or central case studies;
6. state the new scientific insights and intended use.

The abstract must explain what becomes knowable, not merely that the dataset is
large.

### Security / auditing abstract

1. state the threat or audit decision;
2. describe the intervention/procedure;
3. state the decision statistic/certificate;
4. state calibration or formal guarantee;
5. report power/sensitivity/attack results;
6. state operational scope.

### Use-inspired abstract

1. authentic workflow and decision;
2. why standard task/metric is insufficient;
3. technical contribution;
4. domain-valid aggregate result;
5. process/human/case evidence;
6. operational implication and constraint.

### Abstract audit

For every sentence, write its job in the margin. Delete a sentence whose only
job is `sounds impressive`. Check:

- no contribution is an activity such as “we conduct extensive experiments”;
- every number has a comparison and condition;
- every causal/mechanistic verb is licensed;
- the final sentence states an implication, not a generic future promise;
- the abstract and main evidence spine have the same order.

## 3. Introduction

The Introduction should make the paper feel necessary, plausible, and easy to
navigate before technical detail.

### Universal move sequence

The following moves may occupy one or several paragraphs; do not force one
sentence per move.

1. **Prior and stakes** — establish the specific practice, lens, or capability.
2. **Contradiction** — show what it cannot explain, measure, or achieve.
3. **Structural reason** — explain why this is not fixed by another generic
   component or more tuning.
4. **Key insight** — give the paper’s conceptual answer in plain language.
5. **Contribution object** — state what was built, proved, measured, or studied.
6. **Evidence preview** — preview the 1–3 proof modules and decisive artifacts.
7. **Contribution claims and scope** — claim-shaped bullets or prose that maps
   directly to the body.

The first three moves establish why; the next two establish what; the final two
establish why the reader should believe and care.

### Contradiction-first opening patterns

```text
[Practice/model class] has become [dominant/valuable] because [benefit].
Yet [specific observation or requirement] is incompatible with [assumption].
```

```text
Most work trains or evaluates [system] under [setting A].
Deployment instead requires [setting B], where [unresolved behavior] matters.
```

```text
[Feature] is commonly treated as the source of [advantage].
We find that under [important condition], the same feature causes [failure].
```

```text
Existing methods avoid the cost in [dimension A] or [dimension B], but their
complexity remains prohibitive when both are large.
```

```text
Claims of [phenomenon] rely on [measurement choice].
Because this choice is [nonlinear/discontinuous/biased], it cannot distinguish
[true change] from [artifact].
```

### Key-insight paragraph

The key-insight paragraph should answer:

- What is the one conceptual move?
- Why was it not obvious from the dominant formulation?
- How does it resolve the contradiction?
- What does it permit the method/theorem/study to do?

Useful logic:

```text
The obstacle arises because [cause].
This suggests [insight].
We operationalize the insight through [object/procedure].
The resulting [property] should yield [prediction/payoff].
```

Do not fill this paragraph with implementation details or all component names.

### Evidence-preview paragraph

Preview the paper as proof modules, not a benchmark list:

> We establish the claim in three steps. First, **[module 1 conclusion]** using
> **[artifact]**. Second, **[module 2 conclusion]** by **[diagnostic/formal
> evidence]**. Third, **[module 3 conclusion]**, which delineates **[scope or
> implication]**.

The preview may mention one or two decisive numbers/theorems. It should let the
reader predict the Results structure.

### Contribution statements

Write contributions as refutable claims:

Weak:

- We propose a novel framework.
- We conduct extensive experiments.
- We provide useful insights.

Stronger:

- We identify **[failure]** and show that it is concentrated in **[condition]**,
  rather than being explained by **[alternative]**.
- We introduce **[operation]**, which enforces **[invariant]** without changing
  **[resource/quality condition]**.
- Across **[scope]**, the method **[exact outcome]** at matched **[constraint]**.
- We prove **[formal statement]**, closing **[specific gap]** under
  **[assumptions]**.

Every contribution claim must map to a proof module and a main artifact.

### Introduction by archetype

- **Anomaly/repair:** show the phenomenon early, then diagnosis, then remedy.
- **Theory:** state the formal question and main result before a long survey.
- **Systems:** define operating point and bottleneck before system components.
- **Data/human:** foreground the missing construct/population, not file size.
- **Counter-belief:** represent the prior fairly, then give the alternative and
  predictions.
- **New paradigm:** make old-vs-new formulation concrete before implementation.

### Introduction anti-patterns

- generic history of the field;
- a list of every prior method family before stating the problem;
- project chronology;
- three generic “challenges” invented to match three components;
- contribution bullets that name activities;
- an evidence preview stronger than the body;
- a paragraph of limitations before the reader has accepted the contribution;
- vague claims that the method is “simple, general, and effective” without
  specifying each property.

## 4. Related Work

Related Work establishes novelty and comparison, not completeness of citation
coverage.

Build an internal contrast matrix:

| Closest work/class | Shared goal | Different assumption/object | Consequence for capability/evidence | Comparison in paper |
|---|---|---|---|---|

Render by conceptual relation:

```text
shared goal
→ closest approach
→ exact structural difference
→ why that difference matters for the paper's claim
```

Prioritize the closest alternatives. Do not attack earlier work or use vague
phrases such as “few works have explored.” Verify every citation.

Related Work may appear before method, after method, or near the end depending on
reader dependencies. Put essential contrast in the Introduction even when the
full section comes later.

## 5. Background and Problem Setup

Include only what later claims require:

- task/decision/formal problem;
- inputs, outputs, population, and operating point;
- assumptions and notation;
- evaluation contract and main metrics;
- prior result or system fact used by the contribution.

End with the unresolved requirement or formal question. Do not turn Background
into a general tutorial.

Use a running example when it materially reduces notation or makes a formal
object concrete. State explicitly that it illustrates rather than proves.

## 6. Method / Model / Procedure

A method section is an argument for design, not documentation of source files.

### Start with a design contract

```text
Input:
Output:
Requirement/bottleneck:
Invariant or design principle:
One-sentence operation:
Assumptions:
Expected effect/prediction:
```

### Default method sequence

```text
requirements
→ overview / conceptual diagram
→ formal object or objective
→ components/stages in dependency order
→ operational procedure if state/order matters
→ guarantee, complexity, or design rationale
→ implementation/reproducibility details needed for interpretation
```

### Component-subsection microstructure

For each component:

1. **Why needed** — which requirement or failure does it address?
2. **What it does** — equation, operation, or dataflow.
3. **Why this form** — intuition, invariant, or trade-off.
4. **Interface** — what it consumes and passes to the next component.
5. **Claim created** — what later experiment or theorem will test.

Do not write `Encoder`, `Loss`, `Training` as isolated code modules unless that
order also explains the idea.

### Equation, diagram, and algorithm coordination

- diagram: components, interfaces, conceptual sequence;
- equation: objective, estimator, invariant, or relationship;
- algorithm: exact stateful/iterative procedure;
- prose: rationale, conditions, and interfaces.

Do not repeat the same content in all four.

### Algorithm placement

Place pseudocode near the first place exact state/order matters. It should expose
inputs, outputs, maintained state, decision-critical steps, stopping/branching,
and complexity/invariants. Do not include a standard training loop whose only
novelty is one loss term.

### Method wording

Prefer requirement-linked sentences:

> To prevent updates from altering representations used by preserved facts, we
> project the edit onto **[space]** before applying **[operation]**.

Avoid component announcement without rationale:

> Next, we introduce our projection module.

## 7. System / Infrastructure Section

Start with the operating point:

```text
Workload:
Latency/throughput objective:
Hardware and memory hierarchy:
Precision/batch/sequence/model scale:
Output-quality or correctness target:
Baseline implementation level:
```

Then:

1. quantify the bottleneck;
2. show the end-to-end dataflow;
3. explain placement, scheduling, compression, compilation, or optimization;
4. state correctness/quality preservation;
5. describe implementation details required for comparison;
6. defer evaluation to an end-to-end-first Results sequence.

Do not open with a component inventory.

## 8. Dataset / Benchmark / Human-Artifact Construction

Use:

```text
construct and intended use
→ target population / source universe
→ sampling and recruitment
→ collection or generation protocol
→ annotation/interaction design
→ quality and validity
→ coverage and missingness
→ leakage/contamination
→ ethics, consent, governance, and release
```

Separate **construction evidence** from **scientific analyses enabled by the
artifact**. The latter often deserve their own proof modules or case-study
sections.

A coverage table should show dimensions relevant to the claim, not every
metadata field. A participant-linked dataset must describe who is represented
and who is not.

## 9. Theory

### State the product early

Give the formal question, assumptions, main theorem, and plain-language
consequence before lengthy proof machinery.

### Main-theorem block

```text
Problem/model:
Assumptions:
Statement:
Improvement or separation from prior work:
Interpretation:
Consequence:
```

### Proof exposition

1. give a proof roadmap;
2. identify the two to four conceptual steps;
3. introduce propositions/lemmas only as stable interfaces;
4. say where each assumption enters;
5. keep the key insight in the main text;
6. move routine, standard, or orthogonal technical work to the appendix;
7. include a complete proof somewhere.

Use a lemma when it reduces the reader's active dependency state. Do not name
every algebraic step.

### Theory plus experiments

Add experiments only when they:

- demonstrate a formal consequence;
- test tightness or a predicted regime;
- show the analyzed procedure is operational;
- connect the abstraction to a real phenomenon.

Do not add benchmark experiments merely because neighboring papers have them.

## 10. Experiments and Results

### Begin with an evaluation contract

State once:

```text
Claims/RQs tested:
Datasets/tasks/populations:
Baselines and comparison classes:
Metrics and why they match the claims:
Resource/protocol controls:
Seeds/runs/uncertainty:
Selection policy:
```

Keep only the details required to interpret the main results. Put exhaustive
reproducibility in the appendix.

### Organize by proof modules or reader questions

Do not organize by the chronological order of experiments or default dataset
names. Choose the ordering mode from Part II.

### Result-paragraph pattern

```text
claim/question
→ diagnostic design
→ exact artifact readout
→ calibrated conclusion
→ implication/next doubt
```

Good artifact reference:

> In the low-label region of Figure 4, the proposed estimator reduces calibration
> error while the accuracy curves remain overlapping; the advantage disappears
> once labels exceed **[threshold]**. The result therefore supports a low-data
> calibration claim, not a universal accuracy claim.

Weak artifact reference:

> Figure 4 shows the results, and our method performs well.

### Main comparison

The main comparison should make the contest legible:

- group protocol-matched methods together;
- separate unmatched external-data/compute settings;
- highlight only cells relevant to the claim;
- state uncertainty;
- direct attention to the exact row/column or curve region;
- report cost/quality parity when necessary.

### Ablations

Admit an ablation only if it distinguishes a design claim or alternative.
Prefer replacement controls or interventions over deletion when deletion breaks
several functions. Keep one or two claim-critical ablations in the main text;
move knob inventories to the appendix.

### Generalization and robustness

Use independently motivated settings. Show heterogeneity rather than only an
average. If the strongest result is regime-specific, make the regime the claim
instead of apologizing that it is not universal.

### Qualitative results and cases

State selection policy before the panel or case. Tell the reader what semantic
behavior to inspect. Pair with aggregate evidence when claiming prevalence or
superiority. Treat a case as central when the research question concerns
process, context, heterogeneity, or workflow.

### Stop rule

Stop the Results section when:

- every central proof module is closed;
- the strongest alternative is addressed;
- material scope/cost is visible;
- further results would only repeat the belief update.

## 11. Discussion and Implications

A Discussion is useful when the established results change several scientific,
engineering, stakeholder, or policy decisions. Organize by consequence, not by
repeating Results.

Possible moves:

```text
what the evidence changes
→ which prior explanation/practice should be revised
→ what design or evaluation follows
→ what remains unresolved
```

Do not use Discussion to introduce unsupported mechanism stories.

## 12. Limitations and Scope

Keep this section precise and proportionate. Include:

- tested models/tasks/populations/assumptions;
- material untested generalizations;
- known failure regimes or counterexamples;
- resource, data, human, deployment, or governance constraints;
- risks directly connected to the contribution.

Use fact → claim consequence:

> Evaluation uses English multi-turn tasks and five commercial model families;
> the findings therefore establish interaction sensitivity in this setting but
> do not characterize multilingual dialogue.

Do not write a broad self-critique, speculate about every possible weakness, or
repeat minor null results. The main text should already frame the correct
scope.

## 13. Conclusion

The conclusion completes the promise stack:

1. restate the question or contradiction;
2. give the answer/thesis;
3. name the decisive evidence at a higher level;
4. state the consequence;
5. optionally state one concrete unresolved direction created by the result.

Do not repeat the full contribution list, introduce new results, or end with
“more work is needed” as the main message.

## 14. Paragraph and Sentence Architecture

### Paragraph roles

A paragraph should normally have one dominant job:

- establish prior/context;
- expose contradiction;
- explain insight;
- define object;
- report evidence;
- interpret evidence;
- establish scope;
- transition to next question.

Typical evidence paragraph:

```text
topic claim
→ design/protocol
→ exact evidence
→ interpretation
→ consequence/transition
```

Do not force every paragraph to have the same length or a mechanical summary
sentence.

### Logical connectors

Use connectors that name the relation:

- contrast: `however`, `by contrast`, `whereas`;
- cause: `because`, `therefore`, `as a result`;
- scope: `under`, `within`, `for`, `when`;
- evidence: `Table 2 isolates`, `Figure 4 shows`, `Theorem 1 establishes`;
- transition: `This leaves the question of...`, `We next test whether...`.

Avoid chains of `Moreover`, `Furthermore`, and `Additionally` that merely append
facts.

### Calibrated verbs and modals

- use `does`, `reduces`, `enables`, or `establishes` when directly shown;
- use `can` for capability/existence, not as a weak substitute for `does`;
- use `may` only for genuine uncertainty or possibility;
- use `suggests` for incomplete explanation;
- use `consistent with` when alternatives remain;
- use `causes`, `drives`, or `mechanism` only with identifying evidence.

### Specificity test

Delete or rewrite a sentence that could survive unchanged after replacing the
method, dataset, and result with unrelated ones.

Weak:

> These results highlight the effectiveness and robustness of our approach.

Stronger:

> The gain persists across all four domain shifts and remains within one point
> after halving the adaptation set, indicating that it does not depend on the
> full target-domain sample.
