---
name: ml-paper-writing
description: Write, restructure, revise, compress, and red-team machine-learning research papers using evidence-grounded claims and a reviewer-friendly narrative. Use for ML/CV/NLP/AI paper planning from repositories, notes, results, or drafts; title, abstract, introduction, related work, method, experiments, limitations, conclusion, figures, and tables; claim-evidence audits; experiment planning; removing generic AI-like or defensive prose; venue-oriented paper review; and rebuttal preparation.
---

# ML Paper Writing

## Objective

Build the paper around its strongest defensible contribution. Treat the paper as an academic release whose job is to maximize acceptance, attention, and useful intellectual impact. Select and emphasize the most compelling supported story instead of averaging over everything the project produced. Do not write a project report, experiment diary, or self-rejection memo.

Optimize three layers together:

1. Select the strongest defensible narrative.
2. Engineer an explicit claim-evidence structure.
3. Draft, compress, and review every section against that structure.

Use persuasive framing, selective emphasis, and a memorable winning axis. Treat these as legitimate scholarly communication tools. Preserve a minimal scientific floor: do not fabricate evidence or conceal information that directly invalidates the central claim. When evidence is weak, change the claim or story rather than relying on stronger adjectives.

Treat a paper as valuable even without universal SOTA performance when it gives the community a useful insight, a new idea, a better problem formulation, or a capability worth building on. Make that intellectual payload the headline.

## Scientific Floor

1. Never invent results, citations, datasets, equations, implementation details, comparisons, reviewer feedback, or causal explanations.
2. Preserve the meaning of supplied results and citations. Mark unverifiable information as missing or uncertain.
3. Distinguish observation, association, hypothesis, mechanism, and general principle. Do not silently promote a weaker finding to a stronger claim.
4. Treat an ablation as evidence that a component matters under the tested protocol, not automatic proof of the proposed mechanism.
5. Compare methods under matched data, splits, preprocessing, compute, model access, tuning budget, and metrics whenever the paper implies a fair comparison.
6. Report a result, assumption, counterexample, cost, or baseline only when omitting it would make the central claim materially false or misleading, or when the venue explicitly requires it.
7. Do not volunteer peripheral negative conclusions. State only the exact boundary needed to keep the central claim defensible.
8. Include the comparisons necessary to establish the chosen claim. If the method does not win on a dimension that is not central to its value, do not make that dimension the paper's competition.
9. Use persuasive wording to clarify and amplify supported value, never to invent support that does not exist.

## Select the Working Mode

Choose the smallest mode that satisfies the request:

- **Paper build**: turn code, notes, results, and figures into a paper architecture and draft.
- **Evidence architecture**: design experiments, figures, tables, and analyses for target claims.
- **Section draft**: draft one requested section from established claims and evidence.
- **Section revision**: restructure or rewrite supplied text while preserving supported content.
- **Compression**: meet a page or word budget without damaging the claim-evidence chain.
- **Consistency audit**: check alignment across title, abstract, introduction, results, conclusion, figures, and tables.
- **Reviewer red team**: identify plausible rejection arguments and concrete repairs.
- **Rebuttal support**: answer reviewer concerns using existing evidence; never fabricate a promised result.

Do not force the full-paper workflow onto a narrow editing request. Run the integrity rules and relevant final checks in every mode.

## Inspect Inputs Before Writing

1. Read the supplied manuscript, repository, experiment logs, tables, figures, notes, venue constraints, and bibliography as applicable.
2. Separate facts into:
   - directly supported by supplied artifacts;
   - plausible but unverified;
   - missing;
   - contradicted.
3. Preserve traceability for every number and citation. Record a source file, table, figure, log, or user statement when possible.
4. Identify inconsistent terminology, protocols, dataset names, metrics, and numerical values before polishing prose.
5. Ask only for information whose absence would materially change the paper. Otherwise state a bounded assumption and continue.

## Establish the Paper Contract

Lock the following fields before drafting a full paper or restructuring its story:

```text
Paper identity:
Target reader and venue:
Exact problem and setting:
Why the problem matters:
Structural gap in prior work:
Key insight:
Method or artifact:
Strongest defensible claim:
Contribution type:
Winning axis:
Relevant comparison class:
Scope boundary:
Claims explicitly not made:
Decisive evidence anchors:
```

Write the identity in one sentence:

```text
For [task or setting], [insight or design] enables [capability]
under [conditions], supported by [decisive evidence].
```

Treat this sentence as a contract, not a slogan. Revise it when the evidence changes. Remove paper elements that do not support, qualify, contextualize, or reproduce the contract.

## Build the Claim-Evidence Ledger

Record every central claim before polished drafting:

```text
Claim ID:
Exact claim:
Claim type: empirical | methodological | theoretical | mechanistic | efficiency | scope
Importance: central | supporting | contextual
Required evidence:
Available evidence and source:
Status: supported | partial | missing | contradicted
Placement:
Required action: keep | narrow | test | move | remove
```

Apply these rules:

1. Map every abstract and contribution claim to a result, proof, analysis, or clearly labeled scope statement.
2. Split compound claims when their evidence differs.
3. Replace vague claims such as “robust,” “efficient,” “general,” or “significant” with the tested condition and metric.
4. Narrow or remove unsupported claims. Recommend new experiments only when they are necessary for a valuable claim.
5. Propagate every claim change through the title, abstract, introduction, captions, results, conclusion, and limitations.

## Choose the Narrative Around a Meaningful Winning Axis

Identify value that the evidence can defend, including:

- a new task, capability, dataset, benchmark, or evaluation view;
- a structural insight or mechanism;
- a better result under matched conditions;
- weaker assumptions or less supervision;
- lower data, compute, memory, latency, annotation, or deployment cost;
- improved calibration, robustness, controllability, interpretability, or scalability;
- a useful trade-off or a well-supported negative result;
- a boundary or finding that changes how the field understands the problem.

Then:

1. Make the winning axis explicit, memorable, and easy to repeat rather than asking the reviewer to infer it from a table.
2. Explain why the axis matters, when the advantage appears, and what problem it solves.
3. Control the comparison range strategically: include the evidence needed for the chosen claim and avoid turning every available metric or setting into a headline contest.
4. Do not organize the paper chronologically around what the team tried. Present the shortest valid reasoning path from problem to insight to method to evidence.
5. Do not introduce a naive baseline only to narrate a sequence of patches. State the structural challenge and the final solution directly.
6. Do not conceal a simple method behind unexplained terminology. State the concrete implementation that realizes the insight.

### Handle Unfavorable Results Strategically

Classify each unfavorable result before deciding placement:

- **Core-changing**: a matched strong baseline wins on the claimed axis, a proof fails, or evidence contradicts the claimed mechanism. Change the claim, axis, or mechanism statement; disclose what remains material after that change.
- **Meaningful trade-off or boundary**: the method gains value at a cost, or works best in a defined regime. Frame the intended regime and trade-off as part of the contribution.
- **Secondary but potentially useful**: a noncentral sensitivity or out-of-scope diagnostic. Use it only when it strengthens reader understanding; otherwise move it to an appendix or omit it.
- **Non-informative exploration history**: debugging failures, dead ends, or obsolete trials that do not affect the final scientific account. Omit.

Avoid global self-criticism such as “the method has severe limitations” when the evidence supports only a local boundary. Do not promote a local loss into a paper-level conclusion. Reframe around the regime, constraint, or capability where the work creates value.

## Design the Evidence Architecture

Require every experiment to answer a paper question. Specify:

```text
Claim tested:
Research question:
Why the test is diagnostic:
Intervention or comparison:
Datasets, tasks, and models:
Controls and matched conditions:
Metrics and direction:
Runs, seeds, and uncertainty:
Positive interpretation:
Null or negative interpretation:
Target figure or table:
```

Cover only roles needed by the claims:

1. **Main utility**: compare with strong, recent, and relevant baselines under fair conditions.
2. **Design validation**: remove, replace, or disable claimed components; test interactions when components are coupled.
3. **Generalization and robustness**: evaluate across datasets, shifts, model scales, regimes, or stress conditions relevant to the claim.
4. **Cost and trade-off**: report compute, latency, memory, data, annotation, or deployment costs when they affect the value proposition.
5. **Boundary evidence**: show realistic failure cases or conditions where the conclusion stops applying.

Prefer diagnostic experiments over a large undirected experiment count. Do not call experiments “extensive” unless their coverage is itself relevant and evident.

## Design Core Figures and Tables Before Prose

1. Give each figure or table one main message and connect it to a ledger claim.
2. Use a teaser or pipeline figure when it materially clarifies the core idea or execution path.
3. Make captions self-contained: state the setting, compared objects, metric direction, essential notation, and takeaway supported by the visual.
4. Show uncertainty and number of runs when relevant.
5. Label metric direction and units; align precision; group matched settings clearly.
6. Use restrained emphasis for key values. Do not highlight so many cells that emphasis loses meaning.
7. Use minimal visual ink: avoid dense grid lines, unnecessary decoration, tiny text, and overloaded panels.
8. Keep table protocols comparable. Visually separate unmatched settings instead of implying direct ranking.
9. Check that the prose explains why the result occurs or matters, not only that one number is larger.
10. For LaTeX tables, prefer captions above tables, `booktabs` rules, no vertical lines, consistent decimal precision, and clear grouped headers.

## Use the Evidence-First Full-Paper Workflow

For a paper build, follow this order:

1. Establish the Paper Contract.
2. Build the Claim-Evidence Ledger.
3. Select the narrative spine and meaningful winning axis.
4. Plan core figures, tables, and experiments.
5. Draft Experiments and Results around research questions.
6. Draft Method from the actual pipeline and reproducibility details.
7. Draft Background and Related Work around the structural gap.
8. Write a rough Introduction to test whether the story closes.
9. Integrate terminology, notation, cross-references, and evidence.
10. Rewrite the final Introduction from scratch using the finished evidence.
11. Write Abstract, Title, Conclusion, and Limitations.
12. Compress to the target budget.
13. Run reverse outlining, consistency audit, and reviewer red team.

Write the Introduction twice: use the first pass to expose story problems and the second to represent what the completed paper actually proves.

## Apply the Section Playbooks

### Title

1. Name the task or setting and the distinctive idea, capability, or axis.
2. Prefer concrete technical nouns over promotional adjectives.
3. Avoid claims broader than the evaluation scope.
4. Make the title distinguish the paper from the nearest work.

### Abstract

Use this default sequence:

1. task and stakes;
2. exact structural gap or technical challenge;
3. key insight;
4. method that implements the insight;
5. decisive evidence with conditions and numbers when available;
6. implication and scope.

Choose a compact variant when appropriate:

- challenge → contribution;
- challenge → insight → contribution;
- multiple contributions, each paired with its technical advantage.

Keep technical names understandable on first mention. Include only claims that appear in the ledger. Do not open with generic field-wide enthusiasm or end with an unsupported claim of broad impact.

### Introduction

Build the logic backward before writing forward.

First determine:

1. the exact challenge solved;
2. the contribution and insight;
3. why the design can solve the challenge;
4. how prior work leads to the unresolved structural gap.

Then write:

1. problem and stakes;
2. relevant prior paradigm;
3. structural limitation and technical reason;
4. key insight;
5. method overview with enough concrete design to remove mystery;
6. evidence preview;
7. refutable contributions.

Adapt the opening to the setting:

- Define a niche task before applications.
- Open with applications or the unresolved challenge for a familiar task.
- Move from a general task to the exact new setting when the setting needs orientation.
- Decompose a novel task into concrete requirements when no direct prior method exists.
- Trace traditional to recent approaches only when that chain reveals the precise unresolved reason.
- Use a historical line of work when it genuinely provides conceptual backing for the new insight.

State contributions as falsifiable findings or artifacts, not activities such as “we conduct extensive experiments.” Avoid a literature tour that delays the paper's actual problem.

### Related Work

1. Group work by technical paradigm, assumption, or problem-solving route rather than publication chronology.
2. Cover the closest, strongest, and recent competitors.
3. For each group, summarize its mechanism, relevant strength, assumption, and gap tied to this paper.
4. Distinguish the current work in technical terms, not marketing language.
5. Do not hide a strong baseline or use citations as decoration.
6. Preserve citation accuracy; never infer bibliographic details from memory when sources are available.

### Method

Start from the actual pipeline:

1. Sketch the end-to-end flow.
2. Map pipeline stages to subsections.
3. List all symbols, inputs, outputs, modules, losses, and training/inference differences.
4. For every important module, cover the triad:
   - **Motivation**: the unresolved problem that requires it;
   - **Design**: representation plus input → operations → output;
   - **Technical advantage**: why it should help relative to an alternative and how that advantage is testable.
5. Draft the concrete design before adding motivation and advantages when the explanation is still vague.
6. Put definitions before use and maintain one term for one concept.
7. Include equations only when they increase precision. Define every symbol and connect the equation to the execution path.
8. Provide reproducibility-critical architecture, optimization, preprocessing, hyperparameter, and inference details or point to a clearly identified appendix.

Use an overview subsection containing the setting, core contribution, optional pipeline figure, and subsection map when it improves navigation.

### Experiments and Results

Organize around questions, not a sequence of tables:

1. State the claim or research question.
2. Explain why the protocol tests it.
3. Describe necessary setup and fairness controls.
4. Report the result with uncertainty where appropriate.
5. Interpret the pattern at the strength supported by the design.
6. State a meaningful boundary or alternative explanation when it affects the conclusion.

Include strong baselines, standard metrics, ablations for key design claims, interaction tests when needed, and realistic hard settings when they support the contract. Separate statistical significance from practical importance. Do not equate correlation with cause or component removal with mechanism identification.

### Limitations

1. State assumptions, scope boundaries, costs, and failure conditions that materially affect use or interpretation.
2. Distinguish a technical defect from an intentional task boundary or trade-off.
3. Use neutral, exact language; do not amplify a narrow issue into a verdict on the whole method.
4. Do not use the section to hide contradictory evidence or to list generic disclaimers.
5. Connect each limitation to a concrete future test only when that test follows from the evidence.

### Conclusion

1. Restate the problem, insight, and method without repeating the abstract verbatim.
2. Summarize the strongest evidence and the condition under which it holds.
3. State the scientific or practical implication at the supported scope.
4. Close with the most meaningful boundary or next direction when useful.
5. Do not introduce new claims, citations, or results.

## Write Clear Paragraphs and Natural Prose

1. Give each paragraph one primary message.
2. Put that message in the first sentence unless a deliberate short setup improves comprehension.
3. Connect each sentence to the previous one by a real relation: cause, contrast, consequence, refinement, or example.
4. Define unfamiliar nouns and terms before reusing them.
5. Prefer concrete subjects and verbs over abstract containers such as “framework,” “paradigm,” or “aspect” without content.
6. Vary sentence length and structure according to information, not for cosmetic randomness.
7. Use active voice when responsibility or comparison fairness matters; use passive voice when the actor is irrelevant.
8. Replace “novel,” “robust,” “significant,” and “effective” with the exact difference or evidence whenever possible.
9. Remove generic openings, empty significance statements, repetitive transitions, automatic three-item lists, mechanical paragraph summaries, and interchangeable closing sentences.
10. Remove defensive phrases that volunteer a global negative evaluation. Preserve precise disclosures.
11. Prefer the shortest sentence that retains the technical relation and scope.

### Reverse-Outline Every Revised Section

After drafting:

1. Write the section thesis.
2. List every paragraph's topic sentence.
3. List the evidence or explanation under each paragraph.
4. Verify topic sentence → section thesis and evidence → topic sentence.
5. Move, split, revise, or remove any paragraph that does not map cleanly.
6. Add temporary descriptive headings if the logic remains hard to see, then remove unnecessary headings in the final draft.

## Compress Without Breaking the Paper

Preserve, in order:

1. Paper Contract and core claim qualifiers;
2. decisive evidence and fair-comparison details;
3. method information needed to understand and reproduce the contribution;
4. the closest related-work distinction;
5. material limitations and uncertainty.

Cut repeated motivation, generic field background, chronological discovery history, duplicated result narration, low-information transitions, and experiments unrelated to a claim. Move secondary diagnostics and implementation detail to an appendix only when the main paper remains self-contained.

## Run the Reviewer Red Team

Audit these dimensions:

1. paper identity and narrative coherence;
2. technical soundness and claim-evidence alignment;
3. originality relative to the nearest work;
4. significance of the solved problem and winning axis;
5. comparison fairness and evaluation completeness;
6. method clarity and reproducibility;
7. generalization, costs, assumptions, and limitations;
8. consistency across title, abstract, introduction, figures, results, and conclusion;
9. prose clarity and generic or defensive writing;
10. strongest plausible rejection argument.

Return each actionable issue as:

```text
Severity: critical | major | minor
Location:
Reviewer concern:
Why it matters:
Required repair:
Possible rewrite or experiment:
```

Repair the underlying claim, evidence, protocol, structure, or wording. Do not merely insert defensive disclaimers. Separate “needs revision” from “needs new evidence.”

## Output Contracts

For a full-paper build, return before polished prose:

1. Paper Contract;
2. Claim-Evidence Ledger;
3. narrative spine and winning axis;
4. experiment, figure, and table plan;
5. missing evidence or contradictions.

For a section rewrite, return:

1. revised text first;
2. a compact outline only when it helps review;
3. no more than five critical notes unless the user requests a full audit;
4. any changed or unsupported claim explicitly flagged.

Track each paragraph's role internally (opening, challenge, insight, method, advantage, evidence, or boundary). Show role labels only when the user requests an annotated draft.

For an evidence audit, return the ledger and the highest-value repairs before prose suggestions.

For a reviewer red team, lead with the strongest plausible rejection argument, then list prioritized issues and repairs.

Match the user's language for discussion. Produce paper text in the requested language; default to English for ML manuscript prose when no preference is given.

## Final Gate

Do not call the paper or section complete until all applicable checks pass:

- The strongest contribution is explicit and scientifically meaningful.
- A reviewer can repeat the paper's main idea and community insight in one sentence.
- Every central claim has evidence or a clearly marked missing-evidence action.
- The comparison class and protocol are fair and visible.
- Material adverse evidence and scope boundaries are disclosed precisely.
- No local result is inflated into an unsupported mechanism or general principle.
- Each section advances the same paper identity.
- Each paragraph has one recoverable message and a clean evidence or explanation chain.
- Figures, tables, captions, and prose agree numerically and conceptually.
- Citations, terminology, notation, and reported values are consistent.
- Generic AI-like language, project-log narration, and global self-defeating prose are removed.
- The strongest plausible rejection argument has a concrete repair or an explicit residual risk.
