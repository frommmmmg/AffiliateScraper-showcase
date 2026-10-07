<div align="center">

# AffiliateScraper

[English](README.md) · [中文](README.zh.md) · [Español](README.es.md) · Deutsch · [Français](README.fr.md)

🌐 Feeds **[affproof.com](https://affproof.com)** · [GitHub @frommmmmg](https://github.com/frommmmmg)

✍️ Von **姜芊泽 (Jiang Qianze)** · WeChat-Offizialkonto: **Pin海引航**

</div>

> **Dieses Repository ist ein Schaufenster, keine Quellcode-Veröffentlichung.** AffiliateScraper ist nicht quelloffen, deshalb gibt es hier keinen Code, nur was es kann, wie es gebaut ist und wie es aussieht. Wenn du darüber sprechen möchtest, melde dich über mein [GitHub-Profil](https://github.com/frommmmmg).

**Ein Radar für lohnende Partnerprogramme.** Es findet die Self-Service-Programme, die unabhängige SaaS- und KI-Unternehmen auf Plattformen wie Tolt, Rewardful, PromoteKit, FirstPromoter und PartnerStack betreiben, statt der großen geschlossenen Marktplätze.

Die bestzahlenden Programme sind selten in einem Marktplatz. Sie liegen auf der eigenen Anmeldeseite des Unternehmens, und jede Hosting-Plattform hinterlässt in URLs und Formulierungen einen erkennbaren Fußabdruck. AffiliateScraper macht aus diesen Fußabdrücken Suchregeln und erledigt dann den langweiligen Teil: Es liest, was es findet, extrahiert die Provisionsbedingungen, bewertet jedes Programm und speichert alles so, dass ein Mensch es filtern, exportieren und prüfen kann.

| | |
|---|---|
| **Meine Rolle** | Von einer Person entworfen und gebaut, als Entdeckungsstufe der AffProof-Datenpipeline |
| **Status** | Im täglichen Einsatz |
| **Ausgabe** | CSV-, JSON- und Markdown-Exporte sowie eine Keyword-Ebene, um zu entscheiden, was man schreibt |
| **Technik** | Python · SQLite · Pydantic · Such-APIs (DuckDuckGo, Google CSE, Serper) |

### Was es kann

**Entdeckung**
- **Suche per Dorks.** Eine gepflegte Bibliothek von Suchregeln, eine Familie pro Hosting-Plattform, mit Ausschlusslisten, die Blogs und Bewertungsseiten fernhalten. Die Suchen laufen über DuckDuckGo, Google CSE oder Serper, die Proxy-Einstellungen sind konfigurierbar.
- **Auf die richtigen Programme gezielt.** Gesucht werden wiederkehrende Provisionen von 30 % bis 50 %, sofortige Freischaltung und ein öffentlicher Anmeldelink, keine Einmalzahlungen.

**Verstehen**
- **Strukturierte Auswertung.** Markenname, Provisionssatz, wiederkehrend oder einmalig, Cookie-Dauer, Auszahlungsschwelle, Freigabeart und Kategorie werden mit Pydantic-Modellen extrahiert und validiert.
- **Eine einfache Note.** Stufen S, A und B, wobei S eine wiederkehrende Provision von mindestens 30 % mit starkem Konversionspotenzial bedeutet.

**Speicherung und Ausgabe**
- **Saubere Speicherung und Export.** SQLite mit Deduplizierung und Unique-Constraints auf der Anmelde-URL, Export nach CSV, JSON und Markdown, damit dieselben Daten in einer Tabelle, einem Frontend oder einer Notiz geöffnet werden können.

**Eine Keyword-Ebene**
- **Von „wer zahlt mir“ zu „was schreibe ich“.** Die KI beurteilt die Suchabsicht ohne kostenpflichtige SEO-Tools und sortiert Keywords in vier Stufen, von Menschen kurz vor dem Kauf bis zu bloß Neugierigen. Felder für Volumen, Wettbewerb und Gebot sind für echte Keyword-Planner-Daten reserviert, denn das Gebot eines Werbetreibenden beweist, dass die Nachfrage real ist.

## Screenshots

![Die mitgelieferten Beispielprogramme auf der Kommandozeile (öffentliche Beispieldaten).](assets/cli-list.png)
*Die mitgelieferten Beispielprogramme auf der Kommandozeile (öffentliche Beispieldaten).*

## So funktioniert es

![Von der Suchanfrage zur sortierten, deduplizierten Programmliste.](assets/affiliatescraper-pipeline.svg)
*Von der Suchanfrage zur sortierten, deduplizierten Programmliste.*

<!--notes-->
## Technische Notizen

- **Bewusst schlichte Technik.** Python, SQLite und Pydantic, ohne kostenpflichtiges SEO-Werkzeug im Ablauf, es läuft also auf einem Laptop, und die Daten liegen in einer Datei.
- **Ein Schritt nach dem anderen.** Jeder Befehl erledigt eine Aufgabe und hält an. Nichts reiht sich von selbst in den nächsten Schritt ein, so bleibt ein Mensch Herr darüber, was in die Datenbank gelangt.
- **Eine menschliche Prüfung für jeden Eintrag.** Die manuelle Routine hat drei Schritte: bestätigen, dass es eine echte unabhängige Anmeldeseite ist, sie nach den Provisionsbedingungen bewerten und die Anmeldung testen, ob die Freigabe sofort erfolgt.
- **Ausgabe, die andere Werkzeuge lesen können.** CSV für Tabellen, JSON für Frontends und Markdown für Notizen, geschrieben aus derselben Tabelle.
- **Gebaut, um etwas Größeres zu speisen.** Es ist die Entdeckungsstufe der AffProof-Pipeline, deren spätere Stufen Belege sammeln, das Prüfprofil schreiben, es prüfen, importieren und übersetzen.

<!--author-->
## Über den Autor

<img src="assets/wechat-qr.png" alt="QR-Code des WeChat-Offizialkontos Pin海引航" width="200" align="right">

**姜芊泽 (Jiang Qianze)** ist ein Pseudonym. Ich bin unabhängiger Entwickler und baue Werkzeuge, Daten und Automatisierung für Marken, Händler und Creator, die ins Ausland expandieren. Jedes Projekt in diesen Vorstellungen habe ich allein entworfen, gebaut und betrieben, von der Produktidee bis zu Servern und Dokumentation.

Über diese Arbeit schreibe ich in meinem WeChat-Offizialkonto **Pin海引航** (auf Chinesisch). Scanne den Code, um ihm zu folgen, oder finde mich auf [GitHub](https://github.com/frommmmmg).

<br clear="right">
<!--/author-->

**Weitere Projekte:** [AffProof](https://github.com/frommmmmg/AffProof-showcase) · [Tonu.app](https://github.com/frommmmmg/Tonu.app-showcase) · [AutoPin-CS](https://github.com/frommmmmg/AutoPin-CS-showcase)

---

<div align="center">

<sub>Screenshots verwenden nur Beispiel- oder öffentliche Daten. © Alle Rechte vorbehalten. Beschreibungen dürfen mit Quellenangabe zitiert werden; die Software selbst darf nicht weitergegeben werden.</sub>

</div>
