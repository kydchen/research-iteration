# Origins and adaptation notes

This version reorganizes and rewrites three Agent4Sci skills for HCI, social computing, and technical systems research. It was adapted on 2026-10-25 and translated into English on the same date, retaining the instruction to follow the user's requested output language. It is an independent adaptation, not the authors' original release, and has not been evaluated under the Agent4Sci protocol.

Upstream copyright: Copyright 2026 Ming Zhong, Stacy Li, and the Agent4Sci authors. The upstream project uses Apache License 2.0. The complete terms are included in this skill's [LICENSE](../LICENSE).

## Verifiable upstream snapshot

- Paper: [Automating ML for Science: Can Frontier Agents Climb Scientific Hills in the Wild?](https://arxiv.org/html/2610.28763v1). Relevant material appears in Section 4, Appendix A.5, and Appendix D.
- Repository: [maszhongming/agent4sci](https://github.com/maszhongming/agent4sci).
- Repository commit inspected for this adaptation: `74b0e8c4dc55610072bed4326b6bfac24dc77377`. This identifies the retrieved snapshot, not necessarily the version used in the paper's experiments.
- [research/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/research/SKILL.md)
- [experiment/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/experiment/SKILL.md)
- [checklist/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/checklist/SKILL.md)
- [experiment/best_practices.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/experiment/best_practices.md)

## How the three stages were adapted

| Stage | Purpose retained | Changes in this adaptation |
| --- | --- | --- |
| Research | Use literature and domain knowledge to develop distinct ideas and assess novelty | Calibrate contributions against the closest prior work and concrete evidence, include qualitative, design, and empirical research, and allow implementation inspection to inform the question |
| Experiment | Use small trials, record progress, diagnose failures, and manage resources | Verify baselines as needed, prioritize investigations that can change a decision, apply budgets and stopping conditions, and reuse project logs and assigned responsibilities |
| Checklist | Detect narrowing directions and take corrective action | Check at result and decision points, allow continuing, revising, changing direction, or concluding, and optionally add time-based checks during long tasks |

The original skills assume prepared scientific machine-learning benchmarks and substantial GPU resources. This adaptation removes requirements to prioritize high-risk work, saturate every GPU, prohibit necessary baseline reproduction, use multiple agents by default, produce four fixed literature reports, or keep a session active. It includes none of the upstream hooks, polling scripts, or model configuration.

## Interpreting the evidence for usefulness

The paper's main comparison evaluates the three skills together. It does not establish each stage's independent contribution. Appendix A.5 acknowledges limitations arising from adaptation to the existing tasks and Claude's behavior. The value of this version for HCI, social computing, qualitative research, and current models still needs to be assessed through actual use.

Useful observations include whether the skill reduces unsupported novelty claims, distinguishes key explanations with smaller investigations, changes subsequent decisions in response to negative results, and makes better use of time and resources. Completing more steps or producing more documents is not itself evidence of effectiveness.
