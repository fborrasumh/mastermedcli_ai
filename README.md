# Laboratorio IA · Máster Universitario en Investigación en Medicina Clínica (UMH) — 13 tutores metodológicos

Suite de 12 simuladores metodológicos con IA + 1 **TFM·Coach** para el **Máster Universitario en Investigación en Medicina Clínica** de la UMH (tit_m_193), alineados con las asignaturas del plan de estudios oficial (60 ECTS, modalidad online).

## ⚠ Aviso de uso responsable y docente

Estas herramientas son **simuladores formativos** de metodología de la investigación. **No sustituyen la formación reglada, la supervisión del tutor/a de TFM ni el dictamen de un comité de ética de la investigación (CEIm).** Ningún diseño, análisis o texto generado por la IA debe usarse en investigación real sin verificación. Contrasta siempre con las guías vigentes (CONSORT, STROBE, PRISMA, SPIRIT, GRADE, Declaración de Helsinki, ICH-GCP) y con tu equipo investigador.

## Arquitectura (kernel compartido)

- Single-file HTML + JavaScript vanilla, sin frameworks ni backend.
- Modelo `gpt-4o-mini` vía API de OpenAI; clave en `localStorage` (`ia_openai_key`), compartida entre todas las apps del mismo dominio.
- Flujo en 3 fases: **Caso metodológico generado por IA → Simulación en rol (tutor / editor / monitor / metodólogo) → Evaluación con rúbrica (JSON estructurado)**.
- Historial de sesiones en **IndexedDB** (una base por app: `medurg_umh_<id>`).
- Exportación de informe: **Markdown**, **.docx** (docx.js con carga perezosa desde CDN) e impresión/PDF del navegador.
- Idéntico kernel que la suite de Medicina de Urgencias-Emergencias, reutilizado y reorientado hacia investigación clínica.

## Catálogo por asignatura

### Obligatorias (7,5 ECTS) — 1er semestre
| Asignatura | App |
|---|---|
| Metodología de la Investigación I | MetodoLab·I·AI |
| Metodología de la Investigación II | MetodoLab·II·AI |
| Documentación Científica Avanzada y Elaboración Práctica de un Proyecto de Investigación | DocScience·AI |
| Aplicación de la Evidencia Científica en Medicina | EvidencIA·AI |

### Optativas (4,5 ECTS) — 2º semestre
| Asignatura | App |
|---|---|
| Escritura y Publicación de un Artículo Científico | Manuscript·AI |
| Técnicas de Comunicación y Herramientas Web en Investigación | SciComm·AI |
| Ensayos Clínicos en Investigación Clínica | TrialLab·AI |
| Metodología de la Investigación Cualitativa en Ciencia de la Salud | QualiLab·AI |

### Optativas (3 ECTS) — 2º semestre
| Asignatura | App |
|---|---|
| Técnica «In vivo / In vitro» en la Investigación Clínica | BioTech·AI |
| Modelos de Inteligencia Artificial en Ciencias de la Salud | MedAI·Lab |
| Investigación en Gestión Clínica | GestClinLab·AI |
| Revisiones Sistemáticas y Metaanálisis | MetaLab·AI |

### Trabajo Fin de Máster
| Asignatura | App |
|---|---|
| Trabajo Fin de Máster | TFM·Coach·Clínica |

## Despliegue en GitHub Pages

1. Crea un repositorio (p. ej. `medclinica-umh-ia`).
2. Sube el contenido de esta carpeta `docs/`.
3. Settings → Pages → Source: rama `main`, carpeta `/docs`.
4. La URL será `https://<usuario>.github.io/medclinica-umh-ia/`.

## Uso propuesto en la evaluación continua

El estudiante realiza las sesiones marcadas por cada asignatura, exporta el informe con transcripción + rúbrica y lo entrega como evidencia. La nota de la rúbrica es orientativa: la calificación final la fija el profesorado.

## Fuente del plan de estudios

Máster Universitario en Investigación en Medicina Clínica (UMH), ficha oficial `tit_m_193` y web del máster `mastermedcli.umh.es`. El plan combina 4 obligatorias (30 ECTS), optativas de 4,5 y 3 ECTS hasta completar 12 ECTS, y el TFM (18 ECTS).
