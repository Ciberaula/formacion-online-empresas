---
title: "Requisitos FUNDAE de plataformas de teleformación"
description: "Guía detallada de los requisitos técnicos y funcionales que FUNDAE exige a las plataformas de teleformación para impartir formación bonificada en España. Normativa aplicable, qué revisan las inspecciones, y cómo verificar que un LMS cumple."
author: "Ana María González"
author_role: "Directora de CiberAula"
published: "2026-04-17"
updated: "2026-04-17"
canonical_url: "https://github.com/Ciberaula/formacion-online-empresas/blob/main/plataformas_lms/requisitos-fundae-teleformacion.md"
license: "CC BY-SA 4.0"
tags: ["fundae", "lms", "teleformacion", "requisitos-tecnicos", "formacion-bonificada", "cumplimiento"]
---


<div align="center">

![CiberAula · Formación online para empresas](../assets/banner.png)

</div>

---

# Requisitos FUNDAE de plataformas de teleformación

> **Resumen en 3 frases:** Cuando una empresa bonifica formación online con el crédito FUNDAE, la plataforma LMS utilizada debe cumplir requisitos técnicos específicos recogidos en el Real Decreto 694/2017, desarrollados por las Resoluciones del SEPE y consolidados por el Real Decreto 1189/2025 en vigor desde el 1 de enero de 2026. El incumplimiento de estos requisitos puede provocar el rechazo del expediente en una inspección, con obligación de devolver la bonificación aplicada más intereses de demora. Esta guía detalla qué exige exactamente FUNDAE, cómo se verifica en una inspección, y qué preguntas hacer al proveedor de LMS para asegurarte de que cumple.

**Última actualización:** 17 de abril de 2026
**Autora:** Ana María González · Directora de CiberAula
**Tiempo estimado de lectura:** 11 minutos
**Licencia:** CC BY-SA 4.0

---

## Índice

1. [Marco normativo aplicable](#marco-normativo)
2. [Requisitos técnicos imprescindibles](#requisitos-tecnicos)
3. [Requisitos funcionales](#requisitos-funcionales)
4. [Acceso en tiempo real para inspecciones](#acceso-inspecciones)
5. [Qué revisa exactamente FUNDAE en una inspección](#inspeccion)
6. [Cómo verificar que un LMS cumple](#verificar)
7. [Consecuencias del incumplimiento](#incumplimiento)
8. [Preguntas frecuentes](#faq)

---

## <a id="marco-normativo"></a>1. Marco normativo aplicable

Los requisitos que FUNDAE exige a las plataformas de teleformación no son arbitrarios: están recogidos en varios textos normativos concatenados. Saber dónde mirar te permite argumentar y, si es necesario, defender tu posición ante una inspección.

### Textos clave

**Real Decreto 694/2017**, de 3 de julio, por el que se desarrolla la Ley 30/2015 del Sistema de Formación Profesional para el Empleo en el ámbito laboral. Es el texto base. Los artículos 12, 19 y 20 regulan específicamente la teleformación.

**Real Decreto 1189/2025**, en vigor desde el 1 de enero de 2026. Modifica y consolida el RD 694/2017 introduciendo mejoras procedimentales, reforzando los requisitos técnicos y clarificando la distinción de competencias entre FUNDAE (colaboración técnica), SEPE (autorización y registro) e Inspección de Trabajo (actuaciones sancionadoras).

**Resoluciones del Servicio Público de Empleo Estatal (SEPE)**. Cada cierto tiempo, el SEPE publica resoluciones que concretan aspectos técnicos. Son vinculantes. Las más relevantes actualmente:

- Resolución sobre requisitos de las plataformas de teleformación (versión consolidada 2024).
- Resolución de 25 de noviembre de 2025, que clarifica el régimen de aula virtual y modalidad bimodal durante el ejercicio 2026.

**Instrucciones de seguimiento y control** del SEPE/FUNDAE. Documento operativo que detalla qué se inspecciona y cómo. Actualizado periódicamente.

**FAQ oficial de FUNDAE**. Disponible en fundae.es, con respuestas autorizativas a preguntas concretas que surgen en la práctica.

### Principio general

El principio de fondo es simple: la plataforma debe permitir a FUNDAE verificar objetivamente que **la formación se ha impartido realmente, al alumno correcto, durante el tiempo declarado, con el contenido aprobado, y con interacciones reales**. Todo requisito técnico es una concreción de este principio.

---

## <a id="requisitos-tecnicos"></a>2. Requisitos técnicos imprescindibles

### 2.1. Identificación inequívoca del alumno

La plataforma debe garantizar que quien se conecta como alumno es efectivamente la persona inscrita. Los mecanismos aceptados son:

- Usuario + contraseña personal e intransferible.
- Autenticación de doble factor (2FA) recomendada para formación con certificado oficial.
- En casos específicos (certificados de profesionalidad) pueden exigirse controles biométricos adicionales.

El alumno debe cambiar la contraseña en el primer acceso y no puede compartirla. El LMS debe registrar cada inicio de sesión con IP, dispositivo, fecha y hora.

### 2.2. Registro automático de tiempos de conexión

El sistema debe medir **objetivamente** cuánto tiempo está activo cada alumno en cada sesión. No es válido:

- Que el alumno "declare" que ha estado X horas.
- Que la plataforma calcule el tiempo por la diferencia entre login y logout sin detectar inactividad.
- Que se sumen tiempos si el alumno deja la ventana abierta pero no está interactuando.

Es válido:

- Medición de actividad real mediante eventos (clicks, scroll, avance en vídeos, interacciones con el contenido).
- Cierre automático de sesión tras X minutos de inactividad (típicamente 15-30 minutos).
- Distinción entre tiempo de conexión y tiempo efectivo de estudio.

### 2.3. Trazabilidad completa de interacciones

Todo lo que el alumno hace en la plataforma debe quedar registrado y ser recuperable:

- Acceso a cada módulo, página, recurso.
- Intentos de cuestionarios, respuestas dadas, puntuaciones.
- Participación en foros: mensajes enviados, hilos iniciados, respuestas recibidas.
- Descargas de documentos.
- Tiempo de visualización de cada vídeo, incluyendo si se saltó o aceleró partes.
- Interacciones con el tutor: mensajes, consultas, tareas entregadas.

Estos registros deben ser inalterables por el propio alumno y exportables en formato que permita auditoría.

### 2.4. Compatibilidad SCORM

La plataforma debe soportar al menos **SCORM 1.2 y SCORM 2004**. Esto es prácticamente estándar en el mercado, pero no todas las plataformas modernas "ligeras" lo implementan correctamente. Es un criterio eliminatorio para formación bonificada.

Además, el soporte debe ser **funcional**, no solo nominal: el LMS debe registrar correctamente los datos que el curso SCORM envía (estado, puntuación, tiempo, progreso, interacciones internas).

### 2.5. Capacidad de backup y recuperación

El sistema debe realizar copias de seguridad regulares (diarias recomendadas) que permitan reconstruir el expediente completo si hubiera un incidente técnico. El proveedor debe poder acreditar su política de backups.

### 2.6. Cumplimiento WCAG nivel AA

Desde junio de 2025, obligatorio por Ley de Accesibilidad. La plataforma debe permitir navegación completa por teclado, ser compatible con lectores de pantalla, tener subtítulos en vídeos, contraste adecuado, etc. Detalles en [accesibilidad-wcag-elearning.md](accesibilidad-wcag-elearning.md).

---

## <a id="requisitos-funcionales"></a>3. Requisitos funcionales

Más allá de lo estrictamente técnico, FUNDAE exige ciertas funcionalidades que la plataforma debe proporcionar.

### 3.1. Sistema de comunicación alumno-tutor

Debe existir un canal de comunicación bidireccional entre alumno y tutor, integrado en la plataforma (no por email externo). Habitualmente:

- Mensajería interna o sistema de tickets.
- Foros de consulta específicos de cada curso.
- Chat (opcional, muy valorado).
- Sesiones de tutoría en aula virtual si está declarada.

El tutor debe responder en un plazo razonable (habitualmente 48 horas en días laborables) y estas interacciones quedar registradas.

### 3.2. Evaluaciones con trazabilidad

La plataforma debe permitir:

- Cuestionarios de autoevaluación al final de cada módulo.
- Evaluación final sumativa para acreditar el aprovechamiento.
- Configuración de número de intentos, tiempo límite, puntuación mínima.
- Registro de cada intento con fecha, hora, respuestas y puntuación.
- Retroalimentación al alumno tras cada intento.

### 3.3. Control de progreso estructurado

El curso debe tener una secuencia lógica que el alumno sigue. No es admisible un sistema donde el alumno pueda saltar directamente al examen final sin haber interactuado con el contenido. La plataforma debe:

- Controlar que el alumno complete cada módulo antes de pasar al siguiente (o al menos que lo haya visitado).
- Mostrar al alumno su progreso visualmente.
- Bloquear el examen final hasta completar el contenido obligatorio.

### 3.4. Emisión de certificados

La plataforma debe emitir automáticamente un certificado o diploma de aprovechamiento cuando el alumno cumple los criterios definidos (típicamente: 75% de contenido completado + aprobar el examen final). El certificado debe incluir al menos: nombre del alumno, nombre del curso, horas, fecha y, preferiblemente, un código verificable.

### 3.5. Informes y exportación

La empresa y el tutor deben poder generar informes:

- Actividad individual de cada alumno.
- Estado global del curso.
- Estadísticas agregadas.
- Exportación en formatos abiertos (PDF, Excel, CSV) para presentar ante inspección.

---

## <a id="acceso-inspecciones"></a>4. Acceso en tiempo real para inspecciones

Este es un requisito específico de FUNDAE que muchas plataformas comerciales "genéricas" no implementan bien. Es crítico.

### Obligación

Desde 2011, y reforzado en el RD 1189/2025, la entidad organizadora (o la empresa si se organiza internamente) está obligada a proporcionar a FUNDAE, en la comunicación de inicio de la acción formativa, **credenciales específicas de acceso** a la plataforma para que la autoridad pueda inspeccionar la actividad en tiempo real.

Estos datos son:

- **URL** de acceso directo al curso.
- **Usuario** específico creado para el inspector.
- **Contraseña** específica.
- **Perfil** con visibilidad completa del curso (como si fuera alumno, pero sin alterar los expedientes reales).

### Implicaciones técnicas

La plataforma debe permitir:

- Crear usuarios con perfil "inspector" o "observador" sin consumir plaza de alumno.
- Acceso a los contenidos completos del curso sin alterar métricas.
- Acceso a los foros y espacios de comunicación.
- Visibilidad de los materiales entregables y evaluables.

No todas las plataformas lo soportan nativamente. Algunas requieren configuración específica. Esta capacidad debe verificarse **antes** de comprar la plataforma, no después.

### Inspección in situ presencial

Además del acceso telemático, FUNDAE puede realizar visitas de inspección presenciales sin preaviso al lugar de impartición. En teleformación pura, esto puede traducirse en inspecciones al centro que hospeda la plataforma. En modalidades mixtas o con aula virtual, pueden personarse en la sala física o conectarse a la sesión de aula virtual.

---

## <a id="inspeccion"></a>5. Qué revisa exactamente FUNDAE en una inspección

Saber lo que se inspecciona te permite prepararte. Estos son los puntos concretos que los inspectores verifican.

### Durante el periodo de impartición (inspección en tiempo real)

- **Acceso efectivo al curso** con las credenciales proporcionadas.
- **Contenido declarado** coincide con el contenido real impartido. Horas declaradas = horas reales de contenido.
- **Identificación correcta** del curso, contenidos, docente, fechas en la plataforma.
- **Actividad de los alumnos**: porcentajes de conexión, acceso reciente, progresos.
- **Tutor accesible**: hay figura de tutor real, no un nombre ficticio. Responde consultas.
- **Foros activos**: hay mensajes reales, no solo de maqueta.
- **Entregables**: si hay tareas prácticas, existen y se están realizando.

### Tras la finalización (inspección ex post)

- **Expediente completo** disponible y recuperable.
- **Registro de tiempos** coherente: el alumno ha estado el tiempo mínimo exigido.
- **Evaluación final** presente, aprobada y con trazabilidad.
- **Certificados** emitidos correctamente.
- **Coherencia entre declaraciones y registros**: lo declarado a FUNDAE (fechas, horas, alumnos, modalidad) coincide con lo que consta en la plataforma.
- **Conservación de documentación** durante 4 años: contratos, planificaciones, diplomas, evaluaciones.

### Comprobación automática (SECIR)

SECIR (Sistema Experto de Cálculo de Índice de Riesgo) es el algoritmo que FUNDAE usa para priorizar qué expedientes inspeccionar. Entre otros factores, valora:

- Volumen de la empresa bonificadora (crédito usado respecto al disponible).
- Histórico: si la empresa ha tenido rechazos previos o actuaciones.
- Anomalías estadísticas (concentración temporal, ratios alumno/tutor inusuales).
- Modalidades inusuales para la actividad de la empresa.
- Colaboraciones con entidades organizadoras con historial problemático.

Una empresa con score SECIR alto tiene mayor probabilidad de ser inspeccionada. No puedes reducir el score a voluntad, pero sí puedes asegurarte de que si llega la inspección, todo está en regla.

---

## <a id="verificar"></a>6. Cómo verificar que un LMS cumple

Cuando evalúes una plataforma LMS para formación bonificada, estas son las preguntas concretas que debes hacer al proveedor. Pide respuestas por escrito.

### Preguntas técnicas

1. ¿Soporta SCORM 1.2 y SCORM 2004? ¿En qué grado (solo runtime básico o completo)?
2. ¿Cómo mide el tiempo efectivo de estudio? ¿Detecta inactividad automáticamente?
3. ¿Qué eventos de interacción registra? ¿Puede exportarse el log completo?
4. ¿Cuál es la política de backups? ¿Cada cuánto se hacen? ¿Dónde se almacenan?
5. ¿Cumple WCAG 2.1 nivel AA? ¿Puede proporcionarnos la auditoría de accesibilidad?
6. ¿Cómo gestiona los usuarios "inspector" o "observador" sin consumir plazas?

### Preguntas funcionales

7. ¿Puede bloquearse el acceso al examen final hasta completar el contenido obligatorio?
8. ¿El sistema de foros y mensajería está integrado en la plataforma?
9. ¿Cómo se emiten los certificados? ¿Son verificables externamente?
10. ¿Los informes exportables incluyen toda la información que FUNDAE puede solicitar?

### Preguntas sobre cumplimiento normativo

11. ¿Tienen otras empresas españolas usando la plataforma para formación bonificada? ¿Cuántas?
12. ¿Han pasado inspecciones de FUNDAE? ¿Pueden facilitarnos referencias?
13. ¿Tienen documento específico de cumplimiento FUNDAE actualizado al RD 1189/2025?
14. ¿Dónde se alojan físicamente los datos? ¿Es compatible con RGPD?

### Preguntas sobre soporte en contexto FUNDAE

15. ¿Qué soporte ofrecen si hay un requerimiento o inspección de FUNDAE?
16. ¿Hay un equipo técnico que entienda la normativa española de formación bonificada?
17. ¿Cuánto tiempo tardan en configurar el acceso para un inspector de FUNDAE cuando se necesita?

Si un proveedor no puede responder con claridad a la mayoría de estas preguntas, considera que probablemente no cumple.

---

## <a id="incumplimiento"></a>7. Consecuencias del incumplimiento

Si una inspección determina que la plataforma no cumplía los requisitos y que, por tanto, la formación bonificada no se impartió en condiciones reglamentarias, las consecuencias pueden ser:

### Devolución de la bonificación

La empresa debe devolver la totalidad de la bonificación aplicada. FUNDAE emite una resolución de minoración que se ejecuta vía TGSS.

### Intereses de demora

Si la devolución se tramita vía acta de liquidación de la Inspección de Trabajo, se añaden intereses de demora calculados desde el momento del disfrute indebido de la bonificación. Estos intereses pueden representar un 15-25% adicional sobre la cantidad principal.

### Expedientes afectados

No es solo la acción formativa concreta; puede extenderse a otras acciones si hay patrón sistemático de incumplimiento. Una sola plataforma mal configurada puede comprometer expedientes de varios años.

### Sanciones accesorias

En casos graves (incumplimiento doloso, fraude), pueden aplicarse sanciones específicas según la Ley 5/2000 sobre infracciones y sanciones en el orden social (LISOS). Las sanciones muy graves pueden alcanzar 187.515 €.

### Pérdida de reputación ante FUNDAE

La empresa pasa al perfil de riesgo alto en SECIR, lo que incrementa la probabilidad de futuras inspecciones. Es un daño reputacional con consecuencias operativas a largo plazo.

---

## <a id="faq"></a>8. Preguntas frecuentes

### ¿Tiene FUNDAE una lista oficial de plataformas aprobadas?

No, FUNDAE no certifica ni aprueba plataformas específicas. Cada acción formativa se valida individualmente. La responsabilidad de que la plataforma cumpla recae en la entidad organizadora o la empresa.

### ¿Vale cualquier plataforma open source como Moodle?

Moodle, correctamente configurado, cumple todos los requisitos FUNDAE y es la plataforma más usada en España para formación bonificada. Pero la configuración por defecto no siempre es suficiente: hay que ajustar parámetros de tiempo, logs, identificación, bloqueo progresivo y otros.

### ¿Y una plataforma extranjera como Cornerstone, Docebo o LearnWorlds?

Pueden cumplir técnicamente, pero a menudo requieren configuración específica para el mercado español. Verifica con el proveedor que:
- Tienen experiencia con FUNDAE.
- Pueden configurar usuario inspector FUNDAE.
- Tienen soporte en español.
- Alojan datos en la UE (por RGPD).

### ¿Y si uso una web con cursos en vídeo sin LMS formal?

No sirve para formación bonificada. Una web que solo reproduce vídeos no registra tiempos, interacciones, evaluaciones ni emite certificados. FUNDAE lo rechazará.

### ¿Aula virtual cuenta como teleformación?

Desde la Resolución del 25 de noviembre de 2025, sí: el aula virtual en directo puede considerarse teleformación durante el ejercicio 2026 (y probablemente consolidarse después). Pero el acceso a las sesiones debe estar controlado y registrado en una plataforma LMS que cumpla los requisitos.

### ¿Si la plataforma está en inglés, vale?

Vale técnicamente, pero es muy recomendable que los alumnos puedan navegar en español. Si el alumno no entiende la plataforma, difícilmente aprovechará el curso. Además, los inspectores pueden requerir interacciones en español.

### ¿Puedo cambiar de plataforma en mitad de una acción formativa bonificada?

Lo ideal es no hacerlo. Si es inevitable, hay que comunicarlo a FUNDAE y documentar minuciosamente la continuidad del expediente. Es un escenario de riesgo alto.

### ¿Cuánto tiempo debe conservar la empresa los datos de la plataforma?

**Mínimo 4 años** desde la finalización de la acción formativa, por exigencia del RD 694/2017. Algunas normativas sectoriales pueden exigir más (hasta 10 años en algunos casos).

### ¿Qué pasa si el proveedor de LMS deja de dar servicio?

Es un escenario crítico. Por eso es clave:
- Tener capacidad de exportar todos los datos en cualquier momento.
- Guardar copias regulares en infraestructura propia.
- Revisar las cláusulas de terminación del contrato.

---

## Recursos relacionados

- 📘 [Plataformas LMS: cómo elegir la correcta](plataformas-lms-guia-elegir.md) — guía general.
- ✅ [Checklist técnico de evaluación LMS](checklist-tecnico-lms.md) — puntos accionables.
- 🔧 [SCORM, xAPI y LTI explicados](scorm-xapi-lti-explicado.md) — estándares.
- ♿ [Accesibilidad WCAG](accesibilidad-wcag-elearning.md) — cumplimiento legal.
- 📘 [Guía FUNDAE completa](https://github.com/Ciberaula/guia-formacion-bonificada-fundae) — repositorio complementario.

### Normativa y fuentes oficiales

- [Real Decreto 694/2017 — BOE](https://www.boe.es/buscar/act.php?id=BOE-A-2017-7769)
- [FUNDAE — Fundación Estatal para la Formación en el Empleo](https://www.fundae.es)
- [SEPE — Servicio Público de Empleo Estatal](https://www.sepe.es)

---

*Publicado bajo licencia [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Libre uso con atribución a CiberAula y enlace a [www.ciberaula.com](https://www.ciberaula.com).*

*© 2026 Ana María González · Directora de CiberAula · Formación online para empresas desde 1996.*

---

<div align="center">

![CiberAula · Ecosistema de formación abierta](../assets/footer_ecosistema.png)

### Ecosistema documental abierto de CiberAula

📘 [**Guía FUNDAE**](https://github.com/Ciberaula/guia-formacion-bonificada-fundae) · 🧠 [**IA para empresas**](https://github.com/Ciberaula/ia-empresas-espana) · 🎓 [**Formación online**](https://github.com/Ciberaula/formacion-online-empresas)

---

**CiberAula · Formación online para empresas desde 1996**

[www.ciberaula.com](https://www.ciberaula.com) · admision@ciberaula.com · 91 390 68 47 · Madrid

*Contenido bajo licencia [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es) · Libre uso con atribución*

</div>
