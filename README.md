# wuu Career Skills
由 wuu 设计并与 AI 协作实现的职业证据与岗位定制技能。面向 PE/VC、FA、投行、战略分析、战略投资及企业管培生。
## 三个技能如何协作
1. career-wiki-curator：将本人材料整理为持久化的 Markdown Wiki，保存具体动作、方法、范围、产出、责任和来源；记录冲突。
2. jd-resume-local：拆解 JD，用相关证据组织中英文简历，兼顾文本可解析性、硬要求覆盖和人工阅读效率。
3. resume-evidence-audit：分别检查证据、金融岗位责任边界、机器可读性和人工阅读重点，含重新实现的文本校验脚本。
三个 skill 均为本项目需求驱动、AI 辅助原创整合；外部实现的阅读、取舍与出处见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。
网页工作台已在作者本机应用这些方法。本仓库发布可独立导入的通用技能，不包含网站运行时、本人简历、私有 Wiki、内部报告或登录凭据。
## 安装
下载仓库 ZIP 并解压，将 skills 下的三个完整目录复制到支持 SKILL.md 的宿主技能目录。Codex 可放在用户目录 ~/.agents/skills/。不同宿主的导入菜单和目录不同；本包不是模型、插件安装器或独立 AI 服务。
例如让支持本地技能的助手读取：`skills/career-wiki-curator/SKILL.md`，再使用 `skills/jd-resume-local/SKILL.md`。
## 使用
- “按 career-wiki-curator 整理我提供的这份脱敏成果，保留具体操作和责任边界。”
- “按 jd-resume-local，结合 Wiki 和来源，为以下 JD 输出中文及英文简历。”
- “比较同语言定稿与上一交付版，事实变更和表达偏好分别记录。”
首次使用配置资料目录与身份信息，不把示例候选人作为自己的经历。
## 示例与验证
examples/ 中全部为虚构示意。运行 `python tests/validate_package.py` 检查技能元信息和必要资源。语义、事实与实际分页仍须按技能审查；这些测试不是 ATS 认证。
## 设计取舍
有依据的“按区域拆分并测算同比”优于笼统“支持分析”；同样不为追求具体而捏造样本量或效果。
旧简历、新简历与原始成果共同构成证据池；新稿简洁不代表旧稿细节失效。
## 参考与来源
知识架构受 [Andrej Karpathy 的 LLM Wiki](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) 启发，采用 raw/wiki/schema 与 ingest/query/lint 思路；本仓库另行设计职业证据和责任边界规则，未复制原文全文。
技能设计参考作者提供的既有简历工作流与实际使用反馈，使用 AI 辅助编写代码和文档。不宣称 ATS、面试或录用保证。第三方宿主和模型仍有自己的使用要求。

## 技能沿革
- jd-resume-local：根据用户最初提供的 JD 定制简历 skill 及偏好更新原则重新设计，是主写作技能；保留 STAR、证据映射、双语对齐和迭代方法，不沿用参考作者的个人经历。
- career-wiki-curator：为职业证据整理另行设计的配套技能。
- resume-evidence-audit：参考开源校验/审稿方法重新实现的配套审稿技能。
STAR 是问题/任务、本人行动、结果或交付物的逻辑，不要求每条机械四句，也不为量化捏造结果。
