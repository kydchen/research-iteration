# Research Iteration

[中文说明](README_CN.md)

A research skill for turning an idea, a pilot result, or a stalled project into a useful next investigation. It helps an agent check prior work, choose a small study that can distinguish competing explanations, and revise its direction as evidence arrives.

The workflow supports human-computer interaction (HCI), social computing, computational social science, and technical systems research, including qualitative inquiry, design studies, surveys, experiments, digital-trace analyses, and system measurements. It adapts the research, experiment, and checklist skills from [Agent4Sci](https://github.com/maszhongming/agent4sci) into one self-contained `SKILL.md`, so Codex, Claude Code, and the Claude apps load the same instructions.

## Three stages, one skill

| Stage | Use it when | What it helps produce |
| --- | --- | --- |
| Research ideation | You are choosing a question or comparing directions | A grounded question, a specific difference from prior work, and a small first investigation |
| Investigation management | You are planning, running, or interpreting a pilot | Comparable conditions, traceable results, a resource budget, and reasons to continue or stop |
| Reflection | Results conflict, progress stalls, or you are about to increase investment | A decision to continue, revise, change direction, or conclude, with supporting evidence |

Start at the stage your task needs. A question about research ideas does not automatically start experiments. The skill preserves existing project roles, records, and data-access rules.

Each stage ends in explicit checks rather than general advice: a novelty gate against the closest prior work, a decision gate asking what results could change in conclusions, interpretations, uncertainty, evidence boundaries, or later decisions, failure triage before a direction is abandoned, and checkpoint questions for drift and anchoring. Descriptive and exploratory work can pass the decision gate even when the next activity stays the same.

## What changes from Agent4Sci

The Agent4Sci paper reports three recurring limitations of frontier agents: novelty miscalibration, resource under-utilization, and rapid collapse into local engineering sweeps. Its original skills counter them on scientific machine-learning benchmarks with prepared baselines and substantial GPU resources. This adaptation keeps the counter-pressure and changes the operating assumptions:

- Choose investigations for the knowledge they could add and the explanations they could distinguish. High risk or implementation complexity does not make an idea valuable by itself.
- Keep the forcing questions. A new setting, population, platform, or model applied to an answered question is labeled an application or replication, and at least one candidate should change the framing.
- Verify a baseline when necessary and reuse reliable results when their conditions match. Baseline reproduction is not prohibited.
- Work within the project's resource budget. Idle GPUs are not a reason to launch more experiments, but existing data and parallel pilots should be used before new collection.
- Apply the evidence standards appropriate to the method. Interviews, fieldwork, and design inquiry are not recast as metric optimization or causal experiments. Automated and LLM-based classification or coding uses suitable held-out human annotations, while other measurements use checks or reference standards appropriate to the measure. Both require attention to validity and systematic errors across relevant groups.
- Reflect at meaningful result and decision points. The skill installs no hooks, timers, background workers, or required multi-agent workflow.

The source snapshot, a mechanism-by-mechanism mapping, and the revision history are recorded in [PROVENANCE.md](PROVENANCE.md).

## Install

The skill consists of one Markdown instruction file and optional display metadata. It has no package dependencies or bundled executable scripts. Research tasks may still require the tools and data appropriate to the project.

Choose an installation location for your agent. The following commands are for a new installation and will fail if the destination already exists.

### Codex

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/kydchen/research-iteration.git ~/.agents/skills/research-iteration
```

For a project-scoped installation, clone into `.agents/skills/research-iteration` inside that project instead. These locations follow the [official Codex skill documentation](https://learn.chatgpt.com/docs/build-skills#where-to-save-skills). If an existing installation is already discovered elsewhere, update that copy rather than adding a duplicate. Restart Codex if the new skill does not appear.

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/kydchen/research-iteration.git ~/.claude/skills/research-iteration
```

For a project-scoped installation, use `.claude/skills/research-iteration`. See the [official Claude Code skill documentation](https://code.claude.com/docs/en/skills). The `agents/openai.yaml` file supplies Codex display metadata and is not required by Claude Code.

### Claude apps

Everything the skill needs is in `SKILL.md`, so it can also be added as a custom skill in the Claude apps without the other files.

## Use

In Codex, invoke `$research-iteration`. In Claude Code, invoke `/research-iteration`. The agent may also select it when a request matches its description.

### Develop a research question

```text
$research-iteration Use this proposal and the attached papers to compare two research directions. Identify the closest prior work and recommend a small first study that could change our judgment. Respond in English.
```

### Plan a pilot

```text
$research-iteration We have interview notes about how people check AI-generated work. Help plan a pilot analysis that preserves the participants' context and distinguishes the explanations already in our proposal. Do not collect new data.
```

### Reconsider a stalled direction

```text
$research-iteration Review these experiment records. What have we learned, which explanations remain plausible, and should we continue, revise the design, or stop within the remaining budget?
```

Replace `$research-iteration` with `/research-iteration` for Claude Code. Provide the materials you actually have; missing evidence should remain visible rather than being filled in.

The skill instructions and display metadata are written in English. Responses and deliverables follow the user's requested language, or the language of the user's request when no output language is specified. The READMEs are available in English and Chinese. Both describe the same skill implementation.

## Files and related workflows

- [SKILL.md](SKILL.md): the complete skill, covering stage selection, ideation, investigation management, and checkpoints.
- [PROVENANCE.md](PROVENANCE.md): source snapshot, adaptation choices, revision history, and evidence limits.
- [agents/openai.yaml](agents/openai.yaml): Codex display metadata.
- [LICENSE](LICENSE): Apache License 2.0.

An optional, separately installed `research-argument-map` skill can map the relationships between a question, claims, and evidence. Research Iteration focuses on choosing the next investigation. Neither workflow requires the other or an automatic writing or editing pass.

## Evidence and limitations

The [Agent4Sci paper](https://arxiv.org/html/2610.28763v1) evaluates its original three-skill combination on scientific machine-learning benchmarks. According to its abstract, the skills raised mean relative improvement over the published best from 10.4% to 20.1% for Claude Opus and from 4.4% to 8.1% for Codex. Those results do not establish the independent value of each skill or the effectiveness of this adaptation in HCI, social computing, computational social science, or qualitative research.

This version has passed frontmatter and link checks. Its effect on real research outcomes has not been evaluated in a controlled comparison, and it has not been tested end to end in Claude Code. Research novelty, methodological adequacy, and the strength of a conclusion still require source-based judgment.

## Attribution and license

Adapted from [Agent4Sci](https://github.com/maszhongming/agent4sci), using commit [`74b0e8c`](https://github.com/maszhongming/agent4sci/tree/74b0e8c4dc55610072bed4326b6bfac24dc77377) as the source snapshot. The instructions were reorganized and rewritten on 2026-10-25. This is an independent adaptation and is not the authors' original release.

Upstream copyright: Copyright 2026 Ming Zhong, Stacy Li, and the Agent4Sci authors.

Licensed under [Apache License 2.0](LICENSE).
