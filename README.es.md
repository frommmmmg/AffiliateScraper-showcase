<div align="center">

# AffiliateScraper

[English](README.md) · [中文](README.zh.md) · Español · [Deutsch](README.de.md) · [Français](README.fr.md)

</div>

> **Este repositorio es un escaparate, no una publicación de código.** AffiliateScraper es un proyecto privado, así que aquí no hay código: solo qué hace, cómo está construido y qué aspecto tiene. Si quieres hablar de él, escríbeme desde mi [perfil de GitHub](https://github.com/frommmmmg).

**Un radar de programas de afiliados que merecen la pena.** Apunta a los programas de comisión recurrente de empresas independientes de SaaS e IA en plataformas como Tolt, Rewardful, PromoteKit, FirstPromoter y PartnerStack, en lugar de los grandes mercados cerrados.

**Puntos clave**

- **Descubrimiento con dorks.** Una biblioteca de reglas mantenida y listas de exclusión, ejecutadas con DuckDuckGo, Google CSE o Serper.
- **Análisis estructurado.** Marca, porcentaje de comisión, recurrente o puntual y categoría se extraen y validan con modelos Pydantic.
- **Almacenamiento y exportación limpios.** SQLite con deduplicación y restricciones únicas, exportado a CSV, JSON y Markdown.
- **Una capa de palabras clave con IA.** Convierte la lista de productos en las páginas que vale la pena escribir, con niveles de intención de búsqueda y sin herramientas SEO de pago.
- **CLI de una línea** para cargar, listar, buscar, exportar y generar palabras clave.

También alimenta el pipeline de diligencia debida de AffProof.

**Tecnología:** Python · SQLite · Pydantic · APIs de búsqueda

## Capturas

![Listado de los programas de ejemplo desde la línea de comandos (datos de muestra públicos).](assets/cli-list.png)
*Listado de los programas de ejemplo desde la línea de comandos (datos de muestra públicos).*

## Cómo funciona

![De una consulta de búsqueda a una lista de programas ordenada y sin duplicados.](assets/affiliatescraper-pipeline.svg)
*De una consulta de búsqueda a una lista de programas ordenada y sin duplicados.*

---

<div align="center">

<sub>Las capturas usan solo datos de ejemplo o públicos. © Todos los derechos reservados. Las descripciones pueden citarse con atribución; el software no se puede redistribuir.</sub>

</div>
