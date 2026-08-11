# Part VIII — Operating Modes and Output Contracts

## Contents

1. Modes A–I: blueprint, story, artifact, evidence, full paper, section, rewrite, red team, and compression
2. Story and promise-stack audits
3. Artifact-only, exact-readout, one-job, dependency, and deletion audits
4. Missing-evidence, materiality, claim-evidence, alternative-explanation, and reproducibility audits
5. Non-defensive writing and five-minute memory tests
6. Definition of done

## Mode A — Research-to-Paper Blueprint Compilation

Use when given a repository, result folder, notes, or a broad paper-planning
request.

Maintain the full blueprint internally, but return a compact decision surface by
default:

1. selected Paper Contract and winning axis;
2. one to three proof modules with closure status;
3. artifact and section spine;
4. claim-breaking or review-blocking evidence gaps;
5. strongest plausible rejection reason and next research actions.

Add a Candidate Story Portfolio only when several credible stories compete.
Expand the reader-belief graph, Claim–Evidence Ledger, artifact cards, routing
map, or section plans when they expose a decision the user needs to make. Return
the complete fillable blueprint only when explicitly requested or when the
workspace is too complex to manage compactly.

Do not draft the full paper until the user asks or the compact blueprint is
sufficiently closed.

## Mode B — Story Selection

Use when the project contains several possible contributions.

Output:

- two to five Story Cards;
- qualitative scoring and risk analysis;
- selected story and nearest alternative;
- what evidence would force a switch;
- which existing results become central, supporting, appendix, or omitted;
- one-sentence identity and working title options.

## Mode C — Artifact Routing

Use when the user asks what should become a figure, table, theorem, algorithm,
case study, and so on.

For every item return:

```text
Claim/module:
Reader task:
Chosen representation:
Why this representation:
Main / Appendix / Run / Drop:
Exact takeaway/readout:
Placement:
Removal consequence:
```

Then provide the complete artifact storyboard in order.

## Mode D — Experiment / Proof / Evidence Planning

Start from open proof modules, not a generic request for “more experiments.”

For every proposed action give:

```text
Gap priority:
Claim affected:
Competing outcomes:
Minimal diagnostic protocol:
Target artifact/readout:
Positive branch:
Negative branch:
Null/ambiguous branch:
Cost/priority:
```

Reject optional decoration.

## Mode E — Full Paper Development

Recommended order:

```text
blueprint
→ empty artifacts and captions/theorem statements
→ Results / formal core
→ Method/System/Construction
→ Background/Related Work
→ draft Introduction
→ integration and evidence audit
→ rewrite Introduction from the completed body
→ Abstract
→ Title, Conclusion, and Scope
→ compression
→ reviewer red team
```

The Introduction is written twice: once to test the story and once from the
completed evidence.

## Mode F — Section Drafting

Before writing, infer:

- Paper Contract;
- local reader question;
- claim and wording ceiling;
- prerequisite and next transition;
- exact evidence/artifact readout;
- genre-specific section moves.

Return polished prose first unless the user asks for analysis. Do not insert
unsupported numbers, citations, or claims.

## Mode G — Rewrite / De-AI / Non-Defensive Editing

Preserve supported technical content and citations. Then:

1. recover each paragraph's job;
2. move the claim or reader question to a useful position;
3. remove chronology, generic rhetoric, and self-judgment;
4. replace vague nouns/adjectives with objects, operations, conditions, and
   evidence;
5. make advantage and scope explicit;
6. restore varied natural syntax;
7. check that no qualifier material to correctness was lost.

## Mode H — Reviewer Red Team

Evaluate:

- paper identity and promise-stack consistency;
- significance and winning-axis relevance;
- soundness and claim–evidence alignment;
- originality and closest-work contrast;
- construct/measurement validity;
- comparison fairness;
- mechanism/causal overclaiming;
- theory assumptions, proof completeness, and consequence;
- reproducibility;
- material scope, risks, and limitations;
- artifact overload and section order;
- strongest plausible rejection argument.

For each issue return:

```text
Severity: critical / major / minor
Location:
Reviewer concern:
Why it matters:
Repair layer: story / claim / evidence / artifact / order / prose
Required repair:
Possible rewrite or experiment/proof:
```

## Mode I — Compression and Appendix Design

Return:

- main-text minimum closed argument;
- appendix audit interface;
- items to drop;
- dependency-safe cut order;
- claims that would weaken under each cut;
- final page and attention budget.

---

# Part IX — Final Audits

## 1. Story-Competition Audit

- Were multiple plausible stories considered?
- Was the selected story chosen for evidence and importance rather than volume?
- Is the winning axis meaningful and independently motivated?
- Would another story be more closed or memorable?
- Which evidence would kill or switch the story?

## 2. Promise-Stack Audit

Read only:

```text
title
abstract
first two introduction paragraphs
contribution/evidence preview
identity anchor and caption/theorem statement
conclusion
```

They should express the same thesis at different resolution. Flag:

- title stronger than body;
- abstract claiming a different paper;
- introduction promising experiments absent from Results;
- identity anchor emphasizing a secondary result;
- conclusion introducing a new thesis.

## 3. Artifact-Only Read

Read only section headings, captions, table headers, algorithm titles, theorem
statements, and case-study questions. The argument should remain reconstructable.

For each artifact ask:

- What claim does it update?
- What exact readout matters?
- Why is this representation necessary?
- What is the next reader doubt?

## 4. Exact-Readout Audit

Every result paragraph must identify:

- exact table cell/row/column;
- exact curve region, trend, or boundary;
- exact theorem clause/assumption;
- exact case evidence or coding result.

Flag `Figure X shows that our method works well` and similar non-readouts.

## 5. One-Job and Identity-Anchor Audit

Ordinary artifacts should have one primary job. The identity anchor may combine
problem, idea, and payoff, but must retain one hierarchy and takeaway.

Split overloaded artifacts. Remove decorative ones.

## 6. Dependency and Ordering Audit

- Does every section receive the context it requires?
- Is the largest current doubt answered before the next claim?
- Is the chosen ordering mode correct?
- Is validity shown before a novel measurement claim?
- Is the theorem stated before proof machinery?
- Is the anomaly established before the repair?
- Is the systems operating point fixed before performance?

## 7. Missing-Evidence Audit

- Which central proof modules remain open?
- Are gaps correctly prioritized?
- Does every proposed experiment have decision branches?
- Are optional “reviewer expected” experiments being run without a claim
  decision?
- Can the paper be strengthened more by narrowing a claim than by adding volume?

## 8. Materiality and Selection Audit

- Were representative subsets and cases selected by a declared rule?
- Are material full results available for audit?
- Was any claim-changing contrary evidence hidden?
- Are unmatched comparisons visibly separated?
- Does the main text aggressively select without misrepresenting?

## 9. Claim–Evidence Consistency Audit

Check every claim in:

- title;
- abstract;
- introduction;
- contribution statements;
- subsection headings;
- captions;
- discussion;
- conclusion.

Each must map to evidence and obey its wording ceiling.

## 10. Alternative-Explanation Audit

For each explanation/mechanism claim:

- What is the strongest alternative?
- What outcome differs under the two accounts?
- Which artifact tests that difference?
- Do multiple tests have independent failure modes?
- Is causal language stronger than identification?

## 11. Comparison and Reproducibility Audit

Verify data, pretraining, tuning, inference budget, hardware, precision, workload,
assumptions, population, selection, uncertainty, prompts, seeds, and copied
literature values. Ensure the route from inputs to every headline number is
documented.

## 12. Non-Defensive Writing Audit

Flag:

- global self-judgments;
- apology before claim;
- unfavorable result elevated into a paper-wide verdict;
- failure to state the winning condition;
- generic hedging where a scoped direct claim is possible;
- contribution left for the reviewer to infer from a table.

## 13. Five-Minute Memory Test

Ask a fresh simulated reader for:

1. one-sentence thesis;
2. identity artifact/formal object;
3. decisive number/theorem/finding;
4. implication.

If answers are inconsistent with the Paper Contract, redesign the promise stack
and evidence spine before line editing.

## 14. Deletion Audit

For every paragraph and artifact:

> If this disappears, which claim becomes harder to understand, believe, scope,
> reproduce, or act on?

If none, cut or move it.

---

# Definition of Done

A paper blueprint is ready for drafting when:

- one story clearly dominates plausible alternatives;
- the target reader, prior, contradiction, winning axis, and scope are explicit;
- the dominant thesis is supported by one to three coherent proof modules;
- every central claim has a complete or explicitly open evidence pack;
- missing evidence is prioritized and decision-linked;
- an identity anchor makes the idea reconstructable;
- every main-text artifact has a distinct belief job and exact readout;
- the section order follows the correct doubt/impact/theorem/construct mode;
- the main text forms a minimum closed argument;
- material contrary evidence and comparison conditions remain visible;
- title, abstract, introduction, identity anchor, and conclusion share one
  promise;
- the agent can state one sentence, one artifact, one result, and one implication
  a reader should remember;
- no result is present merely because the project produced it;
- no experiment is proposed unless an outcome can change the paper;
- prose is direct, specific, non-defensive, and no stronger than the evidence.

A paper is ready for submission only after venue rules, citation correctness,
ethics, anonymity, reproducibility, and disclosure requirements are checked
separately.

---
