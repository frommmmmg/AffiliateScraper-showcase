<div align="center">

# AffiliateScraper

[English](README.md) · [中文](README.zh.md) · [Español](README.es.md) · [Deutsch](README.de.md) · Français

</div>

> **Ce dépôt est une vitrine, pas une publication de code source.** AffiliateScraper est un projet privé : il n'y a donc pas de code ici, seulement ce qu'il fait, comment il est construit et à quoi il ressemble. Pour en discuter, contactez-moi via mon [profil GitHub](https://github.com/frommmmmg).

**Un radar des programmes d'affiliation qui valent la peine.** Il vise les programmes à commission récurrente d'entreprises SaaS et IA indépendantes, sur des plateformes comme Tolt, Rewardful, PromoteKit, FirstPromoter et PartnerStack, plutôt que les grandes places de marché fermées.

**Points forts**

- **Découverte par dorks.** Une bibliothèque de règles entretenue et des listes d'exclusion, exécutées via DuckDuckGo, Google CSE ou Serper.
- **Analyse structurée.** Marque, taux de commission, récurrent ou ponctuel et catégorie sont extraits et validés par des modèles Pydantic.
- **Stockage et export propres.** SQLite avec déduplication et contraintes d'unicité, export en CSV, JSON et Markdown.
- **Une couche de mots-clés assistée par IA.** Transforme la liste de produits en pages à écrire, avec des niveaux d'intention de recherche et sans outil SEO payant.
- **CLI en une ligne** pour charger, lister, rechercher, exporter et générer des mots-clés.

Il alimente aussi le pipeline de diligence d'AffProof.

**Technologies :** Python · SQLite · Pydantic · API de recherche

## Captures d'écran

![Liste des programmes d'exemple en ligne de commande (données d'exemple publiques).](assets/cli-list.png)
*Liste des programmes d'exemple en ligne de commande (données d'exemple publiques).*

## Comment ça marche

![De la requête de recherche à une liste de programmes classée et dédoublonnée.](assets/affiliatescraper-pipeline.svg)
*De la requête de recherche à une liste de programmes classée et dédoublonnée.*

---

<div align="center">

<sub>Les captures n'utilisent que des données d'exemple ou publiques. © Tous droits réservés. Les descriptions peuvent être citées avec attribution ; le logiciel lui-même ne peut pas être redistribué.</sub>

</div>
