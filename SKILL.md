---
name: ml-paper-writing
description: Convert machine-learning research materials into a strategically positioned, well-organized paper and research-completion plan. Use for selecting the strongest paper story; organizing claims into proof modules; deciding what belongs in prose, equations, figures, tables, algorithms, theorems, examples, cases, the appendix, a new experiment, or nowhere; planning missing evidence; drafting or revising titles, abstracts, introductions, related work, methods, theory, systems, experiments, captions, limitations, and conclusions; compressing papers; removing generic AI or defensive prose; and reviewer red-teaming across empirical ML, CV, NLP/LLM/agents, RL, theory, systems, data/benchmark, security, human, and use-inspired work.
---

# ML Paper Writing: Research-to-Paper Compiler

## Mission

Turn the available research into the strongest coherent paper the evidence can support. Treat the paper as an academic launch: optimize acceptance, attention, memorability, and useful community insight instead of distributing space evenly across the project.

Produce two coupled outcomes when building a full paper:

1. a **paper program**: thesis, proof modules, artifact sequence, section logic, and prose;
2. a **research-completion program**: the missing experiments, proofs, controls, or analyses that would materially strengthen or change the paper.

Do not write a project report, experiment diary, generic template, or self-rejection memo.

## Preserve the Scientific Floor

Use aggressive narrative selection and positive marketing. Do not confuse editorial selection with evidentiary manipulation.

1. Never invent results, numbers, citations, proofs, methods, protocols, or causal explanations.
2. Never suppress a fact that would make the headline claim materially false or misleading.
3. Never imply a fair rank from unmatched data, compute, model access, tuning, inference, hardware, population, or assumptions.
4. Never infer a mechanism from a non-identifying ablation alone.
5. Never present a selected example as population-level evidence.
6. Change the claim, winning axis, proof module, or story when central evidence contradicts it.
7. Preserve correctness qualifiers during rewriting and compression.

Apply the materiality test:

> Would a reasonable reviewer substantially change their interpretation, scope, or confidence in the headline claim after seeing the omitted fact?

If yes, disclose it. If no, it need not occupy the main narrative.

## Keep One Canonical Internal State

Maintain only four objects by default. Keep them compact and use them internally unless showing them helps the user make a decision.

### 1. Research Inventory

Separate verified observations, interpretations, aspirations, contradictions, and missing information. Preserve a source path or artifact for every important number and citation.

### 2. Paper Contract

Lock:

```text
Target reader and venue:
Reader's prior or current practice:
Contradiction, bottleneck, or missing capability:
Key insight:
Contribution object:
Dominant thesis:
Winning axis and comparison class:
Operating conditions or assumptions:
Decisive evidence:
Scope and claims not made:
Five-minute memory sentence:
```

Use this identity form:

```text
For [task or setting], [insight or design] enables or establishes
[capability or conclusion] under [conditions], supported by [decisive evidence].
```

### 3. Proof Modules and Claim–Evidence Ledger

Use one dominant thesis and normally one to three proof modules. Define each module by:

```text
Reader question:
Claim:
Why the claim is necessary for the thesis:
Required evidence:
Available evidence:
Strongest alternative explanation:
Wording ceiling:
Closure: closed | partial | open | contradicted
```

Map every central claim in the title, abstract, introduction, headings, captions, results, and conclusion to a proof module and evidence source.

### 4. Artifact and Section Spine

Order the smallest set of artifacts and sections that closes the proof modules:

```text
reader state before
→ question
→ artifact or formal statement
→ exact readout
→ licensed belief update
→ next doubt
```

Let this spine determine section order. Do not default to a result dump organized by dataset names or experiment chronology.

## Create Optional Objects Only When Triggered

- Generate a **Candidate Story Portfolio** only when two or more credible paper identities compete.
- Build a **Missing-Evidence Matrix** only when important modules remain open or the user asks what research to run next.
- Design an **Identity Anchor** and full **Artifact Storyboard** for full-paper planning or when the core idea lacks a memorable visual/formal object.
- Expand the **Promise Stack** when integrating or auditing title, abstract, introduction, identity anchor, and conclusion.
- Fill the complete reusable blueprint only when the user asks for a full blueprint or when a broad research workspace is too complex for the compact state.

Do not expose a large stack of planning tables merely to demonstrate process.

## Load References Selectively

Do not read every reference by default. Load only the bundle required by the request.

### Reference map

- Read [strategy.md](references/strategy.md) for story selection, positioning, winning-axis decisions, scientific wording, or a full paper build.
- Read [argument-architecture.md](references/argument-architecture.md) for contribution archetypes, result-order selection, or a full paper build.
- Read [compiler-core.md](references/compiler-core.md) for research-folder inspection, candidate stories, proof modules, evidence ledgers, or missing-evidence planning.
- Read [artifact-router.md](references/artifact-router.md) when choosing among prose, equations, diagrams, plots, tables, algorithms, formal statements, examples, error analyses, ablations, and cases.
- Read [artifact-storyboard.md](references/artifact-storyboard.md) for identity anchors, captions, main-text evidence spines, section order, or full-paper planning.
- Read [paper-blueprints.md](references/paper-blueprints.md) when the contribution type determines the paper architecture: method, anomaly, paradigm, measurement, mechanism, counter-belief, simplification, unification, theory, systems, data, security, domain, agent, or position work.
- Read [paper-blueprint-template.md](references/paper-blueprint-template.md) only when producing the complete fillable research-to-paper blueprint.
- Read [section-renderers.md](references/section-renderers.md) when drafting or revising a specific section or converting a stable blueprint into prose.
- Read [marketing-quality.md](references/marketing-quality.md) for mixed results, non-defensive writing, de-AI editing, comparison framing, or compression.
- Read [operating-modes-audits.md](references/operating-modes-audits.md) for reviewer red teams, consistency audits, artifact-only reads, final submission checks, or mode-specific output contracts.

### Common bundles

- **Full paper from research materials**: strategy → argument architecture → compiler core → relevant paper blueprint → artifact storyboard → section renderers → marketing quality → final audits.
- **Choose the story**: strategy → argument architecture → compiler core.
- **Plan experiments or evidence**: compiler core → relevant claim pack in argument architecture or paper blueprints → artifact router.
- **Plan figures/tables/formal objects**: artifact router → artifact storyboard.
- **Draft or revise one section**: section renderers → marketing quality. Infer the compact Paper Contract internally; return prose first.
- **Review or compress**: marketing quality → operating modes and audits.

## Use the Fast Operating Protocol

For a full paper or major restructuring:

1. Inspect all available research before selecting the story.
2. Generate competing stories only when the material genuinely supports alternatives.
3. Choose the story with the best combination of importance, contrast, evidence, diagnosticity, compressibility, audience fit, closure, and risk.
4. Name the meaningful contest, winning axis, comparison class, conditions, and why that contest matters.
5. Compile the thesis into one to three proof modules.
6. Order modules by the reader's largest current doubt: impact-first, validity-first, diagnosis-first, mechanism-first, theorem-first, construct-first, operating-point-first, or procedure-first.
7. Route every admitted result to the representation that best serves the reader's task.
8. Create empty key artifacts or theorem statements before prose; let missing cells and clauses expose missing research.
9. Build the minimum closed artifact and section spine.
10. Draft from the spine, then align the promise stack and run audits.
11. Stop when every central claim is closed and additional evidence no longer changes a reasonable reader's belief.

## Select and Market the Story Aggressively

Prefer the most publishable value, including:

- a new capability, task, dataset, benchmark, or evaluation view;
- a contradiction, corrected belief, or negative result;
- a structural insight, mechanism, theorem, or unification;
- better performance under matched conditions;
- weaker assumptions or less supervision;
- a better cost, data, memory, latency, quality, calibration, robustness, or controllability frontier;
- a simpler method that removes an unnecessary coupling;
- a scalable measurement or operational workflow previously unavailable.

Then:

1. Make the winning condition and advantage explicit; do not expect reviewers to infer them from tables.
2. Lead with the regime, metric, use case, or formal consequence that best expresses the contribution.
3. Select diagnostic main-text experiments, representative teaching examples, and the shortest complete argument.
4. Move exhaustive grids, secondary datasets, full protocols, and reproducibility material to the appendix.
5. Omit debugging history, obsolete implementations, redundant results, and abandoned chronology.
6. Do not make a dimension the paper's competition when it does not express the work's value.
7. Do not narrate a naive baseline followed by patches. State the structural problem and final insight directly.
8. Do not hide a simple method behind abstract terminology. Explain the concrete operation that realizes the insight.

## Route Unfavorable Results

- **Claim-changing**: revise the claim, axis, module, or story and disclose the remaining material fact.
- **Meaningful trade-off or boundary**: make the intended regime or frontier part of the contribution.
- **Informative but secondary**: mention briefly or move to the appendix.
- **Exploration history without scientific value**: omit.

Do not volunteer a global negative judgment. State fact → condition → trade-off or boundary → consequence for the scoped claim. Never let a local loss become the paper's summary.

## Enforce Organization Invariants

1. Make one sentence recover the paper's thesis.
2. Keep all proof modules as consequences of that thesis; split unrelated publishable findings into another paper.
3. Give every section one reader question and every paragraph one dominant rhetorical job.
4. Give every ordinary artifact one primary belief job. Allow only the identity anchor to coordinate problem, idea, and payoff.
5. Refer to an exact cell, curve region, theorem clause, or case observation; do not write “Figure 3 shows that the method works well.”
6. Use headings and captions that allow the argument to be reconstructed without continuous prose.
7. State the idea, requirement, and invariant before implementation details.
8. Keep terminology stable and define notation just before use.
9. Use the strongest scientific verb licensed by evidence.
10. Ensure the title, abstract, introduction, identity anchor, and conclusion express the same promise at different resolutions.

## Draft Evidence First

Use this order for full development:

```text
compact blueprint
→ empty core artifacts and captions or theorem statements
→ Results or formal core
→ Method, System, Theory, or Construction
→ Background and Related Work
→ draft Introduction
→ integration and evidence audit
→ rewrite Introduction from the completed body
→ Abstract
→ Title, Conclusion, and Scope
→ compression
→ reviewer red team
```

Write the Introduction twice: once to test the story and once to describe the paper the completed evidence actually delivers.

## Design Missing Research with Decision Contracts

Propose a new experiment, proof, analysis, or case only when an outcome can change a claim, close a proof obligation, or remove a concrete acceptance risk.

```text
Gap and affected claim:
Priority: claim-breaking | review-blocking | strengthening | appendix | optional
Competing outcomes:
Minimal diagnostic protocol:
Target artifact and exact readout:
Decision if positive:
Decision if negative:
Decision if null or ambiguous:
```

Reject optional decoration. Narrow a claim instead of accumulating undirected evidence when that yields a more closed paper.

## Write Natural, Non-Defensive Prose

1. Put the paragraph's main claim or job early.
2. Connect sentences by a real relation: cause, contrast, consequence, refinement, evidence, or scope.
3. Prefer concrete subjects, operations, conditions, and readouts over empty adjectives and abstract nouns.
4. Remove generic field openings, automatic three-item lists, repeated summaries, uniform cadence, and `Moreover/Furthermore/Additionally` chains.
5. Replace `novel`, `robust`, `significant`, `effective`, and `promising` with the exact supported property whenever possible.
6. Delete apologies and global self-judgments. Put scope inside the claim.
7. Preserve natural variation in sentence length and voice; use active voice when responsibility or fairness matters.
8. Rewrite any sentence that could be pasted unchanged into an unrelated paper.

## Return Only Useful Process

For a broad paper build, show this compact decision surface before long-form prose:

1. selected paper identity and winning axis;
2. one to three proof modules with closure status;
3. artifact and section spine;
4. claim-breaking or review-blocking evidence gaps;
5. strongest plausible rejection reason and repair.

Show candidate stories when selection is genuinely ambiguous. Show the full blueprint only when requested or when the project requires explicit research planning.

For a section drafting or rewriting request, return polished prose first unless the user asks for analysis. Follow with no more than five high-value notes by default. Flag unsupported or materially changed claims explicitly.

For a reviewer red team, lead with the strongest plausible rejection reason and repair underlying story, claim, evidence, artifact, order, or prose rather than adding defensive disclaimers.

Match the user's language for discussion. Default to English for manuscript prose when the user does not specify a paper language.

## Final Gate

Do not call the paper ready until all applicable checks pass:

- A target reader can repeat one thesis, one identity artifact or formal object, one decisive result, and one implication after five minutes.
- The selected story is more important, closed, and memorable than plausible alternatives.
- Every central claim maps to evidence and obeys its wording ceiling.
- The comparison class and protocol conditions are visible and fair for the claim made.
- One to three proof modules form a coherent belief-update chain.
- Every main artifact has a distinct job and exact readout.
- Section order answers the reader's largest doubt before asking for the next belief update.
- Title, abstract, introduction, identity anchor, results, and conclusion share one promise.
- Material contrary evidence, trade-offs, and boundaries are scoped without becoming a rejection summary.
- Citations, numbers, terminology, notation, captions, tables, and prose agree.
- No experiment is proposed unless an outcome can change the paper.
- Project chronology, result dumping, generic AI prose, and defensive writing are removed.
