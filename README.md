# 《AI时代商业分析新工作方法》配套 Skills 工具包

版本：`2026.08.26-rc2`  
状态：作者官方 GitHub 发布版；使用前仍应在目标模型与平台复测。  
作者：龙叔

> 本仓库仅收录《AI时代商业分析新工作方法》的配套 Skills。九个 Skill 统一放在 [`skills/`](skills/) 目录中，不与作者或其他项目的 Skill 混放。本仓库由权利人公开发布；公开可访问不等于采用 MIT、Apache、BSD、Creative Commons 等开源许可，具体使用边界以 [LICENSE.md](LICENSE.md) 为准。

这九个 Skills 不是九个可以替人拍板的“机器人”，而是商业分析工作流中的九个专业工位。它们把需求澄清、指标口径、数据质量、诊断、SQL、来源、一页报告、反向质疑和复盘拆成可复用的检查协议，并明确什么时候必须由人确认。

## 工具目录

| 中文用途 | Skill 目录 | 何时使用 | 主要输出 | 人工闸门 |
|---|---|---|---|---|
| 需求澄清 | [`clarify-analysis-request`](skills/clarify-analysis-request/) | 收到模糊需求时 | 决策任务书、可证伪问题、必要假设 | 决策、范围与授权 |
| 指标口径 | [`define-business-metric`](skills/define-business-metric/) | 取数前或口径冲突时 | 指标卡、冲突矩阵、口径影响 | 口径负责人冻结 |
| 数据质量 | [`assess-data-quality`](skills/assess-data-quality/) | 分析前或结论复核时 | 七维质量报告、使用判定 | 是否安全继续分析 |
| 根因诊断 | [`diagnose-metric-root-cause`](skills/diagnose-metric-root-cause/) | 指标异常或差距诊断时 | 贡献桥、替代解释、补证计划 | 因果措辞与业务机制 |
| SQL 审查 | [`review-analysis-sql`](skills/review-analysis-sql/) | SQL 支撑指标或结论时 | 风险清单、修订逻辑、对账查询 | 生产执行权限与业务口径 |
| 来源核验 | [`verify-claim-sources`](skills/verify-claim-sources/) | 使用外部事实或 AI 主张时 | 主张—来源台账、可用措辞 | 公开引用与时效 |
| 一页分析 | [`draft-one-page-analysis`](skills/draft-one-page-analysis/) | 决策交付前 | 四层闭环决策页、局限、行动 | 结论、预算、责任与承诺 |
| 反向质疑复检 | [`red-team-business-analysis`](skills/red-team-business-analysis/) | 定稿或答辩前 | 高风险质疑、证据计划、降级回答 | 补证、弱化或删除结论 |
| 项目复盘 | [`capture-analysis-retrospective`](skills/capture-analysis-retrospective/) | 项目有结果后 | 内部复盘、复用资产、脱敏作品集 | 结果口径与公开范围 |

“反向质疑复检”是读者名称；`red-team-business-analysis` 是技术目录名。它的目的不是帮人把证据不足的结论“圆过去”，而是主动找出问题定义、口径、样本、因果、成本、阻力和隐私漏洞。

## 建议组合

常用主线：

`需求澄清 → 指标口径 → 数据质量 → 根因诊断 → 来源核验 → 一页分析 → 反向质疑复检 → 项目复盘`

SQL 审查按需插入指标计算和诊断阶段。简单任务不必为了“九个都用上”机械增加流程；但凡结论会影响预算、人员、客户、合规或公开传播，至少应完成指标/质量、来源和反向质疑复检。

## 目录结构

每个 Skill 均包含：

- `SKILL.md`：触发场景、核心步骤、输出和停止条件；
- `agents/openai.yaml`：界面显示信息；
- `references/test-cases.md`：一个最小成功样例和一个失败样例。

在支持 `SKILL.md` 的 Codex 或兼容环境中，可按目标平台当前说明导入单个 Skill 目录。请保留目录层级和文件名。平台、模型、联网、数据库或企业系统权限不随本工具包提供。

## 读者可以怎样使用

通过正规渠道取得本书及本工具包的读者，可以依照[随书读者使用许可](LICENSE.md)：

- 用于个人学习、本人工作，以及所属组织内部的安装、修改和运行；
- 将 Skill 的运行输出用于本职工作和商业分析交付；
- 在组织内部为同一内部工作目的保留必要副本和修改版。

这不是开源许可。不得把原始或修改后的 Skill 文件独立再发行、转售、镜像、转授权、放入公共仓库，或做成面向第三方的公共托管服务。作者与出版方另有书面合同或授权的，以书面约定为准。

## 发布前必读

1. 先读[随书读者使用许可](LICENSE.md)和[版本与使用边界说明](docs/版本与使用边界说明.md)。读者可以在许可范围内用于本人工作和组织内部使用，但不能独立再发行 Skill 文件。
2. 查阅[最小测试结果摘要](docs/最小测试结果摘要.md)和[失败样例摘要](docs/失败样例摘要.md)。
3. 克隆或下载本仓库后，按需将 `skills/<skill-name>/` 复制到目标环境的 Skills 目录；不要打散 Skill 内部层级。
4. 在实际采用的模型和平台上重新运行正向、失败和越权样例；模型升级后也应复测。

Skills 能帮助人稳定检查，但不能替作者、分析者、数据负责人、法务或业务决策人承担事实和结果责任。
