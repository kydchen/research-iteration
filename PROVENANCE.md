# Provenance and adaptation notes

Research Iteration reorganizes and rewrites three Agent4Sci skills for HCI, social computing, computational social science, and technical systems research. It is an independent adaptation, not the authors' original release, and it has not been evaluated under the Agent4Sci protocol.

Upstream copyright: Copyright 2026 Ming Zhong, Stacy Li, and the Agent4Sci authors. The upstream project uses Apache License 2.0. The complete terms are included in this repository's [LICENSE](LICENSE).

## Verifiable upstream snapshot

- Paper: [Automating ML for Science: Can Frontier Agents Climb Scientific Hills in the Wild?](https://arxiv.org/html/2610.28763v1) by Ming Zhong, Stacy Li, Nicholas Carlini, and Matthew Jagielski. Relevant material appears in Section 4, Appendix A.5, and Appendix D.
- Repository: [maszhongming/agent4sci](https://github.com/maszhongming/agent4sci).
- Repository commit inspected for this adaptation: `74b0e8c4dc55610072bed4326b6bfac24dc77377` (2026-10-21), still the latest commit on 2026-10-25. It identifies the retrieved snapshot, not necessarily the version used in the paper's experiments.
- [research/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/research/SKILL.md)
- [experiment/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/experiment/SKILL.md)
- [checklist/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/checklist/SKILL.md)
- [experiment/best_practices.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/experiment/best_practices.md)

## What the upstream skills were built to counter

The paper's abstract names three recurring limitations of frontier agents on its benchmarks: novelty miscalibration, resource under-utilization, and rapid collapse into local engineering sweeps. The upstream skills push against them with literature-grounded ideation, a two-tier experiment taxonomy with calibration questions and a demote-and-replace rule, aggressive hardware use, failure triage, and an hourly self-assessment. According to the upstream README, the hourly checklist is enforced through a tool-call hook on Claude and is an on-demand skill on Codex.

## How the mechanisms were adapted

The original skills assume prepared scientific machine-learning benchmarks and substantial GPU resources. This adaptation keeps the forcing checks and replaces the benchmark-specific operating rules.

| Upstream mechanism | Kept as | Changed |
| --- | --- | --- |
| Four literature reviews by subagents with fixed report formats | Grounding in the closest prior work, including work that contradicts the idea, with a stated search scope | No fixed number of reviews or subagents; only retrieved or user-supplied sources count as support |
| Tier 1 and Tier 2 experiments, calibration questions, demote and replace | Novelty gate, at least one candidate that changes the framing, and a cheap pilot of that candidate alongside the primary step | Risk is not a value in itself; a new setting must name the difference it is expected to make, and applications and replications can be the right next step when labeled honestly |
| Hypothesis registration before running | Outcome-to-action map and decision gate, also applied when work starts at the investigation stage | Works for qualitative and design research without forcing causal hypotheses |
| Saturate every GPU, run Tier 1 first, never re-run the baseline | Use existing data first and run independent pilots in parallel within limits | Budgets and stopping rules apply; baselines are verified when no reliable one exists |
| Fix, pivot, or abandon a failed experiment | Classify a failure before abandoning a direction, with inconclusive pilots kept separate from evidence against an idea | Abandoning no longer requires proving that no variant could work |
| Hourly checklist enforced by hooks | Checkpoint questions on drift, anchoring, evidence, and cost | Triggered by results, stalls, new investment, or about three variants within one framing; no hooks, timers, or session keep-alive |

The adaptation adds evidence standards for qualitative and design research, surveys and experiments with people, simulations and prototypes, and computational social science, including the validity of automated and LLM-based measures against held-out human labels, causal identification, and sampling in digital-trace data. It also states which actions need the user's explicit request, such as contacting people, sending participant data to outside services, or spending money. It includes none of the upstream hooks, polling scripts, subagent definitions, or model configuration.

## Revision history

- 2026-10-25: First adaptation, organized as SKILL.md with three reference files, then translated into English while keeping the instruction to follow the user's requested output language.
- 2026-10-25: Consolidated into one self-contained SKILL.md so that Codex, Claude Code, and the Claude apps load the same instructions. Restated the upstream forcing checks as explicit gates, separated inconclusive pilots from evidence against an idea, added computational social science standards and explicit authorization boundaries, and removed instructions that only made sense when read against the upstream text.

## Interpreting the evidence for usefulness

According to the abstract, adding the three skills raised mean relative improvement over the published best from 10.4% to 20.1% for Claude Opus and from 4.4% to 8.1% for Codex. The comparison evaluates the three skills together on scientific machine-learning benchmarks, so it does not establish each stage's independent contribution. Appendix A.5 acknowledges limitations arising from adaptation to the existing tasks and Claude's behavior. The value of this version for HCI, social computing, computational social science, qualitative research, and current models still needs to be assessed through actual use.

Useful observations include whether the skill reduces unsupported novelty claims, distinguishes key explanations with smaller investigations, changes subsequent decisions in response to negative results, and makes better use of existing materials, time, and resources. Completing more steps or producing more documents is not itself evidence of effectiveness.
