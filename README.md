# ARK Research 报告方法技能

一套供 AI Agent 使用的 Research 报告写作与调查规范。通过分析公开研究报告的宏观结构，提炼可迁移的方法，并加入来源审计、独立核验、反方解释和证伪条件。

**这是独立项目，不隶属于 ARK Invest，不代表原作者，也不构成任何机构的背书。** 不复制原报告的独特表达、图表或预测；参考材料及提炼边界见[来源说明](skills/research-report/references/provenance.md)。

## 给 AI Agent 的入口

读取 [`skills/research-report/SKILL.md`](skills/research-report/SKILL.md)，再按其中的导航读取所需规范和模板。

- [完整使用与安装说明](skills/research-report/README.md)
- [第一部分：报告格式规范](skills/research-report/references/report-format.md)
- [第二部分：调查与证据规范](skills/research-report/references/evidence-method.md)

将整个 `skills/research-report` 文件夹放入客户端支持的技能目录。技能名称保持为 `research-report`，调用示例：

```text
请使用 $research-report 分析【公司或行业】。
研究问题：【问题】；分析时点：【日期】；统计期间：【期间】。
请给出完整报告、来源、最强反方、验证指标和数据缺口。
```

不支持技能发现的 Agent，可直接读取技能入口和相对路径引用文件。执行最新数据研究需要 Agent 自带检索能力；本项目没有运行时依赖。

## 包含内容

技能入口、两部分完整规范、来源与边界说明、任务卡、报告模板、证据台账、验证指标模板，以及可选 Codex 展示元数据。

MIT 许可证仅覆盖本项目原创内容，参考作品保留各自权利。金融研究输出不构成投资建议。
