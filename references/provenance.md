# 来源与适配说明

本版本于 2026-10-25 根据 Agent4Sci 的三个 skill 重新组织和改写，供 HCI、社会计算与技术系统研究使用。它是本地适配版，不是作者发布的原版，也未经过 Agent4Sci 的性能评估。

原作者声明：Copyright 2026 Ming Zhong, Stacy Li, and the Agent4Sci authors。上游采用 Apache License 2.0，完整条款保存在本 skill 的 [LICENSE](../LICENSE)。

## 可核对的上游版本

- 论文：[Automating ML for Science: Can Frontier Agents Climb Scientific Hills in the Wild?](https://arxiv.org/html/2610.28763v1)，相关内容为 Section 4、Appendix A.5 和 Appendix D。
- 仓库：[maszhongming/agent4sci](https://github.com/maszhongming/agent4sci)。
- 本次读取的仓库提交：`74b0e8c4dc55610072bed4326b6bfac24dc77377`，它是本次检索到的版本，不宣称就是论文实验时的版本。
- [research/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/research/SKILL.md)
- [experiment/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/experiment/SKILL.md)
- [checklist/SKILL.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/checklist/SKILL.md)
- [experiment/best_practices.md](https://github.com/maszhongming/agent4sci/blob/74b0e8c4dc55610072bed4326b6bfac24dc77377/agent4sci/skills/agents/skills/experiment/best_practices.md)

## 三个环节如何适配

| 环节 | 保留的用途 | 本地修改 |
| --- | --- | --- |
| Research | 以文献和领域知识形成有区别的思路，检查创新性 | 用最近已有工作与具体证据校准贡献，涵盖定性、设计和经验研究，允许边看实现边修正问题 |
| Experiment | 小规模运行、过程记录、失败诊断和资源管理 | 先核验基线，优先能改变决定的验证，遵守预算与停止条件，复用项目日志和既定执行分工 |
| Checklist | 检查方向是否变窄，并采取纠正行动 | 在结果与决策节点触发，允许继续、修改、换方向或收尾，长任务可补充时间检查 |

原版面向已准备好的科学机器学习基准和充足 GPU 资源。本地版本移除了强制高风险优先、用满所有 GPU、禁止必要基线复现、默认多代理、固定四份文献报告，以及必须保持会话活跃的要求。没有安装原仓库的钩子、轮询脚本或模型配置。

## 如何理解效用证据

论文的主比较测试三个 skill 的组合，不能据此判断每一个环节的独立贡献。作者在 Appendix A.5 承认对既有任务及 Claude 行为适配的局限。本地版对 HCI、社会计算、定性研究和当前模型的帮助仍需通过实际任务检验。

后续观察重点是：是否减少无依据的创新性判断，是否用更小的验证区分关键解释，负结果是否改变后续决定，以及时间和成本是否更合理。完成更多步骤或产生更多文档本身不构成有效性证据。
