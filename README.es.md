<div align="center">

# AffiliateScraper

[English](README.md) · [中文](README.zh.md) · Español · [Deutsch](README.de.md) · [Français](README.fr.md)

🌐 Feeds **[affproof.com](https://affproof.com)** · [GitHub @frommmmmg](https://github.com/frommmmmg)

</div>

> **Este repositorio es un escaparate, no una publicación de código.** AffiliateScraper no es de código abierto, así que aquí no hay código: solo qué hace, cómo está construido y qué aspecto tiene. Si quieres hablar de él, escríbeme desde mi [perfil de GitHub](https://github.com/frommmmmg).

**Un radar de programas de afiliados que merecen la pena.** Encuentra los programas de autoservicio que empresas independientes de SaaS e IA alojan en plataformas como Tolt, Rewardful, PromoteKit, FirstPromoter y PartnerStack, en lugar de los grandes mercados cerrados.

Los programas que mejor pagan rara vez están en un mercado. Están en la página de registro de la propia empresa, y cada plataforma de alojamiento deja una huella reconocible en sus URL y su redacción. AffiliateScraper convierte esas huellas en reglas de búsqueda y luego hace la parte aburrida: lee lo que encuentra, extrae las condiciones de comisión, califica cada programa y lo guarda todo de forma que una persona pueda filtrarlo, exportarlo y revisarlo.

| | |
|---|---|
| **Mi papel** | Diseñado y construido por una persona, como la etapa de descubrimiento de la canalización de datos de AffProof |
| **Estado** | En uso diario |
| **Salida** | Exportaciones CSV, JSON y Markdown, más una capa de palabras clave para decidir qué escribir |
| **Tecnología** | Python · SQLite · Pydantic · APIs de búsqueda (DuckDuckGo, Google CSE, Serper) |

### Qué hace

**Descubrimiento**
- **Búsqueda con dorks.** Una biblioteca mantenida de reglas de búsqueda, una familia por plataforma de alojamiento, con listas de exclusión para dejar fuera blogs y sitios de reseñas. Las búsquedas se ejecutan con DuckDuckGo, Google CSE o Serper, y la configuración del proxy es ajustable.
- **Dirigido a los programas adecuados.** Busca comisiones recurrentes del 30% al 50%, aprobación instantánea y un enlace de registro público, no pagos únicos.

**Comprensión**
- **Análisis estructurado.** Marca, porcentaje de comisión, recurrente o puntual, duración de la cookie, umbral de pago, tipo de aprobación y categoría se extraen y validan con modelos Pydantic.
- **Una calificación simple.** Niveles S, A y B, donde S significa una comisión recurrente del 30% o más con gran potencial de conversión.

**Almacenamiento y salida**
- **Almacenamiento y exportación limpios.** SQLite con deduplicación y restricciones únicas sobre la URL de registro, exportado a CSV, JSON y Markdown para que los mismos datos se abran en una hoja de cálculo, un front end o una nota.

**Una capa de palabras clave**
- **De "quién me paga" a "qué escribo".** La IA juzga la intención de búsqueda sin herramientas SEO de pago y ordena las palabras clave en cuatro niveles, desde quien está a punto de comprar hasta quien solo siente curiosidad. Los campos de volumen, competencia y puja están reservados para datos reales de Keyword Planner, porque la puja de un anunciante demuestra que la demanda es real.

## Capturas

![Listado de los programas de ejemplo desde la línea de comandos (datos de muestra públicos).](assets/cli-list.png)
*Listado de los programas de ejemplo desde la línea de comandos (datos de muestra públicos).*

## Cómo funciona

![De una consulta de búsqueda a una lista de programas ordenada y sin duplicados.](assets/affiliatescraper-pipeline.svg)
*De una consulta de búsqueda a una lista de programas ordenada y sin duplicados.*

<!--notes-->
## Notas de ingeniería

- **Una tecnología deliberadamente sencilla.** Python, SQLite y Pydantic, sin ninguna herramienta SEO de pago en el circuito, así que funciona en un portátil y los datos quedan en un solo archivo.
- **Un paso cada vez.** Cada comando hace una tarea y se detiene. Nada encadena solo el siguiente paso, lo que mantiene a una persona al mando de lo que entra en la base de datos.
- **Una revisión humana de cada entrada.** La rutina manual tiene tres pasos: confirmar que es una página de registro independiente real, calificarla por sus condiciones de comisión y probar el registro para ver si la aprobación es instantánea.
- **Salida que otras herramientas pueden leer.** CSV para hojas de cálculo, JSON para front ends y Markdown para notas, escritos desde la misma tabla.
- **Construido para alimentar algo mayor.** Es la etapa de descubrimiento de la canalización de AffProof, cuyas etapas posteriores recogen evidencias, redactan el expediente, lo someten a control, lo importan y lo traducen.

**Otras muestras:** [AffProof](https://github.com/frommmmmg/AffProof-showcase) · [Tonu.app](https://github.com/frommmmmg/Tonu.app-showcase) · [AutoPin-CS](https://github.com/frommmmmg/AutoPin-CS-showcase)

---

<div align="center">

<sub>Las capturas usan solo datos de ejemplo o públicos. © Todos los derechos reservados. Las descripciones pueden citarse con atribución; el software no se puede redistribuir.</sub>

</div>
