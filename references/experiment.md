# Investigation and experiment management

Use this reference to plan, conduct, or interpret one research investigation. Experiments are one form of investigation. Interview pilots, material coding, prototype comparisons, and system measurements should follow their own methodological standards.

## Establish comparison conditions before starting

Identify the question for this round, the existing baseline or comparison material, the main basis for judgment, the budget, and the stopping conditions. Read existing records first and clarify missing information only when it affects execution. Without a request to execute, deliver a plan rather than launching the full study.

- **Technical and quantitative research**: Check data provenance, units of analysis, splits, metric definitions, and code and configuration versions to establish comparability. Reuse verified results when conditions match, and reproduce what is necessary when a credible baseline is missing. Do not copy a fixed seed or fold count without justification, or change them opportunistically to obtain better results.
- **Qualitative and design research**: Establish how materials address the question, the boundaries of sampling and context, how concepts are recognized, and how the analysis will be documented. Retain researcher positionality, counterexamples, and competing interpretations. Do not turn interviews into unsupported causal tests or population-representative statistics.
- **Simulation and prototype research**: State assumptions and simplifications. Distinguish simulation results, prototype feasibility, and effects in actual use.

## Check feasibility before increasing investment

Choose the smallest pilot that can examine the core premise. For code changes, begin with a short but representative run and check inputs, outputs, runtime, and failure signals. For material analysis, check whether the examples, coding, or interpretations can distinguish the phenomena of interest. If the pilot changes the design, record the change and its rationale.

Use existing project logs, directories, and task-management practices. Isolate experimental outputs to avoid overwriting raw materials, baseline results, or other ongoing work. Run independent tasks concurrently only within authorized time, spending, and computing limits. Idle resources alone do not justify additional experiments.

For long jobs, retain a job identifier, log or progress location, and expected completion time. Inspect new results, errors, or material delays, and optimize measured bottlenecks when necessary. Account for CPU, memory, storage, and API quotas as well as GPU use. Do not assume the machine has an NVIDIA GPU.

## Record how an investigation changes the judgment

Reuse the existing research record. If no format exists and the task needs multiple rounds of tracking, one compact table is sufficient:

| ID and status | Question or hypothesis | Materials and comparison conditions | Method, version, and artifact locations | Budget and actual cost | Results and limitations | Decision and next step |
| --- | --- | --- | --- | --- | --- | --- |

Distinguish planned, running, completed, failed, and not-executed work. Record deliberately omitted conditions. Planned comparisons, failed runs, and negative results must not disappear from the record merely because they did not improve a metric.

For quantitative claims, report the size of the difference and appropriate uncertainty. Do not describe a single run or a tiny numerical improvement as a stable effect. Choose comparisons across seeds, folds, periods, or groups according to the question and keep conditions comparable. Do not add repetitions solely because the upstream skill prescribes them.

When work fails, distinguish runtime or data problems, study-design problems, and evidence that does not support the current hypothesis. Retry only when the proposed correction has a clear purpose and remains within budget. Reaching the budget, finding that another investigation is unlikely to change the decision, or lacking necessary materials can justify stopping. There is no need to prove that every variant would fail.

## Preserve the value of validation

Keep data boundaries and evaluation rules fixed. Held-out material reserved for final evaluation must not guide direction selection, tuning, or result selection. Follow the project's established permissions and process for final evaluation. This skill does not authorize opening sealed samples. If held-out results have already informed a change, disclose that they have entered exploration and can no longer serve as independent validation.

Follow existing preregistration, research ethics, informed-consent, and data-access requirements. Exploratory analysis may change a plan, but record the change rather than presenting it retrospectively as a prior decision. Qualitative research should maintain credibility through appropriate counterexample analysis, traceable materials, and reflexivity rather than mechanically adopting training and test splits.

At the end of a round, state the evidence obtained, the strongest conclusion it supports, and the reasons to continue, revise, change direction, or conclude. Before changing direction or increasing investment, read [Reflection at decision points](reflection.md).
