<div align="center">

# AffiliateScraper

English · [中文](README.zh.md) · [Español](README.es.md) · [Deutsch](README.de.md) · [Français](README.fr.md)

🌐 Feeds **[affproof.com](https://affproof.com)** · [GitHub @frommmmmg](https://github.com/frommmmmg)

</div>

> **This repository is a showcase, not a source release.** AffiliateScraper is closed-source, so there is no code here, only what it does, how it is built and what it looks like. To talk about it, get in touch through my [GitHub profile](https://github.com/frommmmmg).

**A radar for affiliate programs worth joining.** It finds the self-serve programs that independent SaaS and AI companies host on platforms such as Tolt, Rewardful, PromoteKit, FirstPromoter and PartnerStack, instead of the big closed marketplaces.

The best-paying programs are rarely in a marketplace. They sit on a company's own sign-up page, and each hosting platform leaves a recognisable footprint in its URLs and wording. AffiliateScraper turns those footprints into search rules, then does the boring part: it reads what it finds, extracts the commission terms, grades each program, and stores everything in a form that can be filtered, exported and checked by a person.

| | |
|---|---|
| **Role** | Designed and built by one person, as the discovery stage of the AffProof data pipeline |
| **Status** | In daily use |
| **Output** | CSV, JSON and Markdown exports, plus a keyword layer for deciding what to write |
| **Stack** | Python · SQLite · Pydantic · search APIs (DuckDuckGo, Google CSE, Serper) |

### What it does

**Discovery**
- **Dork-based search.** A maintained library of search rules, one family per hosting platform, with exclusion lists to keep blogs and review sites out. Searches run through DuckDuckGo, Google CSE or Serper, and the proxy settings are configurable.
- **Aimed at the right programs.** Recurring commissions of 30% to 50%, instant approval and a public sign-up link are what it looks for, rather than one-off payouts.

**Understanding**
- **Structured parsing.** Brand, commission rate, recurring versus one-off, cookie duration, payout threshold, approval type and category are extracted and validated with Pydantic models.
- **A simple grade.** S, A and B ratings, where S means a recurring commission of 30% or more with strong conversion potential.

**Storage and output**
- **Clean storage and export.** SQLite with de-duplication and unique constraints on the sign-up URL, exported to CSV, JSON and Markdown so the same data opens in a spreadsheet, a front end or a note.

**A keyword layer**
- **From "who pays me" to "what do I write".** The AI judges search intent without paid SEO tools and sorts keywords into four levels, from people about to buy to people who are only curious. Fields for volume, competition and bid are reserved for real Keyword Planner data, because an advertiser's bid is proof that demand is real.

## Screenshots

![Listing the seeded sample programs from the command line (public sample data).](assets/cli-list.png)
*Listing the seeded sample programs from the command line (public sample data).*

## How it works

![From a search query to a ranked, de-duplicated program list.](assets/affiliatescraper-pipeline.svg)
*From a search query to a ranked, de-duplicated program list.*

<!--notes-->
## Engineering notes

- **A deliberately plain stack.** Python, SQLite and Pydantic, with no paid SEO tool in the loop, so it runs on a laptop and the data stays in one file.
- **One step at a time.** Every command does one job and stops. Nothing chains into the next step on its own, which keeps a person in charge of what enters the database.
- **A human check on every entry.** The manual routine is three steps: confirm it is a real independent sign-up page, grade it by commission terms, and test the sign-up to see whether approval is instant.
- **Output that other tools can read.** CSV for spreadsheets, JSON for front ends and Markdown for notes, written from the same table.
- **Built to feed something bigger.** It is the discovery stage of the AffProof pipeline, whose later stages collect evidence, write the dossier, gate it, import it and translate it.

**Other showcases:** [AffProof](https://github.com/frommmmmg/AffProof-showcase) · [Tonu.app](https://github.com/frommmmmg/Tonu.app-showcase) · [AutoPin-CS](https://github.com/frommmmmg/AutoPin-CS-showcase)

---

<div align="center">

<sub>Screenshots use sample or public data only. © All rights reserved. Descriptions may be quoted with attribution; the software itself is not for redistribution.</sub>

</div>
