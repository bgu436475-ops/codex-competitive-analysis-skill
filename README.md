# Evidence-First Competitive Analysis for Codex

一个面向 OpenAI Codex 的证据优先竞争分析 Skill：保留定位、产品、定价、客户证明、市场空位与建议等分析框架，同时要求实际体验记录、事实与推断分离、证据等级、逐条可点击来源和访问日期。

> **非官方项目。** 本项目不是 Anthropic 或 OpenAI 的官方产品，也不代表任何一方的认可。

## 安装

Codex 官方的 [Build Skills 指南](https://learn.chatgpt.com/docs/build-skills.md) 说明：项目级 Skill 放在仓库的 `.agents/skills`，个人级 Skill 放在 `$HOME/.agents/skills`。

安装到当前仓库：

```bash
mkdir -p .agents/skills
cp -R /path/to/codex-competitive-analysis-skill/competitive-analysis .agents/skills/
```

安装为个人 Skill：

```bash
mkdir -p "$HOME/.agents/skills"
cp -R /path/to/codex-competitive-analysis-skill/competitive-analysis "$HOME/.agents/skills/"
```

Codex 会自动检测 Skill 变化；若没有出现，再重启 Codex。

## 使用

用 `$` 明确调用，可减少是否触发的歧义：

```text
请使用 $competitive-analysis，对 Cursor、GitHub Copilot、Claude Code 和 OpenAI Codex
做一份面向产品负责人的竞争分析。请核对当前定价，记录能够实际执行的体验路径，
区分事实、观察、推断和建议，并附逐条来源登记与主张登记。
```

Skill 会按当前环境中**实际可用**的网页搜索、浏览器、连接器和本地文件能力开展研究；它不假定某项工具一定存在。能力或来源不可用时，报告必须说明限制，未执行的产品路径必须标为 `Not firsthand-verified`。

## 证据模型

- **FACT：**来源直接支持、可核验的事实。
- **OBSERVATION：**按可复现步骤亲自得到的结果。
- **INFERENCE：**从已引用证据推出的解释，并标注置信度。
- **RECOMMENDATION：**服务具体决策、依赖已登记主张的行动。
- **A–D 证据等级：**A 为亲历或官方直接来源，B 为透明且可独立核验的可靠第三方，C 为社区、聚合或单一轶事，D 仅作待核线索。

关键事实必须给出精确页面链接和访问日期；战略推断原则上需要两个独立支持，否则降置信度并解释缺口。正式报告先建立原子化主张登记，再由登记内容生成正文。

## 仓库内容

- [`competitive-analysis/SKILL.md`](competitive-analysis/SKILL.md)：核心工作流与证据规则。
- [`competitive-analysis/references/report-template.md`](competitive-analysis/references/report-template.md)：可复用调研报告模板。
- [`competitive-analysis/agents/openai.yaml`](competitive-analysis/agents/openai.yaml)：Codex 界面元数据。
- [`examples/cursor/prompt.md`](examples/cursor/prompt.md)：固定 A/B 输入。
- [`examples/cursor/baseline-report.md`](examples/cursor/baseline-report.md)：只使用普通提示词、未经回写的独立输出。
- [`examples/cursor/skill-report.md`](examples/cursor/skill-report.md)：加入本 Skill 后独立生成，并按 Skill 合约完成结构审计修订的最终输出。
- [`examples/cursor/comparison.md`](examples/cursor/comparison.md)：同一量表的逐项评分与局限。

## A/B 示例结论

在一次 Cursor 配对演示中，普通提示词报告为 **17/30**，Skill 报告为 **24/30**。最终 Skill 报告登记了 15 条来源和 32 条主张，提升主要来自主张可核验性与事实/推断分离；来源质量、分析深度和决策价值没有提高。它记录了四个公开入口的实际返回，但没有走通产品内部路径。普通报告保留原始独立输出；Skill 报告由全新 prompt+Skill-only 运行独立生成，随后按 Skill 合约做了结构审计修订，因此这是流程演示，不是盲测基准，也不表示统计显著性；请看[完整评分依据](examples/cursor/comparison.md)。

## 限制

- Skill 改善研究过程和输出约束，不能保证来源本身正确，也不能替代人工复核。
- 证据登记会增加搜索、核验和排版成本；示例中 Skill 报告的 Markdown 字符数约为普通报告的 3.21 倍。
- 官方来源适合确认产品自述，不等于独立验证。高风险决策仍应补充客户访谈、真实试用、合同条款和独立数据。
- 定价、功能和采用数据会变化；复用报告时必须刷新访问日期与来源。

## 上游与许可证

本项目改编自 Anthropic `knowledge-work-plugins` 仓库中固定版本的[历史 `competitive-analysis` Skill](https://github.com/anthropics/knowledge-work-plugins/blob/1316b6508366108158cf08503363d4b4cbc699e5/marketing/skills/competitive-analysis/SKILL.md)，并参考其固定版本的[当前后继 `competitive-brief` Skill](https://github.com/anthropics/knowledge-work-plugins/blob/47caa757e4730eb8daf7d335470f692d4a68b59e/marketing/skills/competitive-brief/SKILL.md)。上游采用 [Apache License 2.0](https://github.com/anthropics/knowledge-work-plugins/blob/1316b6508366108158cf08503363d4b4cbc699e5/marketing/LICENSE)；本项目对内容作了 Codex 化和证据优先修改，并同样按仓库根目录 [`LICENSE`](LICENSE) 中的 Apache-2.0 条款发布。上游所检查版本未包含需要继承的 `NOTICE` 文件。
