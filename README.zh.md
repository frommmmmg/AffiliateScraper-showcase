<div align="center">

# AffiliateScraper

[English](README.md) · 中文 · [Español](README.es.md) · [Deutsch](README.de.md) · [Français](README.fr.md)

🌐 Feeds **[affproof.com](https://affproof.com)** · [GitHub @frommmmmg](https://github.com/frommmmmg)

</div>

> **本仓库仅用于展示，不公开源码。** AffiliateScraper 不开源，所以这里没有代码，只介绍它做什么、怎么构建、长什么样。想聊聊它，请通过我的 [GitHub 主页](https://github.com/frommmmmg)联系我。

**挖掘值得加入的联盟项目的雷达。** 它找的是独立 SaaS 和 AI 公司在 Tolt、Rewardful、PromoteKit、FirstPromoter、PartnerStack 等平台上自助托管的联盟项目，而不是大型封闭联盟市场。

付得最高的项目很少出现在联盟市场里。它们就在公司自己的注册页上，而每个托管平台都会在网址和措辞里留下可辨认的痕迹。AffiliateScraper 把这些痕迹变成搜索规则，然后做那些枯燥的部分：读取搜到的内容，提取佣金条款，给每个项目评级，并把一切存成可以筛选、导出、由人复核的形式。

| | |
|---|---|
| **我的角色** | 一个人设计并构建，是 AffProof 数据流水线的发现阶段 |
| **状态** | 日常使用中 |
| **产出** | CSV、JSON 和 Markdown 导出，以及一个决定该写什么的关键词层 |
| **技术栈** | Python · SQLite · Pydantic · 搜索 API（DuckDuckGo、Google CSE、Serper） |

### 它能做什么

**发现**
- **基于 Dork 的搜索。** 维护一套搜索规则库，每个托管平台一族规则，另有排除名单，把博客和评测站挡在外面。搜索可通过 DuckDuckGo、Google CSE 或 Serper 运行，代理设置可配置。
- **瞄准对的项目。** 它找的是 30% 到 50% 的持续分成、免审即过、有公开注册链接的项目，而不是一次性付费。

**理解**
- **结构化解析。** 品牌名、佣金比例、持续还是一次性、Cookie 有效期、提现门槛、审核方式和所属赛道，都由 Pydantic 模型提取并校验。
- **简单的评级。** S、A、B 三级，S 代表 30% 以上的持续分成且转化潜力高。

**存储与输出**
- **干净的存储与导出。** SQLite 对注册链接去重并加唯一约束，导出为 CSV、JSON 和 Markdown，同一份数据可以在表格、前端或笔记里打开。

**关键词层**
- **从"谁给我分佣"到"我该写什么"。** AI 不依赖付费 SEO 工具来判断搜索意图，把关键词分成四个等级，从快要掏钱的人到只是好奇的人。成交量、竞争度和出价字段预留给真实的 Keyword Planner 数据，因为广告主的出价就是需求真实存在的证明。

## 截图

![在命令行列出内置的示例项目（公开的示例数据）。](assets/cli-list.png)
*在命令行列出内置的示例项目（公开的示例数据）。*

## 工作原理

![从搜索查询到排好序、已去重的项目清单。](assets/affiliatescraper-pipeline.svg)
*从搜索查询到排好序、已去重的项目清单。*

<!--notes-->
## 工程笔记

- **刻意朴素的技术栈。** Python、SQLite 和 Pydantic，流程里没有任何付费 SEO 工具，所以一台笔记本就能跑，数据都在一个文件里。
- **一次只做一步。** 每条命令只做一件事就停下，不会自己接着跑下一步，这样什么能进数据库始终由人说了算。
- **每个条目都有人工核对。** 人工流程分三步：确认是真实的独立注册页，按佣金条款定级，再试注册看是否即时通过。
- **输出能被其他工具读取。** 同一张表写出 CSV（给表格）、JSON（给前端）和 Markdown（给笔记）。
- **为服务更大的东西而建。** 它是 AffProof 流水线的发现阶段，后面的阶段负责收集证据、撰写档案、过门禁、导入和翻译。

**其他项目展示:** [AffProof](https://github.com/frommmmmg/AffProof-showcase) · [Tonu.app](https://github.com/frommmmmg/Tonu.app-showcase) · [AutoPin-CS](https://github.com/frommmmmg/AutoPin-CS-showcase)

---

<div align="center">

<sub>截图只使用示例或公开数据。© 保留所有权利。描述文字可注明出处后引用，软件本身不可再分发。</sub>

</div>
