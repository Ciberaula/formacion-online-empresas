---
title: "SCORM, xAPI y LTI explicados para responsables de formación"
description: "Guía práctica de los estándares de interoperabilidad en elearning: SCORM 1.2, SCORM 2004, xAPI (Tin Can) y LTI. Qué son, para qué sirven, qué elegir según el caso, y por qué importan tanto para la portabilidad del contenido formativo corporativo."
author: "Ana María González"
author_role: "Directora de CiberAula"
published: "2026-04-17"
updated: "2026-04-17"
canonical_url: "https://github.com/Ciberaula/formacion-online-empresas/blob/main/plataformas_lms/scorm-xapi-lti-explicado.md"
license: "CC BY-SA 4.0"
tags: ["scorm", "xapi", "tin-can", "lti", "estandares-elearning", "interoperabilidad"]
---

---

# SCORM, xAPI y LTI explicados para responsables de formación

> **Resumen en 3 frases:** SCORM, xAPI y LTI son los tres estándares principales de interoperabilidad en elearning que permiten que un curso creado en una herramienta pueda reproducirse y rastrearse en una plataforma LMS diferente. Conocerlos bien es crítico porque determinan la portabilidad del contenido formativo, las capacidades de trazabilidad y la capacidad de cambiar de plataforma en el futuro sin empezar de cero. Esta guía explica cada estándar, cuándo usarlo, cómo verificar que tu plataforma lo soporta de verdad, y los errores frecuentes al empaquetar contenido formativo para un LMS.

**Última actualización:** 17 de abril de 2026
**Autora:** Ana María González · Directora de CiberAula
**Tiempo estimado de lectura:** 10 minutos
**Licencia:** CC BY-SA 4.0

---

## Índice

1. [Por qué importan los estándares](#por-que-importan)
2. [SCORM: el estándar clásico](#scorm)
3. [xAPI (Tin Can): el sucesor moderno](#xapi)
4. [LTI: integración de herramientas externas](#lti)
5. [Comparativa rápida](#comparativa)
6. [Cuál elegir según el caso](#cual-elegir)
7. [Errores frecuentes al empaquetar contenido](#errores)
8. [Preguntas frecuentes](#faq)

---

## <a id="por-que-importan"></a>1. Por qué importan los estándares

Imagina que has creado 50 cursos de formación para tu empresa durante los últimos 5 años con mucho esfuerzo. Has invertido tiempo, dinero y trabajo de expertos. Un día, tu proveedor de LMS sube los precios un 400% o cambia las condiciones del servicio. Quieres cambiar de plataforma.

**Si tus cursos están en un formato estándar (SCORM o xAPI), puedes importarlos a otra plataforma y seguir usándolos. Si están en un formato propietario, pueden ser prácticamente imposibles de migrar, y tendrías que rehacerlos.**

Esa es la razón principal por la que los estándares importan: **independencia del proveedor**. Pero no es la única.

Los estándares también garantizan:

- Que el contenido funcione igual en distintos LMS.
- Que la información de progreso del alumno sea comprensible entre sistemas.
- Que los autores puedan usar distintas herramientas de creación (Articulate, Adobe Captivate, iSpring, Rise, Storyline) y que el resultado se pueda subir a cualquier LMS.
- Que el contenido sea "reutilizable": se empaqueta una vez y se reutiliza en múltiples cursos o contextos.

Los tres estándares relevantes hoy son: **SCORM**, **xAPI** y **LTI**. Los explicamos uno por uno.

---

## <a id="scorm"></a>2. SCORM: el estándar clásico

### Qué es

**SCORM (Sharable Content Object Reference Model)** es un estándar desarrollado originalmente por el Departamento de Defensa de Estados Unidos a finales de los años 90. Su objetivo era que el mismo curso funcionase en distintos LMS militares. Se ha convertido en el estándar de facto del elearning corporativo mundial y lleva más de 20 años en uso estable.

### Cómo funciona técnicamente

Un curso SCORM es un **paquete ZIP** con una estructura específica:

- Un archivo `imsmanifest.xml` que describe la estructura del curso (módulos, evaluaciones, orden).
- Archivos HTML, JavaScript, CSS, imágenes, vídeos del contenido.
- Un script de comunicación con el LMS llamado "SCORM API" o "SCORM RTE" (Run-Time Environment).

Cuando el alumno entra al curso, el LMS carga el paquete y abre una conexión con la SCORM API. A partir de ese momento, el curso puede "hablar" con el LMS enviando información: "el alumno ha visto esta página", "ha fallado este test", "lleva 47 minutos", "ha completado el módulo 3".

### Versiones

Hay dos versiones vigentes en el mercado:

**SCORM 1.2 (2001).** La versión simple y más extendida. Funciona en prácticamente cualquier LMS del mundo. Permite registrar: estado (incompleto/completado/aprobado/suspendido), puntuación, tiempo, ubicación dentro del curso. Es suficiente para la mayoría de la formación corporativa bonificada española.

**SCORM 2004 (con varias ediciones, la más actual es la 4ª edición).** Versión más sofisticada. Permite navegación condicional compleja, múltiples objetivos de aprendizaje, secuenciación avanzada. Menos universal: algunos LMS solo soportan la 1.2.

**Recomendación práctica**: si tu LMS soporta SCORM 1.2 y 2004 4ª edición, estás bien. Si tus cursos se empaquetan como SCORM 1.2, funcionarán en más plataformas.

### Limitaciones

- **Solo funciona dentro del LMS**. El alumno tiene que estar en el LMS para que se registre su actividad.
- **No funciona offline** (o lo hace de forma muy limitada).
- **Trazabilidad limitada**. Registra lo básico, pero no granular (por ejemplo, no registra bien interacciones dentro de una simulación compleja).
- **No funciona bien en móviles** en algunas implementaciones antiguas.

---

## <a id="xapi"></a>3. xAPI (Tin Can): el sucesor moderno

### Qué es

**xAPI (Experience API)**, conocida popularmente como **Tin Can API** por su nombre de proyecto original, es el estándar moderno publicado en 2013 como evolución de SCORM. Resuelve las principales limitaciones de SCORM.

### Cómo funciona

xAPI usa un concepto fundamentalmente distinto: en lugar de "el alumno está dentro del LMS y habla con él", xAPI dice "**las experiencias de aprendizaje pueden ocurrir en cualquier parte y se registran en un almacén central**".

Ese almacén central se llama **LRS (Learning Record Store)**. Puede estar dentro del LMS o ser un servicio independiente. Recibe "sentencias" con estructura:

> "[Actor] + [Verbo] + [Objeto]"

Por ejemplo:

- "Juan Pérez **ha completado** el curso de Seguridad en el Trabajo."
- "María García **ha acertado** 7 preguntas de 10 en el examen de IA Act."
- "Pedro López **ha visto** el vídeo 'Introducción a SCORM' durante 12 minutos."

### Ventajas sobre SCORM

- **Experiencias fuera del LMS**: si un empleado asiste a un curso presencial, el formador puede registrar su asistencia en el LRS. Si ve un vídeo en YouTube, puede registrarse. Si participa en un webinar, igual.
- **Funciona offline** y luego sincroniza cuando hay conexión.
- **Trazabilidad granular**: puede registrar cada interacción dentro de una simulación o juego serio.
- **Compatible con móviles** y apps nativas.
- **Datos compartibles** entre sistemas.

### Cuándo usar xAPI

Recomendado para:

- Formación con experiencias mixtas (online + presencial + webinars).
- Aprendizaje social y colaborativo.
- Simulaciones, juegos serios, VR/AR.
- Formación consumida mayoritariamente desde móvil.
- Empresas grandes con múltiples herramientas de aprendizaje.

### Limitaciones

- Menos universal que SCORM. No todos los LMS lo soportan bien.
- Requiere LRS (puede ser un coste adicional).
- Más complejo de implementar.
- **Para formación bonificada FUNDAE, SCORM sigue siendo la opción más segura** porque es más ampliamente validado en inspecciones.

---

## <a id="lti"></a>4. LTI: integración de herramientas externas

### Qué es

**LTI (Learning Tools Interoperability)** es un estándar distinto a SCORM y xAPI. No sirve para empaquetar contenido; sirve para **integrar herramientas externas dentro del LMS como si fueran nativas**.

### Cómo funciona

Imagina que tienes un LMS (Moodle, por ejemplo) y quieres integrar una herramienta externa de laboratorio virtual de química. Sin LTI, el alumno tendría que abrir una pestaña nueva, hacer login separado, y al terminar no quedaría constancia en el LMS.

Con LTI, la herramienta externa aparece **dentro del LMS**, el alumno no necesita hacer login adicional (se hace automáticamente), y al terminar la actividad, los resultados se envían al LMS como si fuera una actividad nativa.

### Versiones

- **LTI 1.1 y 1.2**: versiones antiguas, aún usadas.
- **LTI 1.3 (también llamada LTI Advantage)**: versión moderna, más segura, con más capacidades.

### Cuándo usar LTI

Relevante si tu LMS necesita integrarse con:

- Herramientas de programación (por ejemplo, replits o entornos de código).
- Laboratorios virtuales.
- Simuladores.
- Plataformas de evaluación por competencias externas.
- Herramientas de videoconferencia avanzadas (Zoom, BigBlueButton).
- Generadores de contenido IA.

### Limitaciones

- Solo tiene sentido si tu LMS y la herramienta externa lo soportan.
- En formación corporativa básica (cursos de compliance, idiomas, ofimática) no suele ser necesario.

---

## <a id="comparativa"></a>5. Comparativa rápida

| Característica | SCORM 1.2 | SCORM 2004 | xAPI | LTI |
|---|---|---|---|---|
| Año de publicación | 2001 | 2004 (4ª ed. 2009) | 2013 | 2010 (1.3 en 2019) |
| Propósito principal | Empaquetar contenido | Empaquetar contenido | Registrar experiencias | Integrar herramientas |
| Dónde vive el contenido | En el LMS | En el LMS | Cualquier lugar | Herramienta externa |
| Funciona offline | ❌ | ❌ parcial | ✅ | ❌ |
| Trazabilidad | Básica | Media | Granular | Según herramienta |
| Compatible con móvil | Parcial | Parcial | Sí | Sí |
| Soporte en LMS | Casi universal | Muy amplio | Creciente | Amplio |
| Recomendado para FUNDAE | ✅ | ✅ | ⚠️ caso a caso | ⚠️ caso a caso |
| Complejidad de implementación | Baja | Media | Alta | Media |

---

## <a id="cual-elegir"></a>6. Cuál elegir según el caso

### Formación corporativa bonificada estándar

**Usa SCORM 1.2.** Es el estándar más ampliamente reconocido, funciona en todos los LMS serios del mercado, y FUNDAE lo acepta sin problema. No te compliques con xAPI si no lo necesitas.

### Formación corporativa no bonificada con experiencias mixtas

**Plantéate xAPI** si vas a combinar formación online, presencial, webinars, simulaciones, y quieres trazabilidad unificada. Es una inversión mayor pero te da capacidades que SCORM no tiene.

### Formación con simuladores, laboratorios o herramientas externas

**Usa LTI** para integrar esas herramientas en tu LMS, además de SCORM/xAPI para el resto del contenido.

### Empresas pequeñas y medianas

**Quédate con SCORM 1.2**. Es suficiente para la inmensa mayoría de casos y minimiza la complejidad técnica.

### Empresas grandes con estrategia de learning analytics

**SCORM 2004 + xAPI** para tener lo mejor de ambos mundos. Usa SCORM para cursos donde es suficiente, y xAPI para experiencias ricas y analítica avanzada.

---

## <a id="errores"></a>7. Errores frecuentes al empaquetar contenido

Cuando el proveedor de contenido entrega un paquete SCORM, estos son los errores que más se repiten.

**Error 1: Publicar en una versión de SCORM que el LMS no soporta.** Antes de empaquetar, confirma con IT qué versiones soporta tu LMS. La mayoría de herramientas de autor permiten elegir entre 1.2 y 2004.

**Error 2: No incluir el `imsmanifest.xml` en la raíz del ZIP.** Si el manifest está en una subcarpeta, el LMS no reconoce el paquete. Antes de subir al LMS, abre el ZIP y verifica que el `imsmanifest.xml` está en la primera capa.

**Error 3: Paquetes con rutas absolutas.** Si el curso tiene rutas absolutas (`https://miservidor.com/curso/pagina1.html`) en lugar de relativas (`pagina1.html`), fallará en el LMS. Configura siempre rutas relativas.

**Error 4: Archivos con nombres con acentos o espacios.** `Lección 1.html` puede funcionar en Windows pero romperse en el servidor del LMS (que suele ser Linux). Usa solo letras, números, guiones y guiones bajos.

**Error 5: No configurar correctamente la condición de "completado".** Si el curso nunca envía al LMS la señal de "completado", el alumno puede estudiar 10 horas y el expediente figurará como "en curso". Configura la condición: por tiempo, por páginas visitadas, por aprobar evaluación.

**Error 6: Vídeos embebidos con tamaños excesivos.** Un SCORM de 2 GB dará problemas de carga y almacenamiento. Mejor: vídeos hospedados en plataforma aparte (Vimeo, YouTube privado, servidor propio) y embebidos en el SCORM.

**Error 7: No probar el paquete antes de distribuirlo.** Usa un "SCORM test runner" o crea un alumno de prueba en el LMS para verificar que todo funciona antes de lanzar el curso a los alumnos reales.

**Error 8: Empaquetar con herramientas obsoletas.** Las herramientas de autor evolucionan. Un SCORM empaquetado con Articulate Storyline 2 (de 2014) puede tener problemas en navegadores modernos. Actualiza la herramienta y re-empaqueta cursos antiguos.

---

## <a id="faq"></a>8. Preguntas frecuentes

### Si mi plataforma solo soporta SCORM 1.2, ¿estoy atrasada?

No necesariamente. SCORM 1.2 cubre el 90% de los casos de formación corporativa. Solo si planeas hacer experiencias muy sofisticadas (VR, simuladores complejos, analítica granular) echarás en falta algo más moderno.

### ¿Puedo convertir un curso SCORM a xAPI?

Técnicamente sí, con herramientas específicas. En la práctica suele ser más simple republicar el curso desde la herramienta de autor eligiendo xAPI como formato de salida.

### ¿Qué pasa si el LMS no soporta el estándar que me interesa?

Es un criterio eliminatorio. No compres un LMS que no soporte los estándares que necesitas. Las grandes plataformas (Moodle, la mayoría de SaaS profesionales) soportan SCORM 1.2, SCORM 2004 y xAPI.

### ¿Un curso SCORM y un curso xAPI pueden coexistir en el mismo LMS?

Sí, siempre que el LMS soporte ambos estándares. Muchos casos reales: usar SCORM para formación obligatoria bonificada y xAPI para aprendizaje adicional con más seguimiento.

### ¿Puedo hacer un curso sin estándar, solo HTML?

Puedes, pero el LMS no registrará automáticamente progreso, tiempo, ni resultados. Perderías la ventaja principal del LMS. Solo tiene sentido para contenido muy simple de consulta libre.

### ¿Moodle soporta todos estos estándares?

Sí. Moodle soporta SCORM 1.2 y 2004, tiene módulo oficial para xAPI, y soporta LTI 1.1, 1.3 y LTI Advantage. Es una de las razones por las que es tan popular.

### ¿Los certificados que emite el LMS dependen del estándar?

No. Los certificados son una funcionalidad del LMS, independiente del estándar del contenido. Un curso SCORM puede desencadenar la emisión de un certificado por parte del LMS cuando el alumno lo completa.

### ¿Cómo sé qué estándar usar cuando contrato contenidos a un proveedor?

Especifícalo en el contrato: "El contenido se entregará empaquetado en formato SCORM 1.2 compatible con Moodle 4.3 o superior, con evaluación final al completar y condición de 'completado' cuando el alumno apruebe el examen final con 75% o más."

### ¿Los estándares se actualizan?

SCORM prácticamente no se actualiza desde 2009. xAPI tuvo su última actualización significativa en 2016. LTI sigue evolucionando (LTI Advantage es de 2019). Todos son estándares maduros y estables, lo cual es bueno para la inversión a largo plazo.

---

## Recursos relacionados

- 📘 [Plataformas LMS: cómo elegir la correcta](plataformas-lms-guia-elegir.md) — guía general.
- 📗 [Requisitos FUNDAE](requisitos-fundae-teleformacion.md) — normativa aplicable.
- ✅ [Checklist técnico LMS](checklist-tecnico-lms.md) — puntos accionables.
- ♿ [Accesibilidad WCAG](accesibilidad-wcag-elearning.md) — cumplimiento legal.

### Referencias técnicas

- [ADL — Advanced Distributed Learning](https://adlnet.gov) — entidad que mantiene SCORM y xAPI.
- [IMS Global](https://www.imsglobal.org) — entidad que mantiene LTI y otros estándares.
- [Rustici Software](https://scorm.com) — recursos técnicos sobre SCORM y xAPI.

---

*Publicado bajo licencia [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Libre uso con atribución a CiberAula y enlace a [www.ciberaula.com](https://www.ciberaula.com).*

*© 2026 Ana María González · Directora de CiberAula · Formación online para empresas desde 1996.*

---
