---
name: research-iteration
description: "Turn research ideas, pilot results, or stalled projects into a literature-grounded next investigation that distinguishes explanations within a realistic budget. Use for research questions, experiment or fieldwork pilot planning, and decisions during iterative research in HCI, social computing, and technical systems. Not for routine prose editing, paper summaries, or ordinary code fixes."
license: Apache-2.0
---

# Research ideation, investigation, and reflection

Help the next step produce evidence that can change a research judgment. Respect the project's methodology rather than treating every study as model-metric optimization. Perform only the stage the user requests, building on sufficient existing findings and materials.

Use the language the user requests for responses and deliverables. If no output language is specified, follow the language of the user's request. English instructions do not make English the default output language.

## Enter at the current stage

- **Ideation or topic selection**: Use the guidance below to develop grounded candidate questions and a small first investigation.
- **Conducting or interpreting an investigation**: Read [Investigation and experiment management](references/experiment.md). Reuse the existing plan and records rather than restarting topic selection.
- **Stalled progress, conflicting evidence, or a planned increase in investment**: Read [Reflection at decision points](references/reflection.md). Make a specific decision to continue, revise, change direction, or conclude.

Load only the references relevant to the current stage. An ordinary discussion of ideas does not automatically launch experiments, create long-running tasks, or introduce a new set of project documents. When roles or execution responsibilities are already assigned, deliver the plan, review, or work order appropriate to the current role.

## Ground the question in research objects and evidence

Read the current proposal, key materials, and existing results. Identify the research population or system, unit of analysis, core concepts, established facts, and unresolved questions. Use existing project records rather than asking the user to supply known information again. If the research question is not yet clear, offer candidate formulations and label them as suggestions.

Start from a phenomenon, tension, or consequence worth explaining. State whose understanding or judgment the completed research could change, and about what. In HCI and social computing, retain participants, organizational arrangements, power, and contexts of use. In technical systems research, explain how a mechanism produces consequences observable by users or in the system.

Distinguish whether the task aims to describe a phenomenon, explain a mechanism, compare methods, develop design knowledge, or investigate a technical claim. Contributions can come from new empirical material, boundary conditions, theoretical explanations, or design insights. Complexity and risk do not determine research value.

## Calibrate the difference from prior work

Search directly relevant domain research and methods or neighboring fields that could meaningfully inform the question. Based on papers, official implementations, and project materials actually inspected, explain what the closest work answers, what remains unresolved, and whether a candidate is an application of a known method or an engineering improvement.

Keep verifiable citations and source locations. Separate verified differences, the analyst's inferences, and matters still to check. Not finding prior work does not establish its absence. If the full text, implementation, or a key appendix was unavailable, state which judgments remain unsupported. Do not guarantee novelty beyond the scope of the search.

Alternate literature search and implementation inspection when useful, letting actual data and system constraints revise the ideas. Do not require a fixed number of literature reviews before proceeding or enable multiple agents by default.

## Choose a next step that distinguishes explanations

When a comparison is useful, propose a small set of substantively different directions. For each promising direction, explain:

- **Question and basis**: Who or what is being studied, which observations or literature motivate the question, and what knowledge it could add.
- **Explanations to distinguish**: Possible mechanisms, alternative explanations, or an empirical question that needs clarification. Do not impose causal hypotheses on qualitative or design research.
- **Smallest useful investigation**: Which materials, comparison, prototype, or analysis could first establish whether the direction merits further work. State which outcomes would support continuing and which would require revising or abandoning the current explanation.
- **Feasibility**: What existing materials, implementations, and access conditions allow, the time or resources required, and the conditions for stopping.

Consider both feasible approaches and well-grounded exploratory approaches. Prioritize their potential knowledge gain, ability to distinguish explanations, and cost. An exploratory approach should specify what changes in the problem representation, explanatory mechanism, way of observing, or design premise. When the user seeks innovation, avoid proposing only parameter variations within one framing. Use small pilots to investigate substantively different ideas. When the task is reproduction, description, or reliability improvement, complete that goal directly.

Recommend one next step and explain the choice. Verify a baseline when a reliable one is missing, and reuse existing results when they are verifiable and applicable. Keep long-term effects, causal relationships, and population-level claims unresolved when a small pilot cannot establish them.

## Connect to existing work

Use the project's current research notes, experiment records, and directories. When saving work is needed, record the decision, evidence locations, and next step without automatically creating several documents that say the same thing.

If the user wants to inspect specific relationships among research questions, claims, and evidence, an available `research-argument-map` skill can help. This skill focuses on choosing the next investigation. It does not require a diagram or automatically invoke writing and editing skills.

Lead the deliverable with a judgment. Make its basis, remaining uncertainty, and next step verifiable. Use a table when there are actual alternatives to compare, and summarize the decision without exposing every internal self-assessment question.

## Origins and adaptation

Adapted from Agent4Sci's research, experiment, and checklist skills on 2026-10-25 for local research workflows. Preserve attribution in [Origins and adaptation notes](references/provenance.md) and [LICENSE](LICENSE). Read the notes only when checking sources, adaptation choices, or applicability.
