# Research Iteration：研究构思与迭代

[English](README.md)

把研究构思、试点结果或停滞的项目推进为下一步值得做的研究。这个 skill 帮助代理核对已有工作，选择能区分不同解释的小规模研究，并在新证据出现时调整方向。

适用于人机交互（HCI）、社会计算和技术系统研究，包括定性研究、设计研究、实验与系统测量。它将 [Agent4Sci](https://github.com/maszhongming/agent4sci) 的 research、experiment 和 checklist 三个 skill 整合为一个入口，只在需要时加载对应参考文件。

## 一个入口，三个环节

| 环节 | 适用时机 | 帮助形成什么 |
| --- | --- | --- |
| 研究构思 | 选择研究问题，比较不同方向 | 有依据的问题、与已有工作的具体差别，以及最小的第一步研究 |
| 验证管理 | 规划、开展或解释试点 | 可比较的条件、可追溯的结果、资源预算，以及继续或停止的理由 |
| 阶段反思 | 证据冲突、进展停滞，或准备扩大投入 | 根据证据决定继续、修改、换方向或收尾 |

从当前需要的环节进入。讨论选题不会自动启动实验，也不要求加载全部参考文件。沿用项目既有分工、研究记录和数据访问规则。

## 相比 Agent4Sci 改了什么

原版面向已有基线和充足 GPU 资源的科学机器学习基准。本版本保留文献依据、创新性校准、小规模试跑、失败诊断和方向反思，并调整了以下工作假设：

- 按知识增益和区分解释的能力选择下一步。风险高、实现复杂，本身不等于研究有价值。
- 必要时核验基线，条件匹配时复用可靠结果，允许必要的基线复现。
- 遵守项目资源预算，不因为 GPU 空闲就增加实验。
- 根据方法采用合适的证据标准，不强行把访谈、田野和设计研究写成指标优化或因果实验。
- 在关键结果和决策节点反思，不安装钩子、计时器、后台任务，也不强制使用多代理。

来源版本和具体改动见 [provenance.md](references/provenance.md)。

## 安装

skill 由 Markdown 指令和可选显示信息组成，没有软件包依赖或附带的可执行脚本。具体研究仍可能需要项目相应的工具和数据。

根据使用的代理选择安装位置。下面的命令用于首次安装，目标目录已存在时会停止。

### Codex

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/kydchen/research-iteration.git ~/.agents/skills/research-iteration
```

若只在一个项目中使用，可改为克隆到该项目的 `.agents/skills/research-iteration`。这些路径遵循 [Codex 官方 skill 文档](https://learn.chatgpt.com/docs/build-skills#where-to-save-skills)。如果已有其他位置的副本能被识别，更新原副本即可，避免重复安装。新 skill 未出现时可重启 Codex。

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/kydchen/research-iteration.git ~/.claude/skills/research-iteration
```

项目内安装使用 `.claude/skills/research-iteration`，详见 [Claude Code 官方 skill 文档](https://code.claude.com/docs/en/skills)。`agents/openai.yaml` 提供 Codex 显示信息，Claude Code 不依赖这个文件。

## 使用示例

Codex 使用 `$research-iteration`，Claude Code 使用 `/research-iteration`。请求与描述匹配时，代理也可以自行选择这个 skill。

### 形成研究问题

```text
$research-iteration 根据这份提案和附上的论文，比较两个研究方向。核对最接近的已有工作，推荐一个能改变我们判断的小规模研究。
```

### 规划试点

```text
$research-iteration 我们有一批关于人们如何检查 AI 生成内容的访谈笔记。请规划一次试点分析，保留参与者的情境，并区分提案中已有的不同解释。不要采集新数据。
```

### 调整停滞的方向

```text
$research-iteration 检查这些实验记录。我们已经学到了什么，哪些解释仍可能成立，在剩余预算内应该继续、修改设计，还是停止？
```

在 Claude Code 中，将示例里的 `$research-iteration` 换成 `/research-iteration`。提供实际已有的材料即可，缺失证据应保留为未决项。

skill 正文、参考文件和显示信息均使用英文维护。回答与交付物仍跟随用户指定的输出语言，未指定时跟随提问语言。README 保留中英文版本，两份说明对应同一套 skill。

## 文件与相关流程

- [SKILL.md](SKILL.md)：入口、研究构思和环节选择。
- [references/experiment.md](references/experiment.md)：验证的规划、执行与解释。
- [references/reflection.md](references/reflection.md)：结果和决策节点的反思。
- [references/provenance.md](references/provenance.md)：来源版本、适配选择和证据边界。
- [agents/openai.yaml](agents/openai.yaml)：Codex 显示信息。

如果另行安装了 `research-argument-map`，可以用它检查研究问题、主张与证据之间的关系。Research Iteration 侧重决定下一步研究，两者都不要求自动串联写作润色。

## 效用证据与局限

[Agent4Sci 论文](https://arxiv.org/html/2610.28763v1) 在科学机器学习基准上评估了原版三个 skill 的组合。这些结果不能单独证明每个 skill 的贡献，也不能直接证明本适配版对 HCI、社会计算或定性研究有效。

本版本已通过 skill 格式和内部链接检查，尚未通过受控比较评估其对真实研究结果的影响。Claude Code 的安装说明依据其官方 skill 格式，但本适配版尚未在 Claude Code 中完成端到端测试。研究是否新颖、方法是否充分、结论能支持到哪里，仍需根据实际来源和证据判断。

## 来源与许可

改编自 [Agent4Sci](https://github.com/maszhongming/agent4sci)，本次使用的来源快照为提交 [`74b0e8c`](https://github.com/maszhongming/agent4sci/tree/74b0e8c4dc55610072bed4326b6bfac24dc77377)。指令于 2026-10-25 重新组织和改写。本版本为独立适配，并非原作者发布的原版。

上游版权声明：Copyright 2026 Ming Zhong, Stacy Li, and the Agent4Sci authors.

采用 [Apache License 2.0](LICENSE)。
