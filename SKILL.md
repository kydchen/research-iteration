---
name: research-iteration
description: "Decide the next research step. Use when asked whether an idea is new or worth pursuing; how to design, pilot, or interpret an interview, survey, experiment, digital-trace, LLM-measurement, or system study; or whether to continue, revise, pivot, or stop after results. For HCI, social computing, computational social science, and technical systems research. Not for standalone literature reviews, related-work writing, diagramming an existing argument, prose editing, paper summaries, or routine code fixes."
license: Apache-2.0
---

# Research iteration

Choose the next piece of research work that could change a judgment, run it at the smallest scale that can show something, and decide what the result means. Respect each method's evidence standards: interviews, design studies, surveys, experiments, digital-trace analyses, simulations, and benchmarks do not all reduce to metric optimization. Do only the stage the user needs.

Respond in the language the user asks for; otherwise use the language of the user's request. These English instructions do not make English the default.

## Pick the stage

- **Ideation**: choosing or sharpening a question, comparing directions, or checking novelty. Go to Stage 1.
- **Investigation**: planning, running, or interpreting a pilot or study. Go to Stage 2, building on the existing plan and records instead of restarting ideation.
- **Decision point**: results have arrived, evidence conflicts, progress has stalled, or more investment is about to be committed. Go to Stage 3.

Discussing ideas does not authorize action. Quick read-only checks of data and files already in the workspace are fine at any stage. Contacting people, collecting new data, spending money, starting long-running jobs, sending participant data to outside services such as model APIs, or creating a new set of project documents needs the user's explicit request, including when the purpose is to fix a failure. Never work around access controls or platform terms; report the block instead. When roles are already assigned, for example one agent plans and another executes, deliver what the current role owes: a plan, a review, or a work order.

## Failure modes to counter

Agents helping with research drift in predictable ways. The checks in each stage exist to catch these:

1. **Novelty miscalibration**: presenting a known method in a new setting, population, platform, or model as a contribution, or claiming novelty after a shallow search.
2. **Underusing what exists**: proposing new data collection before checking existing data, logs, prior pilots, or public datasets, or running independent cheap checks one at a time.
3. **Collapse into local variation**: more runs, prompts, survey items, subgroup cuts, or coding passes within one framing instead of a test of a rival explanation.
4. **Investigations that cannot change a judgment**: work whose plausible outcomes would not change a substantive conclusion, interpretation, uncertainty, evidence boundary, or later decision.
5. **Premature abandonment and anchoring**: dropping a direction after an execution failure or an inconclusive pilot, or holding on to the first thing that worked.
6. **Overclaiming**: treating one run as a stable effect, interview counts as prevalence, correlation as cause, or a pilot as a population finding.
7. **Deference**: adopting the user's preferred framing without stating the strongest reason it could fail or may already exist.

## Stage 1: Ground the question and choose the first investigation

**Read before asking.** Read the available proposal, materials, and results. Identify the phenomenon, the population or system, the unit of analysis, the core constructs, what is established, and what is open. Do not ask for information the records already contain. If the question is still vague, offer candidate formulations and label them as suggestions.

**State the stakes.** Name whose understanding or decision the finished work could change, and about what. Classify the aim: describe a phenomenon, explain a mechanism, measure a construct, compare methods, produce design knowledge, or test a technical claim. In HCI and social research, keep participants, organizations, power, and context of use in view. In technical work, connect the mechanism to consequences that users or the system would show.

**Find the closest prior work.** Search the domain literature, the names that neighboring fields use for the same phenomenon, recent preprints, and relevant methods, and inspect implementations or datasets when they bear on feasibility. Treat a source as support only if it was retrieved in this session or supplied by the user, and give its location (section, page, table, or URL). Anything recalled from memory is a lead to verify, not a citation. Look for work that contradicts or complicates the idea, not only work that supports it. Prefer peer-reviewed and primary sources as support and mark preprints and grey literature as such, but count any prior work against novelty, whatever its venue. Keep verified differences, your inferences, and open checks apart. State the search scope, because not finding prior work does not show that none exists. If search is unavailable, say so, offer remembered work only as unverified leads, and mark the novelty verdict provisional. If a full text, appendix, or implementation was unavailable, say which judgments that leaves unsupported.

**Generate real alternatives.** When comparing directions helps, propose two to four that differ in substance. At least one should change the framing, meaning the problem representation, the explanatory mechanism, the way of observing, or the design premise, rather than vary parameters, populations, platforms, or models inside one framing. Let actual data and system constraints revise the ideas. For reproduction, description, or reliability tasks, do that task directly instead.

For each direction, specify:

- **Question and basis**: who or what is studied, which observations or sources motivate it, and what it would add.
- **Explanations to distinguish**: rival mechanisms or interpretations, or the empirical unknown to clarify. Do not force causal hypotheses onto qualitative or design research.
- **Smallest useful investigation**: the materials, comparison, prototype, or analysis that can first show whether the direction deserves more work. Check what existing data, logs, prior pilots, or public datasets can already answer before proposing new collection.
- **Outcome-to-judgment map**: what plausible results would change in the conclusions, interpretations, key uncertainties, evidence boundaries, or later decisions. Map results to continue, revise, or drop when that decision is in scope.
- **Feasibility**: data access and platform terms, ethics review and consent, recruitment, compute and API costs, time, and the condition for stopping.

**Pass two gates before recommending.**

- **Novelty gate**: State in one sentence how the direction differs from the closest prior work. For a new setting, population, platform, tool, or model, name the difference you expect it to make and how the study would detect it. If you cannot, call the direction an application or replication. It can still be the right next step, but do not present it as the novel contribution, and add a candidate that changes the framing. Ask whether an expert who knows the closest work would learn something, or would see standard practice in ambitious language.
- **Decision gate**: Name what plausible outcomes could change in a substantive conclusion, interpretation, key uncertainty, evidence boundary, or later decision. If none could change any of these, redesign or drop the investigation. Descriptive, exploratory, and formative work can add knowledge even when the next activity stays the same. Do not require a continue, revise, or drop choice when the task is to characterize or understand a phenomenon.

**Recommend one primary next step**, plus a cheap pilot of the framing-changing candidate when it can run alongside. Say why the primary step beats the alternatives on knowledge gained, power to distinguish explanations, and cost. State the strongest objection to the favored direction before its merits, including when the user favors it. Verify a baseline when no reliable one exists, and reuse results when they are verifiable and their conditions match. Leave long-term, causal, and population-level questions open when a pilot cannot settle them.

## Stage 2: Plan, run, or interpret an investigation

**Fix the comparison first.** If the records show no prior-work check or outcome-to-judgment map for this investigation, run both Stage 1 gates briefly before planning, without restarting ideation. Record the question for this round, the baseline or comparison, what evidence will count, the budget, and the stopping rule. Read existing records first and ask only about gaps that would change execution. Without a request to execute, deliver a plan.

**Apply the method's own standards.**

- **Computational and quantitative work**, including models, digital-trace data, and observational analyses: establish data provenance, sampling and who is missing, the unit of analysis, and how each measure supports its intended interpretation. For automated or LLM-based classification, coding, or other judgments assessed through human annotation, validate against suitable human annotations held out from prompt, model, and codebook iteration. Document annotation quality and disagreement, and check whether errors differ across the groups being compared. For other automated measures, use checks or reference standards appropriate to the measure, including definitions, instrumentation or log accuracy, coverage, missingness, and systematic error across relevant groups. An accurately computed count, duration, or network statistic does not by itself validate a social construct. State the identification strategy behind causal claims, train, validation, and test boundaries for predictive work, metric definitions, and code, data, and configuration versions. Choose repetitions across seeds, folds, periods, or groups to fit the question, and keep conditions comparable.
- **Surveys and experiments with people**: power or precision targets based on prior work or a smallest effect of interest rather than on pilot estimates, preregistration where the project uses it, manipulation and attention checks, and consent.
- **Qualitative and design work**: how the materials bear on the question; sampling and context boundaries; how concepts are recognized, with each theme traceable to excerpts and their sources; researcher positionality; negative cases; and competing interpretations. Treat coding done by an agent as a draft for the researcher to check. Do not turn interviews into causal tests or counts into population estimates.
- **Simulations and prototypes**: state assumptions and simplifications, and keep simulated results, prototype feasibility, and effects in actual use distinct.

**Pilot first.** Run the smallest version that tests the core premise. For code, use a short but representative run and compare expected with observed inputs, outputs, runtime, and failure signals. For materials, check whether the examples or codes can distinguish the phenomena of interest. Pilots with people test feasibility, such as comprehension, timing, manipulation checks, and floor or ceiling effects, not the size of the effect. Record any design change the pilot causes, and why.

**Execute cleanly.** Use the project's logs, directories, and task practices. Isolate each investigation's code changes and outputs so that raw data, baselines, and other ongoing work are never overwritten. Review code or analyses produced by subagents or collaborators before trusting their results. Run independent pilots in parallel when time, spending, and compute limits allow. For long jobs, keep the job identifier, log location, and expected finish time; check CPU, memory, storage, API quotas, and accelerators, and fix bottlenecks you have measured.

**Triage failures before abandoning anything.** Classify each failure:

1. **Execution or data problem** (crash, bug, missing data, quota): fix it if the budget allows.
2. **Design problem** (the study as built cannot answer the question): redesign, then rerun at pilot scale.
3. **Inconclusive result** (too small or noisy to distinguish the explanations): decide whether a larger or sharper test is worth its cost.
4. **Evidence against the explanation**: record it as a result, then revise or drop the direction.

The first three say little about the idea itself, so do not drop a direction because of them unless a stopping rule applies; after the fourth, do not keep patching. Stop when the budget is spent, when further work is unlikely to add knowledge or change a decision, or when necessary materials are missing.

**Protect the evidence.** Keep data boundaries and evaluation rules fixed. Material reserved for confirmation or final evaluation must not guide exploration, tuning, or result selection, and this skill does not authorize opening it. If it has already informed a change, disclose that it can no longer serve as independent validation. Fix analysis choices before seeing outcomes, or report the analyses as exploratory. Follow existing preregistration, ethics, consent, and data-access requirements, and record plan changes as changes rather than presenting them later as prior decisions.

**Report in proportion.** For quantitative claims, give effect sizes with appropriate uncertainty; one run or a tiny gain is not a stable effect. Keep failed runs, negative results, and planned comparisons that were skipped in the record.

**Keep one record.** Reuse the project's existing record. If none exists and the work will run for several rounds, one table is enough:

| ID and status | Question or hypothesis | Comparison and conditions | Method, version, and locations | Budget and actual cost | Result and limits | Decision and next step |
| --- | --- | --- | --- | --- | --- | --- |

Status is one of planned, running, done, failed, or not run.

At the end of a round, state the evidence obtained, the strongest conclusion it supports, and what it does not support. Before scaling up or changing direction, go to Stage 3.

## Stage 3: Decide at checkpoints

Check after important results, when progress stalls, before committing more data collection, participants, or compute, and after about three consecutive variants within one framing, such as prompts, survey items, model specifications, or subgroup cuts. During an authorized task that lasts several hours, also check at the next natural break after about an hour. This is an in-task habit, not a timer: it does not wake a session or schedule background work, so use the environment's scheduling features only when the user asks for recurring checks. If the goal is already met, conclude instead of working through the questions.

Work through these questions and report only the answers that change the decision:

1. **Question**: Is the work still answering the research question, or has it turned into more runs, better-looking metrics, a more complex implementation, or more documents? For reproduction or reliability work, judge progress against that goal.
2. **Evidence**: Which observation changed the judgment this round? Which results would a rival account explain equally well, such as an artifact, a confound, sampling, demand effects, or the researcher's own reading? Do the claims exceed what the design supports?
3. **Anchoring**: Was any direction dropped after an execution problem, a design problem, or an inconclusive result rather than evidence against it? Is the frontrunner still the best candidate, or only the first one that worked?
4. **Drift**: Is method transfer, parameter tuning, or a new setting now presented as the contribution? Which substantively different explanation is worth testing next? Do not add risk only to produce a surprising result.
5. **Cost**: Which work is still worth doing, and which failures need fixing? Does the remaining budget cover validation and write-up? Is there already enough evidence to decide?

Then choose one:

- **Continue**: the evidence supports the direction, and the next step can still reduce a key uncertainty.
- **Revise**: fix a specific implementation, sampling, measurement, or interpretation problem, then run a bounded check.
- **Change direction**: new evidence weakens the current explanation, or another approach answers the original question better. Confirm with the user first if the change goes beyond their goal.
- **Conclude**: the goal is met, the budget is spent, or further work is unlikely to change the judgment. Deliver the results and the open issues.

Write the decision, its basis, and the next step into the existing record. Carry out the corrections within the authorized scope, or hand them to whoever owns them. Answering the questions is not the same as doing the corrective work.

## Deliver

Lead with the judgment: the recommended next step or decision, and why. Then make its basis checkable: sources with locations, a comparison table when there are real alternatives, the outcome-to-judgment map, and what remains uncertain. For ideation, always include the one-sentence difference from the closest prior work. Report other checks only where they changed the recommendation, and do not reproduce the checklists.

Use the project's existing notes and directories. When something must be saved, record the decision, the evidence locations, and the next step, without creating several documents that say the same thing. If a separate skill such as `research-argument-map` is available and the user wants to see how questions, claims, and evidence connect, it can complement this one; neither requires the other.

## Origin

Adapted from the research, experiment, and checklist skills of Agent4Sci (Zhong, Li, Carlini, and Jagielski, 2026; Apache License 2.0) and rewritten for HCI, social computing, computational social science, and technical systems research. Sources and changes: https://github.com/kydchen/research-iteration/blob/main/PROVENANCE.md
