---
title: "Accesibilidad WCAG aplicada a plataformas de elearning"
description: "Cumplimiento de la Ley 11/2023 de Accesibilidad aplicada a plataformas LMS y contenido formativo en empresas españolas. Qué exige WCAG 2.1 nivel AA, obligaciones desde junio 2025, cómo auditar tu plataforma y checklist de contenido formativo accesible."
author: "Ana María González"
author_role: "Directora de CiberAula"
published: "2026-04-17"
updated: "2026-04-17"
canonical_url: "https://github.com/Ciberaula/formacion-online-empresas/blob/main/plataformas_lms/accesibilidad-wcag-elearning.md"
license: "CC BY-SA 4.0"
tags: ["wcag", "accesibilidad", "ley-accesibilidad", "lms", "elearning", "cumplimiento"]
---

---

# Accesibilidad WCAG aplicada a plataformas de elearning

> **Resumen en 3 frases:** Desde el 28 de junio de 2025, la Ley 11/2023 de Accesibilidad (transposición del Acta Europea de Accesibilidad, Directiva 2019/882) exige que las plataformas de elearning comercializadas o utilizadas en España cumplan el nivel AA de WCAG 2.1 o superior. Esta obligación afecta tanto a la plataforma LMS como al contenido formativo que se imparte: vídeos sin subtítulos, documentos PDF no accesibles o navegación que no funcione con teclado son incumplimientos sancionables. Esta guía explica qué exige WCAG en el contexto concreto de elearning corporativo, cómo auditar tu plataforma y tu contenido, y los errores más frecuentes que se cometen al producir cursos online.

**Última actualización:** 17 de abril de 2026
**Autora:** Ana María González · Directora de CiberAula
**Tiempo estimado de lectura:** 10 minutos
**Licencia:** CC BY-SA 4.0

---

## Índice

1. [Marco legal en España desde 2025](#marco-legal)
2. [Qué es WCAG y qué niveles hay](#que-es-wcag)
3. [Los 4 principios de WCAG aplicados a elearning](#principios)
4. [Requisitos específicos para plataformas LMS](#lms)
5. [Requisitos específicos para contenido formativo](#contenido)
6. [Cómo auditar tu plataforma](#auditoria)
7. [Errores frecuentes en elearning accesible](#errores)
8. [Preguntas frecuentes](#faq)

---

## <a id="marco-legal"></a>1. Marco legal en España desde 2025

### Textos normativos aplicables

**Ley 11/2023**, de 8 de mayo, de trasposición de directivas de la UE en materia de accesibilidad de determinados productos y servicios. Transpone la **Directiva (UE) 2019/882** (Acta Europea de Accesibilidad, EAA).

**Real Decreto 193/2023**, de 21 de marzo, por el que se regulan las condiciones básicas de accesibilidad y no discriminación de las personas con discapacidad para el acceso y utilización de bienes y servicios a disposición del público.

**Real Decreto 1112/2018**, sobre accesibilidad de sitios web y aplicaciones móviles del sector público (aplicable también a servicios asimilados).

### Qué afecta al elearning

Desde el **28 de junio de 2025**, estos requisitos son exigibles en España para:

- **Plataformas LMS** comercializadas o utilizadas para prestar servicios de elearning.
- **Contenido formativo** puesto a disposición de los alumnos.
- **Aplicaciones móviles** de plataformas de aprendizaje.
- **Documentos electrónicos** (PDFs, presentaciones) distribuidos como parte de la formación.

### A quién aplica

La obligación recae fundamentalmente en:

- **Proveedores de LMS** que comercializan su plataforma en España.
- **Entidades organizadoras de formación** que utilizan plataformas LMS para impartir formación.
- **Empresas** que ofrecen formación a sus empleados cuando la relación implica prestación de servicio.

Aunque la ley establece algunas excepciones para microempresas, en el contexto empresarial español y especialmente si usas formación bonificada FUNDAE, **hay que cumplirla**. FUNDAE ha incorporado la accesibilidad como requisito de las plataformas de teleformación.

### Régimen sancionador

Las infracciones graves pueden suponer sanciones de hasta **600.000 €** según la Ley General de derechos de las personas con discapacidad (RDL 1/2013). Además, el incumplimiento puede suponer la no aceptación de expedientes en formación bonificada.

---

## <a id="que-es-wcag"></a>2. Qué es WCAG y qué niveles hay

**WCAG (Web Content Accessibility Guidelines)** es el estándar internacional de accesibilidad web publicado por el **W3C** (World Wide Web Consortium). Es el referente técnico universal al que remite toda la legislación europea y española sobre accesibilidad digital.

### Versiones vigentes

- **WCAG 2.1** (2018): versión más implantada. La que exige la legislación española actual.
- **WCAG 2.2** (2023): versión más reciente, con nueve criterios nuevos. Aún no es obligatoria pero recomendable.
- **WCAG 3.0**: en desarrollo, sin fecha de aplicación obligatoria.

### Niveles de conformidad

Cada criterio WCAG se clasifica en uno de tres niveles:

- **Nivel A**: el mínimo imprescindible. Requisitos básicos sin los cuales el contenido es inaccesible para grandes colectivos.
- **Nivel AA**: nivel de conformidad exigido por la mayoría de legislaciones europeas, incluida la española. Es el estándar al que debe apuntar una plataforma de elearning corporativa.
- **Nivel AAA**: nivel óptimo, no siempre alcanzable en todo el contenido. Excepcional.

**En España, para elearning, el nivel exigible es AA de WCAG 2.1**. Apuntar a AAA donde sea posible es buena práctica pero no obligatorio.

---

## <a id="principios"></a>3. Los 4 principios de WCAG aplicados a elearning

WCAG se organiza en cuatro principios fundamentales conocidos por el acrónimo **POUR**: Perceptible, Operable, Understandable, Robust. Aplicados al elearning:

### 3.1. Perceptible

La información y los elementos de la interfaz deben ser perceptibles para los usuarios, independientemente de sus capacidades sensoriales.

En elearning esto significa:

- **Alternativas textuales** para cualquier imagen, icono o elemento no textual (campo `alt` en HTML, descripción para imágenes complejas).
- **Subtítulos** en todos los vídeos, sincronizados con el audio.
- **Transcripción** completa disponible para contenido solo-audio (podcasts formativos).
- **Audiodescripción** en vídeos donde la imagen transmita información que no esté en el audio (poco frecuente en formación corporativa, pero exigible).
- **Contraste de colores suficiente**: ratio mínimo 4.5:1 para texto normal, 3:1 para texto grande.
- **No depender solo del color** para transmitir información (no hacer "las filas en rojo son errores" sin otro indicador).
- **Redimensionamiento del texto** sin pérdida de funcionalidad (hasta 200%).

### 3.2. Operable

Los componentes de la interfaz y la navegación deben ser operables con distintos métodos de interacción.

En elearning esto significa:

- **Navegación completa por teclado**: el alumno debe poder hacer todo sin ratón (tabular entre elementos, activarlos con Enter, navegar menús con flechas).
- **Sin trampas de teclado** (puntos donde el foco no puede salir).
- **Tiempo ajustable**: si hay exámenes con límite de tiempo, debe poder extenderse para usuarios que lo necesiten.
- **No contenido parpadeante** que pueda provocar ataques epilépticos (frecuencia entre 3 y 55 Hz).
- **Orden lógico de navegación** (tabular en el orden visual de los elementos).
- **Enlaces descriptivos** (no "haz clic aquí", sino "descargar guía de seguridad").

### 3.3. Understandable

El contenido y el funcionamiento de la interfaz deben ser comprensibles.

En elearning esto significa:

- **Idioma declarado** en HTML (atributo `lang="es"`).
- **Texto legible**: frases cortas, lenguaje sencillo (especialmente importante en cursos de cumplimiento donde a veces se abusa del lenguaje técnico).
- **Consistencia**: los mismos elementos deben funcionar igual en todas las páginas del curso.
- **Instrucciones claras**: cada formulario, test o tarea debe explicar exactamente qué hay que hacer.
- **Mensajes de error comprensibles** cuando el alumno se equivoca (no solo "error 42", sino "la respuesta debe ser un número entre 1 y 10").
- **Evitar jerga innecesaria**: especialmente en el interfaz de la plataforma. Si necesitas tecnicismos del tema del curso, explícalos la primera vez que aparecen.

### 3.4. Robust

El contenido debe ser lo suficientemente robusto para ser interpretado de forma fiable por una amplia variedad de agentes de usuario, incluyendo tecnologías de asistencia.

En elearning esto significa:

- **HTML bien formado**: sin errores de sintaxis que rompan la interpretación por lectores de pantalla.
- **Compatibilidad con lectores de pantalla**: JAWS, NVDA en Windows; VoiceOver en Mac/iOS; TalkBack en Android.
- **Uso de etiquetas semánticas**: usar `<button>` para botones, `<h1>-<h6>` para jerarquía de títulos, etc., no solo `<div>` con CSS.
- **Atributos ARIA** cuando sea necesario para aclarar roles o estados.
- **Compatibilidad con navegadores y versiones** mínimamente actualizadas.

---

## <a id="lms"></a>4. Requisitos específicos para plataformas LMS

Además de los principios generales, una plataforma LMS corporativa debe cumplir estos requisitos específicos:

### 4.1. Navegación de la plataforma

- **Menú principal accesible por teclado** con estado de foco visible.
- **Migas de pan** (breadcrumbs) funcionales para saber dónde se está.
- **Sistema de búsqueda** accesible.
- **Saltar al contenido principal** (skip link) para evitar repetir la navegación en cada página.

### 4.2. Formularios

- **Etiquetas asociadas** a cada campo (con `<label>`).
- **Mensajes de error** descriptivos junto al campo que falla.
- **Indicación clara** de campos obligatorios, no solo con asterisco rojo.
- **Confirmación** de acciones importantes (entregar examen, cerrar sesión).

### 4.3. Reproductor de vídeo

- **Controles accesibles por teclado**: play, pause, volumen, subtítulos.
- **Subtítulos integrados** activables/desactivables.
- **Transcripción accesible** junto al vídeo.
- **Pausa automática en reproducción automática**: ningún vídeo se debe reproducir en auto-play sin posibilidad de pausarlo inmediatamente.

### 4.4. Evaluaciones

- **Preguntas legibles** por lectores de pantalla.
- **Tiempo ampliable** para quien lo necesite.
- **Feedback accesible** tras enviar cada respuesta.
- **No depender del arrastrar y soltar** sin alternativa teclado.

### 4.5. Documentos descargables

- **PDFs accesibles** (etiquetados, con texto seleccionable, estructura lógica).
- **Presentaciones** (PowerPoint) con estructura accesible.
- **Documentos Office** correctamente etiquetados.

### 4.6. Certificados

Los certificados que emite la plataforma deben ser PDFs accesibles, no imágenes con texto.

---

## <a id="contenido"></a>5. Requisitos específicos para contenido formativo

El contenido que cargas en el LMS debe ser también accesible. Esta es una responsabilidad de quien crea el contenido (a menudo externalizada), pero la empresa es responsable última ante una inspección.

### 5.1. Vídeos formativos

Obligatorio:

- **Subtítulos sincronizados** en español (o idioma del curso).
- **Transcripción** disponible además de los subtítulos.
- **Calidad de sonido** suficiente.

Muy recomendable:

- **Audiodescripción** si hay elementos visuales con información relevante que no se explicita en el audio.
- **Lengua de signos** en ciertos contextos (obligaciones específicas para sector público).

### 5.2. Presentaciones y documentos

- **PDFs** exportados con opción "Documento etiquetado" (la mayoría de generadores modernos lo ofrecen).
- **Imágenes** con texto alternativo descriptivo.
- **Tablas** con cabeceras marcadas.
- **Enlaces** con texto descriptivo.

### 5.3. Cursos SCORM/xAPI

Los paquetes SCORM deben generarse con herramientas de autor que soporten accesibilidad (Articulate Storyline, Rise, Adobe Captivate modernos lo soportan):

- **Orden de tabulación** lógico.
- **Etiquetas ARIA** correctas.
- **Alternativas textuales** para imágenes interactivas.
- **Controles accesibles** en animaciones y simulaciones.

### 5.4. Juegos serios y simulaciones

Son los más complejos. Deben ofrecer:

- **Modo accesible alternativo** si la versión interactiva no puede ser 100% accesible.
- **Tiempo ampliable** o pausas.
- **Instrucciones claras** antes de empezar.

---

## <a id="auditoria"></a>6. Cómo auditar tu plataforma

### Auditoría básica (30 minutos, sin coste)

**Prueba 1 — Solo teclado**. Intenta hacer un curso completo usando solo el teclado (Tab, Shift+Tab, Enter, Esc, flechas). Si en algún punto te atascas, hay un problema de accesibilidad.

**Prueba 2 — Lector de pantalla**. Activa NVDA (gratuito para Windows) o VoiceOver (integrado en Mac). Cierra los ojos (o ponte un antifaz) e intenta navegar por la plataforma solo con el lector. Evaluarás dos cosas: si los elementos se anuncian correctamente y si puedes avanzar sin ver la pantalla.

**Prueba 3 — Zoom al 200%**. Aumenta el zoom del navegador al 200%. Si el texto se corta, desaparece, o elementos quedan solapados, hay problemas de accesibilidad.

**Prueba 4 — Contraste**. Usa una extensión como "WCAG Color Contrast Checker" en tu navegador para verificar que los ratios de contraste son correctos.

**Prueba 5 — Subtítulos**. Intenta activar los subtítulos en tres vídeos aleatorios. Si no están o son de baja calidad, problema.

### Auditoría automática (1 hora, gratis o coste bajo)

Herramientas como:

- **WAVE** (gratuito) - extensión de navegador que marca errores en la página.
- **axe DevTools** (gratuito versión básica) - integrado en Chrome DevTools.
- **Lighthouse** (integrado en Chrome) - incluye auditoría de accesibilidad.

Estas herramientas detectan ~30% de los problemas. El resto requiere revisión manual.

### Auditoría profesional (coste significativo, recomendada)

Para empresas con volumen importante o en sectores regulados, contrata una auditoría profesional:

- Coste orientativo: 2.000-8.000 € según alcance.
- Duración: 2-4 semanas.
- Resultado: informe detallado con puntos de incumplimiento, priorización y recomendaciones.
- Algunas entidades especializadas en España: ILUNION, Fundación ONCE (servicios), consultoras especializadas en accesibilidad.

### Declaración de accesibilidad

Cualquier plataforma LMS en uso debería publicar una **declaración de accesibilidad** con:

- Estado de cumplimiento (totalmente conforme, parcialmente conforme, no conforme).
- Contenido no accesible con justificación.
- Mecanismo de reclamación.
- Fecha de última revisión.

Si tu proveedor de LMS no publica una, es una bandera roja importante.

---

## <a id="errores"></a>7. Errores frecuentes en elearning accesible

**Error 1: Pensar que accesibilidad = "para personas con discapacidad"**. La accesibilidad beneficia a muchos más perfiles: personas mayores, personas con conexiones lentas, personas en entornos ruidosos (que activan subtítulos), personas que consumen formación en móvil mientras hacen otras cosas.

**Error 2: Hacer vídeos sin subtítulos**. Es el error más común y más fácil de evitar. Herramientas como YouTube, Descript, Whisper, etc., pueden generar subtítulos automáticos con calidad suficiente. Solo hay que revisarlos y corregirlos.

**Error 3: PDFs escaneados**. Si el PDF es una imagen escaneada de un documento, un lector de pantalla no puede leer el texto. El documento debe estar OCR-izado (texto seleccionable) y etiquetado.

**Error 4: Gamificación basada solo en arrastrar y soltar**. Sin alternativa teclado, es inaccesible.

**Error 5: Colores rojo/verde para marcar acierto/error**. Inaccesible para personas con daltonismo. Usa siempre un segundo indicador (icono ✓ ✗, texto "correcto"/"incorrecto").

**Error 6: Diagramas complejos solo en imagen**. Un organigrama o un flujo de proceso complejo necesita descripción textual adicional.

**Error 7: Auto-play en vídeos**. Reproducir vídeo automáticamente al abrir una página es confuso para lectores de pantalla y molesto en general. No lo hagas.

**Error 8: Texto justificado**. El texto justificado (con espacios irregulares entre palabras) es más difícil de leer para personas con dislexia. Alinear a la izquierda.

**Error 9: No declarar el idioma**. Sin `lang="es"`, los lectores de pantalla pronuncian "Bienvenidos" como si fuera inglés.

**Error 10: Dejar la accesibilidad para el final**. Es mucho más caro y difícil accesibilizar un curso ya producido que producirlo accesible desde el inicio.

---

## <a id="faq"></a>8. Preguntas frecuentes

### ¿Mi empresa tiene que cumplir WCAG si solo forma internamente a sus empleados?

Sí. La obligación aplica también a la formación a trabajadores propios. Además, puedes tener empleados con discapacidades que necesiten la accesibilidad.

### ¿Y si usamos una plataforma externa (SaaS)?

La empresa contratante es corresponsable. Si tu proveedor de LMS no cumple, tú incumples. Por eso es crítico exigir en el contrato que cumple WCAG.

### ¿Cómo sé si mi LMS cumple?

Pide al proveedor:
1. Declaración de accesibilidad pública.
2. Informe de auditoría reciente (idealmente externa).
3. Plan de remediación si hay incumplimientos.

### ¿Los subtítulos automáticos de YouTube son suficientes?

Como punto de partida sí, pero siempre hay que revisar y corregir errores. YouTube auto-genera subtítulos pero tiene tasas de error del 10-20% en español, y en términos técnicos específicos del curso puede equivocarse mucho más.

### ¿Cuánto cuesta hacer un curso accesible desde el principio?

Un 15-25% más que un curso no accesible, aproximadamente. Hacerlo accesible a posteriori puede costar el doble que rehacerlo desde cero.

### ¿Existen cursos gratuitos sobre accesibilidad?

Sí. W3C ofrece cursos introductorios. Fundación ONCE tiene recursos en español. Google, Microsoft y IBM ofrecen cursos gratuitos sobre accesibilidad digital. Recomendable para equipos de contenido.

### ¿Qué diferencia hay entre WCAG 2.1 y 2.2?

WCAG 2.2 añade 9 criterios nuevos, principalmente relacionados con accesibilidad cognitiva y motora. Para elearning corporativo, si cumples 2.1 AA estás bien; 2.2 es recomendable pero no obligatorio (aún).

### ¿FUNDAE inspecciona específicamente la accesibilidad?

No específicamente, pero los requisitos técnicos que FUNDAE exige incluyen el cumplimiento WCAG. Una plataforma claramente inaccesible puede ser motivo de rechazo del expediente.

### ¿Y si tengo contenido antiguo no accesible?

Hay dos opciones: rehacerlo, o publicar una declaración de accesibilidad listando qué contenido no cumple y por qué. La segunda opción es admisible si hay justificación (coste desproporcionado de migrar, baja frecuencia de uso, planificación de sustitución).

### ¿Las personas con discapacidad son un grupo pequeño?

**No**. Según el INE, más del 10% de la población española tiene algún tipo de discapacidad (más de 4,5 millones de personas). Entre empleados en activo, muchas discapacidades son no evidentes (auditivas parciales, dislexia, TDAH, TEA). La accesibilidad afecta a una proporción mucho mayor de la plantilla de la que suele pensarse.

---

## Recursos relacionados

- 📘 [Plataformas LMS: cómo elegir la correcta](plataformas-lms-guia-elegir.md) — guía general.
- 📗 [Requisitos FUNDAE](requisitos-fundae-teleformacion.md) — normativa aplicable.
- ✅ [Checklist técnico LMS](checklist-tecnico-lms.md) — puntos accionables.
- 🔧 [SCORM, xAPI y LTI](scorm-xapi-lti-explicado.md) — estándares técnicos.

### Referencias oficiales

- [WCAG 2.1 — W3C](https://www.w3.org/TR/WCAG21/) - estándar oficial (inglés).
- [WCAG 2.1 en español](https://www.w3.org/WAI/translations/) - traducción autorizada.
- [Ley 11/2023 — BOE](https://www.boe.es/buscar/act.php?id=BOE-A-2023-11022)
- [Directiva (UE) 2019/882](https://eur-lex.europa.eu/eli/dir/2019/882/oj) - Acta Europea de Accesibilidad.
- [Fundación ONCE — Accesibilidad](https://www.fundaciononce.es)

---

*Publicado bajo licencia [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Libre uso con atribución a CiberAula y enlace a [www.ciberaula.com](https://www.ciberaula.com).*

*© 2026 Ana María González · Directora de CiberAula · Formación online para empresas desde 1996.*

---
