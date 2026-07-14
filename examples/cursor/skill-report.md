# Cursor 竞争分析

- **研究日期：** 2026-07-14
- **决策：** Cursor 下一步竞争方向
- **竞品：** GitHub Copilot、Claude Code、OpenAI Codex

## 范围与假设

| 项目 | 范围 |
|---|---|
| 市场/客群 | 全球 AI 编程助手；个人、团队、企业 |
| 重点 | 产品覆盖、价格、采用证明、机会、建议 |
| 限制 | 仅公开网页；美元标价；额度不可直接换算 |

## 执行摘要

- Cursor 的可守定位是整合智能体、云端智能体及企业访问、网络和审计控制的工作台。[I-01]
- Copilot 的 GitHub 分发是 Cursor 的一个威胁；Cursor 的公开采用证明缺少可与竞品周活直接比较的口径。[I-02][I-03]
- Copilot 与 Codex 都可能比 Cursor Pro 具有更低的试用摩擦。[I-06][I-07]
- 优先建设跨提供商智能体控制平面，发布任务成本、测试结果、返工率及策略事件的统一指标，并推出有预算上限和迁移支持的团队试点。[R-01][R-02][R-03]

## 证据支持的发现

Cursor 提供智能体、云端智能体、技能及企业访问、网络和审计控制。[F-01] Cursor 列价为 Hobby 免费、Pro 20 美元/月、Teams 40 美元/用户/月。[F-02] Cursor 客户页称 Brex 超过 70% 工程师使用 Cursor。[F-03] 2026-07-14 审阅 Cursor 定价页与客户页时，两页均未披露全球活跃用户或周活数。[F-04]

GitHub 称 Copilot 覆盖 IDE、GitHub、CLI、代码审查、云端及第三方智能体；微软 FY2025 Q4 电话会称 GitHub Copilot 有 2,000 万用户。[F-05][F-07] Anthropic 称 Claude Code 可读代码库、改文件、跑测试并提交代码；Anthropic 2026-02-12 称 Claude Code 周活自 2026-01-01 起翻倍。[F-08][F-10] OpenAI 称 Codex 覆盖 ChatGPT、编辑器、终端、并行智能体及后台工作；OpenAI 2026-06-02 称 Codex 周活超过 500 万。[F-11][F-14]

## 竞争比较

| 产品 | 产品覆盖 | 价格 | 采用证明 |
|---|---|---|---|
| Cursor | 智能体、云端智能体、技能及企业访问、网络和审计控制。[F-01] | Cursor 列价为 Hobby 免费、Pro 20 美元/月、Teams 40 美元/用户/月。[F-02] | Brex 超过 70% 工程师使用。[F-03] |
| Copilot | GitHub 称 Copilot 覆盖 IDE、GitHub、CLI、代码审查、云端及第三方智能体。[F-05] | Free $0；Pro $10；Pro+ $39；Max $100/月。[F-06] | 微软 FY2025 Q4 电话会称 GitHub Copilot 有 2,000 万用户。[F-07] |
| Claude Code | Anthropic 称 Claude Code 可读代码库、改文件、跑测试并提交代码。[F-08] | Pro $20；Max $100/$200 月付，均含 Claude Code。[F-09] | Anthropic 2026-02-12 称 Claude Code 周活自 2026-01-01 起翻倍。[F-10] |
| Codex | OpenAI 称 Codex 覆盖 ChatGPT、编辑器、终端、并行智能体及后台工作。[F-11] | 覆盖 Free 至 Enterprise；Plus $20/月。[F-12][F-13] | OpenAI 2026-06-02 称 Codex 周活超过 500 万。[F-14] |

## 第一手体验日志

环境均为托管网页读取工具；步骤均为：直接打开入口并记录原始返回。

| 产品/入口 | 实际结果 | 内部路径状态 |
|---|---|---|
| Cursor `https://cursor.com/agents` | `403 Forbidden`。[O-01] | **Not firsthand-verified**：403、无账号、未下载。[O-05] |
| Copilot `https://github.com/copilot` | `You can’t perform that action at this time.`[O-02] | **Not firsthand-verified**：入口不可操作且未登录。[O-06] |
| Claude Code `https://claude.com/code` | 重定向后仅为 `Loading...`。[O-03] | **Not firsthand-verified**：仅加载、未登录、未下载。[O-07] |
| Codex `https://chatgpt.com/codex` | 仅公开营销页，无认证工作区。[O-04] | **Not firsthand-verified**：仅营销页且未登录。[O-08] |

## 优势与弱点

| 优势 | 弱点 | 声明 |
|---|---|---|
| 整合智能体、云端智能体及企业访问、网络和审计控制的工作台。 | 公开采用证明缺少可与竞品周活直接比较的口径。 | I-01, I-03 |

## 缺口与市场机会

| 机会假设 | 客户需要 | 置信度 |
|---|---|---|
| 跨提供商智能体控制平面。[I-04] | 未评估 | 中 |
| 可审计的智能体投入产出层。[I-05] | 未评估 | 低 |

## 优先建议

| 优先 | 建议 | 决策/证据 |
|---|---|---|
| 1 | 建设跨提供商智能体控制平面。[R-01] | 下一能力层；F-01,F-05,F-08,F-11,I-01,I-04 |
| 2 | 发布任务成本、测试结果、返工率及策略事件的统一指标。[R-02] | 企业可信度；F-04,F-07,F-10,F-14,I-03,I-05 |
| 3 | 推出有预算上限和迁移支持的团队试点。[R-03] | 降低切入摩擦；F-02,F-06,F-09,F-12,F-13,I-06,I-07 |

## 限制

- Cursor 当前公开采用证明缺少可与竞品周活直接比较的口径。[I-03]
- Cursor 内部路径因 403、无账号且未下载而为 **Not firsthand-verified**。[O-05]
- Copilot 内部路径因入口不可操作且未登录而为 **Not firsthand-verified**。[O-06]
- Claude Code 内部路径因仅加载、未登录且未下载而为 **Not firsthand-verified**。[O-07]
- Codex 内部路径因仅营销页且未登录而为 **Not firsthand-verified**。[O-08]

## 来源登记表

| ID | 来源 | 类型 | 直接链接 | 日期 | 等级 |
|---|---|---|---|---|---|
| S-01 | Cursor 定价 | 主 | https://cursor.com/cn/pricing | 2026-07-14 | A |
| S-02 | Cursor 客户 | 主 | https://cursor.com/customers | 2026-07-14 | A |
| S-03 | Cursor Agents 入口 | 主 | https://cursor.com/agents | 2026-07-14 | A |
| S-04 | Copilot 计划 | 主 | https://docs.github.com/en/copilot/get-started/plans | 2026-07-14 | A |
| S-05 | 微软 FY2025 Q4 | 主 | https://www.microsoft.com/en-us/investor/events/fy-2025/earnings-fy-2025-q4 | 2026-07-14 | A |
| S-06 | Copilot 入口 | 主 | https://github.com/copilot | 2026-07-14 | A |
| S-07 | Claude Code 产品 | 主 | https://www.anthropic.com/product/claude-code | 2026-07-14 | A |
| S-08 | Claude Pro | 主 | https://support.claude.com/en/articles/8325606-what-is-the-pro-plan | 2026-07-14 | A |
| S-09 | Anthropic Series G | 主 | https://www.anthropic.com/news/anthropic-raises-30-billion-series-g-funding-380-billion-post-money-valuation | 2026-07-14 | A |
| S-10 | Claude Code 入口 | 主 | https://claude.com/code | 2026-07-14 | A |
| S-11 | Codex 产品/入口 | 主 | https://chatgpt.com/codex | 2026-07-14 | A |
| S-12 | Codex 套餐 | 主 | https://help.openai.com/en/articles/11369540-using-codex-with-chatgpt | 2026-07-14 | A |
| S-13 | ChatGPT Plus | 主 | https://help.openai.com/en/articles/6950777-what-is-chatgpt | 2026-07-14 | A |
| S-14 | Codex 采用 | 主 | https://openai.com/index/codex-for-knowledge-work/ | 2026-07-14 | A |
| S-15 | Claude Max | 主 | https://support.claude.com/en/articles/11049741-what-is-the-max-plan | 2026-07-14 | A |

## 声明登记表

| ID | 声明 | 类型 | 等级 | 精确来源 | 日期 | 置信度 | 注释 |
|---|---|---|---|---|---|---|---|
| F-01 | Cursor 计划覆盖智能体、云端智能体、技能及企业访问、网络和审计控制。 | FACT | A | https://cursor.com/cn/pricing | 2026-07-14 | 高 | 产品覆盖 |
| F-02 | Cursor 列价为 Hobby 免费、Pro 20 美元/月、Teams 40 美元/用户/月。 | FACT | A | https://cursor.com/cn/pricing | 2026-07-14 | 高 | 价格 |
| F-03 | Cursor 客户页称 Brex 超过 70% 工程师使用 Cursor。 | FACT | A | https://cursor.com/customers | 2026-07-14 | 中 | 采用；客户自报 |
| F-04 | 2026-07-14 审阅 Cursor 定价页与客户页时，两页均未披露全球活跃用户或周活数。 | FACT | A | https://cursor.com/cn/pricing ; https://cursor.com/customers | 2026-07-14 | 高 | 限定未披露 |
| F-05 | GitHub 称 Copilot 覆盖 IDE、GitHub、CLI、代码审查、云端及第三方智能体。 | FACT | A | https://docs.github.com/en/copilot/get-started/plans | 2026-07-14 | 高 | 产品覆盖 |
| F-06 | Copilot 列价为 Free 0、Pro 10、Pro+ 39、Max 100 美元/月。 | FACT | A | https://docs.github.com/en/copilot/get-started/plans | 2026-07-14 | 高 | 价格 |
| F-07 | 微软 FY2025 Q4 电话会称 GitHub Copilot 有 2,000 万用户。 | FACT | A | https://www.microsoft.com/en-us/investor/events/fy-2025/earnings-fy-2025-q4 | 2026-07-14 | 中 | 采用；口径未定义 |
| F-08 | Anthropic 称 Claude Code 可读代码库、改文件、跑测试并提交代码。 | FACT | A | https://www.anthropic.com/product/claude-code | 2026-07-14 | 高 | 产品覆盖 |
| F-09 | Claude Pro 为 20 美元/月，Max 为 100/200 美元/月，均含 Claude Code。 | FACT | A | https://support.claude.com/en/articles/8325606-what-is-the-pro-plan ; https://support.claude.com/en/articles/11049741-what-is-the-max-plan | 2026-07-14 | 高 | 价格 |
| F-10 | Anthropic 2026-02-12 称 Claude Code 周活自 2026-01-01 起翻倍。 | FACT | A | https://www.anthropic.com/news/anthropic-raises-30-billion-series-g-funding-380-billion-post-money-valuation | 2026-07-14 | 中 | 采用；无绝对数 |
| F-11 | OpenAI 称 Codex 覆盖 ChatGPT、编辑器、终端、并行智能体及后台工作。 | FACT | A | https://chatgpt.com/codex | 2026-07-14 | 高 | 产品覆盖 |
| F-12 | Codex 覆盖 Free、Go、Plus、Pro、Business、Edu、Enterprise。 | FACT | A | https://help.openai.com/en/articles/11369540-using-codex-with-chatgpt | 2026-07-14 | 高 | 计划覆盖 |
| F-13 | ChatGPT Plus 美国月付价格为 20 美元。 | FACT | A | https://help.openai.com/en/articles/6950777-what-is-chatgpt | 2026-07-14 | 高 | 价格 |
| F-14 | OpenAI 2026-06-02 称 Codex 周活超过 500 万。 | FACT | A | https://openai.com/index/codex-for-knowledge-work/ | 2026-07-14 | 中 | 采用；厂商自报 |
| O-01 | 工具打开 Cursor Agents 入口时返回 `403 Forbidden`。 | OBSERVATION | A | https://cursor.com/agents | 2026-07-14 | 高 | 公开入口 |
| O-02 | 工具打开 Copilot 入口时返回 `You can’t perform that action at this time.` | OBSERVATION | A | https://github.com/copilot | 2026-07-14 | 高 | 公开入口 |
| O-03 | 工具打开 Claude Code 入口时重定向后仅显示 `Loading...`。 | OBSERVATION | A | https://claude.com/code | 2026-07-14 | 高 | 公开入口 |
| O-04 | 工具打开 Codex 入口时仅获得公开营销页，无认证工作区。 | OBSERVATION | A | https://chatgpt.com/codex | 2026-07-14 | 高 | 公开入口 |
| O-05 | Cursor 内部路径因 403、无账号且未下载而为 `Not firsthand-verified`。 | OBSERVATION | A | https://cursor.com/agents | 2026-07-14 | 高 | 状态 |
| O-06 | Copilot 内部路径因入口不可操作且未登录而为 `Not firsthand-verified`。 | OBSERVATION | A | https://github.com/copilot | 2026-07-14 | 高 | 状态 |
| O-07 | Claude Code 内部路径因仅加载、未登录且未下载而为 `Not firsthand-verified`。 | OBSERVATION | A | https://claude.com/code | 2026-07-14 | 高 | 状态 |
| O-08 | Codex 内部路径因仅营销页且未登录而为 `Not firsthand-verified`。 | OBSERVATION | A | https://chatgpt.com/codex | 2026-07-14 | 高 | 状态 |
| I-01 | Cursor 的可守定位是整合智能体、云端智能体及企业访问、网络和审计控制的工作台。 | INFERENCE | A | https://cursor.com/cn/pricing | 2026-07-14 | 低 | 仅一项 Cursor 官方来源，缺独立验证；支持 F-01 |
| I-02 | Copilot 的 GitHub 分发是 Cursor 的一个威胁。 | INFERENCE | A | https://docs.github.com/en/copilot/get-started/plans ; https://www.microsoft.com/en-us/investor/events/fy-2025/earnings-fy-2025-q4 | 2026-07-14 | 低 | GitHub/Microsoft 属同一生态，缺独立比较证据；支持 F-05,F-07 |
| I-03 | Cursor 的公开采用证明缺少可与竞品周活直接比较的口径。 | INFERENCE | A | https://cursor.com/cn/pricing ; https://cursor.com/customers ; https://www.microsoft.com/en-us/investor/events/fy-2025/earnings-fy-2025-q4 ; https://www.anthropic.com/news/anthropic-raises-30-billion-series-g-funding-380-billion-post-money-valuation ; https://openai.com/index/codex-for-knowledge-work/ | 2026-07-14 | 中 | 支持 F-03,F-04,F-07,F-10,F-14 |
| I-04 | 跨提供商智能体控制平面是 Cursor 的中置信度机会假设。 | INFERENCE | A | https://cursor.com/cn/pricing ; https://docs.github.com/en/copilot/get-started/plans ; https://www.anthropic.com/product/claude-code ; https://chatgpt.com/codex | 2026-07-14 | 中 | 支持 F-01,F-05,F-08,F-11 |
| I-05 | 可审计的智能体投入产出层是 Cursor 的低置信度机会假设。 | INFERENCE | A | https://cursor.com/cn/pricing ; https://cursor.com/customers ; https://www.microsoft.com/en-us/investor/events/fy-2025/earnings-fy-2025-q4 ; https://www.anthropic.com/news/anthropic-raises-30-billion-series-g-funding-380-billion-post-money-valuation ; https://openai.com/index/codex-for-knowledge-work/ | 2026-07-14 | 低 | 支持 F-04,F-07,F-10,F-14,I-03 |
| I-06 | Copilot 可能比 Cursor Pro 具有更低的试用摩擦。 | INFERENCE | A | https://cursor.com/cn/pricing ; https://docs.github.com/en/copilot/get-started/plans | 2026-07-14 | 中 | 支持 F-02,F-05,F-06 |
| I-07 | Codex 可能比 Cursor Pro 具有更低的试用摩擦。 | INFERENCE | A | https://cursor.com/cn/pricing ; https://help.openai.com/en/articles/11369540-using-codex-with-chatgpt ; https://help.openai.com/en/articles/6950777-what-is-chatgpt | 2026-07-14 | 中 | 支持 F-02,F-12,F-13 |
| R-01 | 建设跨提供商智能体控制平面。 | RECOMMENDATION | A | https://cursor.com/cn/pricing ; https://docs.github.com/en/copilot/get-started/plans ; https://www.anthropic.com/product/claude-code ; https://chatgpt.com/codex | 2026-07-14 | 中 | 下一能力层；支持 F-01,F-05,F-08,F-11,I-01,I-04 |
| R-02 | 发布任务成本、测试结果、返工率及策略事件的统一指标。 | RECOMMENDATION | A | https://cursor.com/cn/pricing ; https://cursor.com/customers ; https://www.microsoft.com/en-us/investor/events/fy-2025/earnings-fy-2025-q4 ; https://www.anthropic.com/news/anthropic-raises-30-billion-series-g-funding-380-billion-post-money-valuation ; https://openai.com/index/codex-for-knowledge-work/ | 2026-07-14 | 低 | 企业可信度；支持 F-04,F-07,F-10,F-14,I-03,I-05 |
| R-03 | 推出有预算上限和迁移支持的团队试点。 | RECOMMENDATION | A | https://cursor.com/cn/pricing ; https://docs.github.com/en/copilot/get-started/plans ; https://support.claude.com/en/articles/8325606-what-is-the-pro-plan ; https://support.claude.com/en/articles/11049741-what-is-the-max-plan ; https://help.openai.com/en/articles/11369540-using-codex-with-chatgpt ; https://help.openai.com/en/articles/6950777-what-is-chatgpt | 2026-07-14 | 中 | 降低切入摩擦；支持 F-02,F-06,F-09,F-12,F-13,I-06,I-07 |
