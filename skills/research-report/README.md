# Research 报告写作与调查技能

把研究问题、可追溯证据、分析方法、反方解释和可证伪结论组织成一份 Research 报告。适用于公司、行业、协议和技术研究；重点是形成判断的过程，而非只做观点摘要。

技能入口：[`SKILL.md`](SKILL.md)。完整规范分为[报告格式规范](references/report-format.md)和[调查与证据规范](references/evidence-method.md)。

## 安装与使用

这是一个以 `SKILL.md` 为入口的文件夹技能，没有运行时依赖，也不要求特定搜索、数据库或浏览器供应商。

1. 下载或克隆本仓库，将 **整个** `skills/research-report` 文件夹复制到你的 agent 支持的技能目录。
2. Codex 可放到 `~/.codex/skills/research-report`；Claude Code 可放到 `~/.claude/skills/research-report`。具体发现机制以所用客户端为准。
3. 若 agent 不支持技能发现，直接让它读取该目录中的 `SKILL.md`，并允许它按相对路径读取所引用文件。仅复制入口文件会丢失完整规范。
4. 联网研究需要 agent 自身具备检索能力；无法联网时，技能要求明确限制结论，而非虚构最新数据。

调用示例：

```text
请使用 $research-report 分析【公司或行业】。
研究问题：【最需要回答的决策问题】。
分析时点：【日期和时区】；统计期间：【期间】；预测期：【期间】。
比较对象：【对象或选择原则】；材料：【链接或附件】。
请给出完整版报告、关键事实表、反方解释、3–5 个验证指标和数据缺口。
```

其他 agent 可将 `$research-report` 替换为“读取 skills/research-report/SKILL.md 并遵循其中的研究流程”。用户指定的语言、篇幅和章节顺序优先于默认模板。

## 文件用途

| 文件 | 用途 |
|---|---|
| `SKILL.md` | 激活范围、工作流程、证据底线和文件导航 |
| `references/report-format.md` | 第一部分：章节、标题、摘要、图表、风险和表达规则 |
| `references/evidence-method.md` | 第二部分：调查、来源核验、冲突处理、建模和证伪规则 |
| `references/provenance.md` | 方法来源、样本观察边界、原创与非背书声明 |
| `assets/task-card.md` | 开题时复制填写的任务卡 |
| `assets/report-template.md` | 可删改的完整报告骨架 |
| `assets/evidence-ledger.csv` | 来源和数据口径台账的字段模板 |
| `assets/claim-tests.csv` | 支持条件、证伪条件和追踪计划的字段模板 |
| `agents/openai.yaml` | 可选的 Codex 展示元数据 |

CSV 文件仅含表头；研究时填写实际记录。模板中的方括号是填写提示，不是研究结果。

## 设计边界

- 严格区分核实事实、管理层说法、第三方估算、分析者估算、分析推断和未知。
- 来源可追溯、算术复算、独立验证是三种不同状态。
- 样本中的共同结构是观察；交叉核验、证伪和审计要求多为新增规范，不能冒称原作者做过。
- 不模仿作者个人语言，不代表 ARK、J.P. Morgan 或任何分析师，不附带评级或目标价。
- 金融研究输出为研究框架和判断依据，不构成投资建议。

许可证：MIT。许可证只覆盖本项目原创内容；参考报告及其图表、数据和商标保留各自权利。
