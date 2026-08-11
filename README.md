# ML Paper Writing

[![GitHub stars](https://img.shields.io/github/stars/slark-prime/ml-paper-writing?style=social)](https://github.com/slark-prime/ml-paper-writing)
[![Download ZIP](https://img.shields.io/badge/Download-latest%20ZIP-2563eb)](https://github.com/slark-prime/ml-paper-writing/archive/refs/heads/main.zip)

A Codex skill for turning machine-learning research materials into a strategically positioned, well-organized, reviewer-ready paper.

The skill treats a paper as an academic launch rather than a project report. It identifies the most publishable supported insight, builds a coherent evidence spine around it, and helps complete the missing research needed to make the story credible.

> If this skill is useful to you, please **Star the repository before downloading**. Stars help other researchers discover the project and support continued improvement.

## What it does

- selects the strongest paper story instead of preserving project chronology;
- defines one dominant thesis and one to three proof modules;
- maps every central claim to evidence and a wording ceiling;
- organizes sections around reader questions and belief updates;
- routes results into prose, equations, figures, tables, algorithms, theorems, examples, error analyses, or case studies;
- decides what belongs in the main text, appendix, a new experiment, or nowhere;
- plans claim-changing experiments, proofs, controls, and analyses;
- drafts and revises titles, abstracts, introductions, related work, methods, theory, systems, experiments, captions, limitations, and conclusions;
- handles mixed results with strong, non-defensive positioning;
- removes generic AI prose, result dumping, and self-rejection language;
- runs reviewer, consistency, artifact, and five-minute-memory audits.

It supports empirical ML, computer vision, NLP/LLMs/agents, reinforcement learning, theory, systems, data and benchmarks, security and auditing, human studies, use-inspired research, and position papers.

## Core workflow

```text
research materials
    → Research Inventory
    → Paper Contract
    → Proof Modules + Claim–Evidence Ledger
    → Artifact and Section Spine
    → Draft
    → Reviewer and memory audits
```

The default workflow stays compact. Candidate story portfolios, complete blueprints, missing-evidence matrices, and full artifact storyboards appear only when the task needs them.

## Design philosophy

This skill encourages strong narrative selection and positive marketing:

- lead with the regime, metric, capability, or insight that best expresses the work's value;
- choose the meaningful contest in which the contribution wins;
- make favorable evidence and practical or scientific consequences explicit;
- omit debugging history, abandoned implementations, redundant results, and non-informative failures;
- treat a useful insight, corrected belief, better problem formulation, or new capability as publishable value even without universal SOTA performance.

The scientific floor is intentionally small but firm: do not fabricate evidence, imply fair rankings from unmatched protocols, infer mechanisms from non-identifying ablations, or hide facts that would make the headline claim materially false.

## Installation

Codex loads personal skills from `~/.agents/skills` and repository-scoped skills from `.agents/skills`, as described in the [official OpenAI skill documentation](https://developers.openai.com/codex/skills).

### Download the latest ZIP

1. Open the [repository](https://github.com/slark-prime/ml-paper-writing) and click **Star** in the top-right corner.
2. [Download the latest ZIP](https://github.com/slark-prime/ml-paper-writing/archive/refs/heads/main.zip).
3. Extract the archive and rename the folder from `ml-paper-writing-main` to `ml-paper-writing`.
4. Move it into `~/.agents/skills/` for personal use or `.agents/skills/` for repository-scoped use.

### Personal installation

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/slark-prime/ml-paper-writing.git ~/.agents/skills/ml-paper-writing
```

### Repository-scoped installation

Run from the target repository:

```bash
mkdir -p .agents/skills
git clone https://github.com/slark-prime/ml-paper-writing.git .agents/skills/ml-paper-writing
```

Codex normally detects skill changes automatically. Restart Codex if the skill does not appear.

## Usage

Invoke the skill explicitly with `$ml-paper-writing`, or let Codex select it when the task matches the skill description.

### Build a paper from a research workspace

```text
Use $ml-paper-writing to inspect this repository, experiment results, figures,
and research notes.

First identify the strongest paper story, winning axis, proof modules, artifact
and section spine, and any claim-breaking evidence gaps. Then help me develop
the paper in English for ICML.
```

### Rewrite an Introduction

```text
Use $ml-paper-writing to rewrite this Introduction.

Preserve supported technical claims and citations. Make the contradiction,
key insight, contribution, winning condition, and evidence preview explicit.
Remove project chronology, generic AI prose, and defensive writing. Return the
revised Introduction first.
```

### Plan decisive experiments

```text
Use $ml-paper-writing to audit the evidence for this paper.

Identify open proof modules and propose only experiments whose outcomes would
change a claim, close a reviewer objection, or alter the paper story. For each
experiment, specify positive, negative, and null decision branches.
```

### Run a reviewer red team

```text
Use the reviewer red-team mode of $ml-paper-writing.

Lead with the strongest plausible rejection reason. Check story coherence,
claim–evidence alignment, comparison fairness, missing controls, mechanism
overclaiming, artifact order, reproducibility, and promise-stack consistency.
Give concrete repairs instead of defensive disclaimers.
```

## Progressive-disclosure architecture

The runtime core is intentionally small. It loads specialized references only when the request needs them.

```text
ml-paper-writing/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── strategy.md
    ├── argument-architecture.md
    ├── compiler-core.md
    ├── artifact-router.md
    ├── artifact-storyboard.md
    ├── paper-blueprints.md
    ├── paper-blueprint-template.md
    ├── section-renderers.md
    ├── marketing-quality.md
    └── operating-modes-audits.md
```

This avoids loading a monolithic paper-writing manual for a narrow request such as revising one paragraph, while retaining the full research-to-paper compiler for complex projects.

## Main paper architectures

The skill includes dedicated blueprints for:

- focused methods and invariant fixes;
- anomaly–diagnose–repair papers;
- new paradigms, factorizations, and capabilities;
- scalable diagnosis, measurement, and evaluation;
- mechanism and learning-dynamics papers;
- counter-belief and negative-result papers;
- trade-off decoupling and simplification;
- unification and duality;
- theoretical characterization and algorithmic primitives;
- systems and infrastructure;
- datasets, benchmarks, evaluation, and human artifacts;
- security, watermarking, auditing, and verification;
- domain, workflow, and agent papers;
- position, perspective, and agenda papers.

## Influence

The skill incorporates and extends reviewer-oriented paper-writing ideas from [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills), together with claim–evidence engineering, evidence-first drafting, research-story selection, and non-defensive academic positioning.
