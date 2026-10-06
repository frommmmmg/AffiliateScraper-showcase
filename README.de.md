<div align="center">

# AffiliateScraper

[English](README.md) · [中文](README.zh.md) · [Español](README.es.md) · Deutsch · [Français](README.fr.md)

</div>

> **Dieses Repository ist ein Schaufenster, keine Quellcode-Veröffentlichung.** AffiliateScraper ist ein privates Projekt, deshalb gibt es hier keinen Code, nur was es kann, wie es gebaut ist und wie es aussieht. Wenn du darüber sprechen möchtest, melde dich über mein [GitHub-Profil](https://github.com/frommmmmg).

**Ein Radar für lohnende Partnerprogramme.** Es zielt auf die Programme mit wiederkehrender Provision, die unabhängige SaaS- und KI-Unternehmen auf Plattformen wie Tolt, Rewardful, PromoteKit, FirstPromoter und PartnerStack betreiben, statt auf die großen geschlossenen Marktplätze.

**Highlights**

- **Entdeckung per Dorks.** Eine gepflegte Regelbibliothek samt Ausschlusslisten, ausgeführt über DuckDuckGo, Google CSE oder Serper.
- **Strukturierte Auswertung.** Markenname, Provisionssatz, wiederkehrend oder einmalig und Kategorie werden mit Pydantic-Modellen extrahiert und validiert.
- **Saubere Speicherung und Export.** SQLite mit Deduplizierung und Unique-Constraints, Export nach CSV, JSON und Markdown.
- **Eine KI-Keyword-Ebene.** Macht aus der Produktliste die Seiten, die zu schreiben sich lohnt, mit Suchintention-Stufen und ohne kostenpflichtige SEO-Tools.
- **Einzeilige CLI** zum Laden, Auflisten, Suchen, Exportieren und Erzeugen von Keywords.

Sie speist außerdem die Prüf-Pipeline von AffProof.

**Technik:** Python · SQLite · Pydantic · Such-APIs

## Screenshots

![Die mitgelieferten Beispielprogramme auf der Kommandozeile (öffentliche Beispieldaten).](assets/cli-list.png)
*Die mitgelieferten Beispielprogramme auf der Kommandozeile (öffentliche Beispieldaten).*

## So funktioniert es

![Von der Suchanfrage zur sortierten, deduplizierten Programmliste.](assets/affiliatescraper-pipeline.svg)
*Von der Suchanfrage zur sortierten, deduplizierten Programmliste.*

---

<div align="center">

<sub>Screenshots verwenden nur Beispiel- oder öffentliche Daten. © Alle Rechte vorbehalten. Beschreibungen dürfen mit Quellenangabe zitiert werden; die Software selbst darf nicht weitergegeben werden.</sub>

</div>
