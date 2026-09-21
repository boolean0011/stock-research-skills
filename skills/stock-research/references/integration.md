# 与 Public Equity Investing 的分工

本 Skill 只在用户选择这套 prompt 编排方法时主导流程。普通单项股票研究优先交给现有 Public Equity Investing，避免重复触发。

## 发现与读取

从当前会话技能清单中查找 `public-equity-investing` 或带插件前缀的同名技能，并读取其实际 `SKILL.md`。按它的 invocation-policy、routing-playbook、交付要求进入具体专业流程；专业 skill 的路径相对该已安装目录解析。不要写死本机用户名、缓存版本或假设存在某个 MCP 工具。

本次已确认的标的、时间、资料范围和交付格式传给专业流程，避免每个模块重复询问或重新设置来源。缺少实质输入时仍遵守其检查要求。用户要求完整研究报告以外的单项专业成果时，把最终专业判断交给对应 owner，而非让总控冒充建模工具。

## 复用映射

只加载任务确需的能力，不一次性读取全插件。

| 本流程需要 | 可复用的专业 skill |
| --- | --- |
| 公司身份与事实快照 | company-tearsheet |
| 完整覆盖研究 | initiating-coverage |
| 财报后更新 | earnings-deep-dive |
| 同业估值或现金流估值 | comps-valuation / dcf-model-builder |
| 多空论据与预期差 | long-short-pitch |
| 宏观对上市公司的影响 | economic-impact-report |
| 投资假设与催化剂更新 | thesis-tracker / catalyst-calendar |
| 已有证据的情景计算 | scenario-sensitivity-generator |
| 有明确组合约束的风险分析 | portfolio-risk-management |
| 汇总已完成的研究 | memo-builder |
| 重要报告的来源与口径复核 | deck-report-qc |

执行专业流程后，将其有效输出、来源、假设和限制导入本次模块文件。已提供可用模型或专业分析时优先复用，不为完成角色表演重复建模。总控的综合结论不能覆盖专业流程中未通过的估值或来源检查。

多空角色可复用专业方法与已核验模型，但仍需各自形成并交付本轮论证；已有多空报告不能自动替代看涨研究员、看跌研究员的分别执行。

## 降级

插件未安装、路径不可读或专业能力不适用时，明确说明采用本 Skill 内置模块方法，继续已有资料支持的研究。此时不宣称调用了插件或完成了专业模型。

插件可用不代表 FactSet、Quartr、券商行情或社交平台已授权。按本轮实际可调用工具验证所需来源，数据不足遵循 contracts.md；不自行安装插件、开通付费服务、获取凭据或更改配置。
