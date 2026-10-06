<div align="center">

# AffiliateScraper

[English](README.md) · 中文 · [Español](README.es.md) · [Deutsch](README.de.md) · [Français](README.fr.md)

</div>

> **本仓库仅用于展示，不公开源码。** AffiliateScraper 是私有项目，所以这里没有代码，只介绍它做什么、怎么构建、长什么样。想聊聊它，请通过我的 [GitHub 主页](https://github.com/frommmmmg)联系我。

**挖掘值得加入的联盟项目的雷达。** 它瞄准独立 SaaS 和 AI 公司在 Tolt、Rewardful、PromoteKit、FirstPromoter、PartnerStack 等平台上运营的持续分成项目，而不是大型封闭联盟市场。

**亮点**

- **基于 Dork 的发现。** 维护一套规则库和排除名单，通过 DuckDuckGo、Google CSE 或 Serper 运行。
- **结构化解析。** 品牌名、佣金比例、持续分成还是一次性、所属赛道，都由 Pydantic 模型提取并校验。
- **干净的存储与导出。** SQLite 自动去重、带唯一约束，可导出为 CSV、JSON 和 Markdown。
- **AI 关键词层。** 把产品库变成值得写的页面清单，并标注搜索意图等级，不依赖付费 SEO 工具。
- **一行命令的 CLI**，覆盖载入、查看、搜索、导出和生成关键词。

它同时为 AffProof 的尽调流水线供数。

**技术栈：** Python · SQLite · Pydantic · 搜索 API

## 截图

![在命令行列出内置的示例项目（公开的示例数据）。](assets/cli-list.png)
*在命令行列出内置的示例项目（公开的示例数据）。*

## 工作原理

![从搜索查询到排好序、已去重的项目清单。](assets/affiliatescraper-pipeline.svg)
*从搜索查询到排好序、已去重的项目清单。*

---

<div align="center">

<sub>截图只使用示例或公开数据。© 保留所有权利。描述文字可注明出处后引用，软件本身不可再分发。</sub>

</div>
