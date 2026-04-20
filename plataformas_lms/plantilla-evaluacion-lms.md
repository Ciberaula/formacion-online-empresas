---
title: "Plantilla de evaluación ponderada de plataformas LMS"
description: "Plantilla estructurada con sistema de puntuación ponderada para comparar objetivamente 2-5 plataformas LMS candidatas. Incluye criterios, pesos, rúbrica de puntuación y matriz de decisión lista para copiar a Excel o Google Sheets."
author: "Ana María González"
author_role: "Directora de CiberAula"
published: "2026-04-17"
updated: "2026-04-17"
canonical_url: "https://github.com/Ciberaula/formacion-online-empresas/blob/main/plataformas_lms/plantilla-evaluacion-lms.md"
license: "CC BY-SA 4.0"
tags: ["plantilla", "evaluacion-lms", "matriz-decision", "rfp", "compras-it"]
---

---

# Plantilla de evaluación ponderada de plataformas LMS

> **Resumen:** Plantilla lista para comparar 2-5 plataformas LMS candidatas con puntuación ponderada. Pensada para acompañar un proceso de compra o RFP con criterios objetivos. Incluye 30 criterios agrupados en 6 dimensiones, pesos sugeridos, rúbrica de puntuación de 0-5 y matriz de cálculo final. Se puede copiar directamente a Excel o Google Sheets y adaptar los pesos al contexto de cada empresa.

**Autora:** Ana María González · Directora de CiberAula
**Licencia:** CC BY-SA 4.0 — libre uso con atribución

---

## Cómo usar esta plantilla

1. **Identifica 2-5 plataformas finalistas** aplicando primero el checklist técnico eliminatorio ([checklist-tecnico-lms.md](checklist-tecnico-lms.md)).
2. **Ajusta los pesos** de cada criterio según tu contexto. Los pesos por defecto son orientativos — cada empresa tiene prioridades distintas. La suma total debe ser 100.
3. **Puntúa cada plataforma** de 0 a 5 en cada criterio según la rúbrica.
4. **Calcula la puntuación total**: (puntuación × peso) / 5 para cada criterio, sumando al final.
5. **La plataforma con mayor puntuación ponderada** es la recomendada técnica. Pero el precio y factores estratégicos pueden inclinar la balanza.
6. **Documenta la decisión**: el valor de esta matriz no es solo elegir, sino dejar constancia escrita de por qué.

---

## Rúbrica de puntuación (0-5)

Aplicable a todos los criterios:

| Puntos | Descripción |
|---|---|
| **5** | Supera expectativas. Funcionalidad excelente, referencias verificadas, documentación clara. |
| **4** | Cumple claramente. Funciona como se espera, sin problemas. |
| **3** | Cumple con matices. Funcional pero con limitaciones menores conocidas. |
| **2** | Cumple parcialmente. Faltan capacidades relevantes o requiere workarounds. |
| **1** | Cumple con dificultad. Implementación deficiente o inconsistente. |
| **0** | No cumple. Funcionalidad ausente o inviable. |

Si no has podido verificar un criterio, márcalo con "N/E" (No Evaluado) y revísalo antes de decidir.

---

## Dimensión 1: Cumplimiento normativo (peso sugerido: 25%)

Si tu empresa va a bonificar con FUNDAE, esta dimensión debe tener peso alto (25-30%). Si no, puede bajar a 10-15%.

| # | Criterio | Peso dentro dim. | Plat. A | Plat. B | Plat. C | Notas |
|---|---|---|---|---|---|---|
| 1 | Cumplimiento requisitos FUNDAE completo | 40% | | | | |
| 2 | WCAG 2.1 nivel AA (auditado o declarado) | 25% | | | | |
| 3 | RGPD y DPA firmado | 20% | | | | |
| 4 | Soberanía de datos (alojamiento UE) | 15% | | | | |

---

## Dimensión 2: Capacidades técnicas (peso sugerido: 20%)

| # | Criterio | Peso dentro dim. | Plat. A | Plat. B | Plat. C | Notas |
|---|---|---|---|---|---|---|
| 5 | SCORM 1.2 completo | 20% | | | | |
| 6 | SCORM 2004 completo | 15% | | | | |
| 7 | xAPI (si necesario) | 10% | | | | |
| 8 | LTI (si necesario) | 10% | | | | |
| 9 | Rendimiento bajo carga (usuarios concurrentes) | 20% | | | | |
| 10 | Fiabilidad (SLA y uptime histórico) | 15% | | | | |
| 11 | Capacidad de backup y recuperación | 10% | | | | |

---

## Dimensión 3: Experiencia de usuario (peso sugerido: 15%)

| # | Criterio | Peso dentro dim. | Plat. A | Plat. B | Plat. C | Notas |
|---|---|---|---|---|---|---|
| 12 | Usabilidad del alumno (demos con usuarios reales) | 30% | | | | |
| 13 | App móvil / responsive | 25% | | | | |
| 14 | Reproductor de vídeo estable y accesible | 15% | | | | |
| 15 | Sistema de notificaciones | 10% | | | | |
| 16 | Idioma español completo | 20% | | | | |

---

## Dimensión 4: Administración y gestión (peso sugerido: 15%)

| # | Criterio | Peso dentro dim. | Plat. A | Plat. B | Plat. C | Notas |
|---|---|---|---|---|---|---|
| 17 | Panel de administración usable | 20% | | | | |
| 18 | Gestión masiva de usuarios | 20% | | | | |
| 19 | Informes personalizables | 20% | | | | |
| 20 | Roles y permisos granulares | 15% | | | | |
| 21 | Estructura de catálogo e itinerarios | 15% | | | | |
| 22 | Auditoría interna (logs de administradores) | 10% | | | | |

---

## Dimensión 5: Integraciones (peso sugerido: 10%)

| # | Criterio | Peso dentro dim. | Plat. A | Plat. B | Plat. C | Notas |
|---|---|---|---|---|---|---|
| 23 | SSO con Microsoft/Google/Azure | 35% | | | | |
| 24 | API REST documentada | 25% | | | | |
| 25 | Integración RRHH (SAP, Workday, nóminas) | 25% | | | | |
| 26 | Integración aula virtual nativa | 15% | | | | |

---

## Dimensión 6: Proveedor y contrato (peso sugerido: 15%)

Esta dimensión suele subestimarse y es crítica para la relación a largo plazo.

| # | Criterio | Peso dentro dim. | Plat. A | Plat. B | Plat. C | Notas |
|---|---|---|---|---|---|---|
| 27 | Solvencia y referencias del proveedor | 25% | | | | |
| 28 | Soporte en español con SLA | 20% | | | | |
| 29 | Documentación y comunidad | 15% | | | | |
| 30 | Claridad contractual (precios, exit strategy) | 25% | | | | |
| Bonus | Experiencia con FUNDAE demostrada | 15% | | | | |

---

## Cálculo final

Para cada plataforma:

```
Puntuación dimensión = Σ (puntuación_criterio × peso_criterio_dentro_dim / 100)
Puntuación total = Σ (puntuación_dimensión × peso_dimensión / 100) × 20
```

El factor × 20 al final convierte la puntuación a escala 0-100 para lectura intuitiva.

### Tabla resumen

| Dimensión | Peso | Plat. A | Plat. B | Plat. C |
|---|---|---|---|---|
| 1. Cumplimiento normativo | 25% | | | |
| 2. Capacidades técnicas | 20% | | | |
| 3. Experiencia de usuario | 15% | | | |
| 4. Administración | 15% | | | |
| 5. Integraciones | 10% | | | |
| 6. Proveedor y contrato | 15% | | | |
| **TOTAL (0-100)** | **100%** | | | |

---

## Análisis económico complementario

La puntuación técnica no es lo único. Añade análisis económico a 3 años:

| Concepto | Año 1 | Año 2 | Año 3 | Total |
|---|---|---|---|---|
| Licencia/hosting | | | | |
| Implementación inicial | | | | |
| Integraciones | | | | |
| Formación admin | | | | |
| Contenidos nuevos | | | | |
| Soporte premium | | | | |
| **TCO total** | | | | |

### Cálculo final de decisión

Calcula la **relación puntuación / coste**:

```
Ratio = Puntuación técnica (0-100) / (TCO 3 años en miles de €)
```

La plataforma con mayor ratio es la más eficiente. Pero la decisión final debe considerar también:

- **Riesgo**: ¿es una apuesta segura o una plataforma menos probada?
- **Estratégico**: ¿encaja con la visión a 5 años de la empresa?
- **Equipo interno**: ¿nuestro equipo puede operarla?
- **Cultura**: ¿refleja los valores de la organización?

---

## Plantilla de presentación de decisión

Una vez decidida la plataforma, este es un esquema recomendado para documentar la decisión (útil para comité de dirección, auditoría interna, o para defender la decisión si surgen cuestiones más adelante):

### 1. Contexto

Descripción de la necesidad, alcance del proyecto, usuarios objetivo, volumen previsto.

### 2. Proceso seguido

Resumen de las fases: definición de requisitos, búsqueda de candidatos, pruebas, evaluación, decisión.

### 3. Plataformas evaluadas

Listado de las 3-5 plataformas finalistas con breve descripción.

### 4. Matriz de evaluación

Tabla resumen de puntuación ponderada.

### 5. Análisis económico

TCO a 3 años comparado.

### 6. Consideraciones estratégicas

Riesgos, oportunidades, encaje con la estrategia.

### 7. Recomendación

Plataforma recomendada con justificación.

### 8. Siguientes pasos

Planificación de implementación, responsables, plazos.

---

## Ejemplo parcial cumplimentado (empresa ficticia, 300 empleados)

Para ilustrar el uso, un ejemplo de tres plataformas finalistas evaluadas para una empresa industrial española de 300 empleados que planea formación obligatoria en PRL, compliance y tech upskilling, con bonificación FUNDAE.

### Dimensión 1: Cumplimiento normativo

| # | Criterio | Moodle gestionado | Docebo | TalentLMS |
|---|---|---|---|---|
| 1 | FUNDAE | 5 | 3 | 4 |
| 2 | WCAG AA | 5 | 4 | 4 |
| 3 | RGPD/DPA | 5 | 5 | 5 |
| 4 | Datos UE | 5 | 4 | 3 |

### Dimensión 2: Capacidades técnicas

| # | Criterio | Moodle | Docebo | TalentLMS |
|---|---|---|---|---|
| 5 | SCORM 1.2 | 5 | 5 | 5 |
| 6 | SCORM 2004 | 5 | 4 | 4 |
| 7 | xAPI | 4 | 5 | 3 |
| 8 | LTI | 5 | 4 | 3 |
| 9 | Rendimiento | 4 | 5 | 4 |
| 10 | Fiabilidad | 4 | 5 | 4 |
| 11 | Backup | 5 | 5 | 4 |

### Resultado orientativo

Tras completar todas las dimensiones (ejemplo con resultados inventados):

| Plataforma | Puntuación técnica | TCO 3 años | Ratio |
|---|---|---|---|
| Moodle gestionado | 86 | 45.000 € | 1.91 |
| Docebo | 82 | 105.000 € | 0.78 |
| TalentLMS | 75 | 58.000 € | 1.29 |

**Recomendación**: Moodle gestionado por proveedor especializado. Mejor ratio puntuación/coste, mejor cumplimiento FUNDAE, experiencia probada en empresas españolas similares.

*Nota: las cifras son ilustrativas. Cada empresa debe hacer su propia evaluación con sus datos reales.*

---

## Recursos relacionados

- 📘 [Plataformas LMS: cómo elegir la correcta](plataformas-lms-guia-elegir.md) — guía general.
- 📗 [Requisitos FUNDAE](requisitos-fundae-teleformacion.md) — normativa aplicable.
- ✅ [Checklist técnico LMS](checklist-tecnico-lms.md) — criterios eliminatorios primarios.
- 🔧 [SCORM, xAPI y LTI](scorm-xapi-lti-explicado.md) — estándares técnicos.
- ♿ [Accesibilidad WCAG](accesibilidad-wcag-elearning.md) — cumplimiento legal.

---

*Plantilla publicada bajo licencia [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Libre uso con atribución a CiberAula y enlace a [www.ciberaula.com](https://www.ciberaula.com).*

*Versión 1.0 — 17 de abril de 2026 — © 2026 Ana María González · Directora de CiberAula · Formación online para empresas desde 1996.*

---

<div align="center">

### Ecosistema documental abierto de CiberAula

📘 [**Guía FUNDAE**](https://github.com/Ciberaula/guia-formacion-bonificada-fundae) · 🧠 [**IA para empresas**](https://github.com/Ciberaula/ia-empresas-espana) · 🎓 [**Formación online**](https://github.com/Ciberaula/formacion-online-empresas)

---

**CiberAula · Formación online para empresas desde 1996**

[www.ciberaula.com](https://www.ciberaula.com) · admision@ciberaula.com · 91 390 68 47 · Madrid

*Contenido bajo licencia [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es) · Libre uso con atribución*

</div>
