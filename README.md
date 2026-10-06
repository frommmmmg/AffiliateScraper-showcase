<div align="center">

# AffiliateScraper

English · [中文](README.zh.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Français](README.fr.md)

</div>

> **This repository is a showcase, not a source release.** AffiliateScraper is a private project, so there is no code here, only what it does, how it is built and what it looks like. To talk about it, get in touch through my [GitHub profile](https://github.com/frommmmmg).

**A radar for affiliate programs worth joining.** It targets the recurring-commission programs run by independent SaaS and AI companies on platforms such as Tolt, Rewardful, PromoteKit, FirstPromoter and PartnerStack, instead of the big closed marketplaces.

**Highlights**

- **Dork-based discovery.** A maintained rule library plus exclusion lists, run through DuckDuckGo, Google CSE or Serper.
- **Structured parsing.** Brand name, commission rate, recurring versus one-off and category are extracted and validated with Pydantic models.
- **Clean storage and export.** SQLite with de-duplication and unique constraints, exported to CSV, JSON and Markdown.
- **An AI keyword layer.** Turns the product list into the pages worth writing, with search-intent levels, without paid SEO tools.
- **One-line CLI** for seeding, listing, searching, exporting and generating keywords.

It also feeds AffProof's due-diligence pipeline.

**Stack:** Python · SQLite · Pydantic · Search APIs

## Screenshots

![Listing the seeded sample programs from the command line (public sample data).](assets/cli-list.png)
*Listing the seeded sample programs from the command line (public sample data).*

## How it works

![From a search query to a ranked, de-duplicated program list.](assets/affiliatescraper-pipeline.svg)
*From a search query to a ranked, de-duplicated program list.*

---

<div align="center">

<sub>Screenshots use sample or public data only. © All rights reserved. Descriptions may be quoted with attribution; the software itself is not for redistribution.</sub>

</div>
