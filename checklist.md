---
layout: default
title: "Checklist WCAG 2.2 Nivel AA — Traducción al español"
"
permalink: /wcag-checklist/
---

---
description: "Traducción al español del checklist WCAG 2.2 AA de DigitalA11Y. "
layout: page
---

# WCAG 2.2 — Checklist Nivel AA  
## Leyenda
- **Criterio:** número y nombre del criterio WCAG.
- **Nivel:** A o AA.
- **Resumen:** qué exige el criterio.
- **Puntos a considerar:** prácticas recomendadas indicadas por el autor original.

---

# 1. Principio: Perceptible

---

## **1.1.1 Contenido no textual**  
**Nivel:** A  
**Resumen:** Proporcionar alternativas textuales para contenido no textual.  
**Puntos a considerar:**  
- Siempre proporcionar alternativas textuales para CAPTCHA, imágenes, iconos, gráficos o diagramas.  
- Usar descripciones textuales para gráficos complejos, además de un alt breve.  
- En enlaces con imágenes, usar `alt` + `title` cuando aporte información adicional.

---

## **1.2.1 Solo audio / solo vídeo (prerregrabado)**  
**Nivel:** A  
**Resumen:** Proporcionar alternativas para contenido solo audio o solo vídeo.  
**Puntos a considerar:**  
- Proporcionar transcripciones para audio.  
- Para vídeo sin audio: transcripción o pista de audio descriptiva.  

---

## **1.2.2 Subtítulos (prerregrabado)**  
**Nivel:** A  
**Resumen:** Proporcionar subtítulos para vídeo con audio.  
**Puntos a considerar:**  
- Si el vídeo reemplaza a contenido textual, no se requieren subtítulos.  
- Mejor si hay subtítulos en varios idiomas.

---

## **1.2.3 Audiodescripción o alternativa para vídeo**  
**Nivel:** A  
**Resumen:** Proporcionar audiodescripción o transcripción para vídeo con diálogo.  
**Puntos a considerar:**  
- No necesaria si el vídeo solo depende del audio (ej. discursos).  

---

## **1.2.4 Subtítulos (en vivo)**  
**Nivel:** AA  
**Resumen:** Proporcionar subtítulos en retransmisiones en vivo.  
**Puntos a considerar:**  
- Usar reproductores compatibles con subtitulado en directo.

---

## **1.2.5 Audiodescripción (prerregrabado)**  
**Nivel:** AA  
**Resumen:** Proporcionar audiodescripción cuando la información visual no esté en el diálogo.  
**Puntos a considerar:**  
- Debe describir cambios de escena, acciones, ajustes visuales esenciales.  

---

## **1.3.1 Información y relaciones**  
**Nivel:** A  
**Resumen:** La estructura debe poder determinarse programáticamente.  
**Puntos a considerar:**  
- Usar encabezados jerárquicos, listas, bloques de cita, etc.  
- Asociar correctamente las etiquetas en formularios.  
- Proporcionar encabezados de fila/columna en tablas.  

---

## **1.3.2 Secuencia significativa**  
**Nivel:** A  
**Resumen:** El orden de lectura debe ser lógico.  
**Puntos a considerar:**  
- El orden visual debe coincidir con el DOM.  
- Crear la estructura con HTML primero y luego estilizar con CSS.

---

## **1.3.3 Características sensoriales**  
**Nivel:** A  
**Resumen:** Las instrucciones no deben depender solo de color, forma o ubicación.  
**Puntos a considerar:**  
- Incluir texto para usuarios de lector de pantalla.  
- Combinar color + forma + etiqueta visible.

---

## **1.3.4 Orientación**  
**Nivel:** AA  
**Resumen:** El contenido debe funcionar en vertical y horizontal.  
**Puntos a considerar:**  
- No bloquear la orientación del dispositivo.

---

## **1.3.5 Identificar el propósito de entrada**  
**Nivel:** AA  
**Resumen:** Los campos deben tener propósito programático (autocomplete).  
**Puntos a considerar:**  
- Usar valores correctos de autocompletado.  

---

## **1.4.1 Uso del color**  
**Nivel:** A  
**Resumen:** El color no debe ser la única forma de transmitir información.  
**Puntos a considerar:**  
- Añadir iconos, texto u otros indicadores visuales.

---

## **1.4.2 Control de audio**  
**Nivel:** A  
**Resumen:** El usuario debe poder pausar audio > 3s.  
**Puntos a considerar:**  
- No reproducir audio automático si es posible.

---

## **1.4.3 Contraste mínimo**  
**Nivel:** AA  
**Resumen:** Texto vs fondo ≥ 4.5:1.  
**Puntos a considerar:**  
- Preparar hojas de estilo alternativas si no puede cumplirse en el diseño base.

---

## **1.4.4 Redimensionar texto**  
**Nivel:** AA  
**Resumen:** El texto debe poder ampliarse al 200%.  
**Puntos a considerar:**  
- Evitar scroll horizontal.  

---

## **1.4.5 Imágenes de texto**  
**Nivel:** AA  
**Resumen:** No usar imágenes de texto, salvo excepciones.  

---

## **1.4.10 Reflow / Reflujo**  
**Nivel:** AA  
**Resumen:** El contenido debe refluír sin scroll bidireccional.  
**Puntos a considerar:**  
- Evitar solapamientos en zoom 400%.

---

## **1.4.11 Contraste no textual**  
**Nivel:** AA  
**Resumen:** Elementos interactivos ≥ 3:1.  
**Puntos a considerar:**  
- Indicadores de foco con contraste adecuado.  

---

## **1.4.12 Espaciado de texto**  
**Nivel:** AA  
**Resumen:** El contenido debe seguir siendo funcional si se ajusta el espaciado.  

---

## **1.4.13 Contenido al pasar el puntero o foco**  
**Nivel:** AA  
**Resumen:** El contenido emergente debe ser descartable, persistente y accesible.  

---

# 2. Principio: Operable

(…)# 2. Principio: Operable

---

## **2.1.1 Teclado**
**Nivel:** A  
**Resumen:** Toda la funcionalidad debe ser operable con teclado, sin requisitos de tiempo.  
**Puntos a considerar:**  
- Todos los botones, enlaces y controles deben ser alcanzables con `Tab`.  
- Activables con `Enter` o `Barra espaciadora`.  
- El orden de foco debe ser visible y lógico.  
- Añadir `tabindex="0"` a componentes personalizados.  
- Evitar "accesskeys" que puedan entrar en conflicto.

---

## **2.1.2 Sin trampa de teclado**
**Nivel:** A  
**Resumen:** El usuario no debe quedar atrapado usando solo el teclado.  
**Puntos a considerar:**  
- Comprobar que siempre se puede navegar hacia y desde cualquier elemento.  
- Cualquier zona que requiera permanecer dentro debe incluir instrucciones de salida.  
- Revisar widgets de terceros que suelen causar trampas.

---

## **2.1.4 Atajos por tecla simple**
**Nivel:** A  
**Resumen:** Debe permitirse desactivar o reasignar atajos de una sola tecla.  
**Puntos a considerar:**  
- Preferir combinaciones con teclas no imprimibles.  
- Activar atajos solo cuando el elemento tenga el foco.

---

## **2.2.1 Tiempo ajustable**
**Nivel:** A  
**Resumen:** El usuario debe poder ajustar, extender o desactivar límites de tiempo.  
**Puntos a considerar:**  
- Ofrecer control para extender el tiempo ×10.  
- Notificar antes de la expiración de sesión.  
- Contenido en movimiento debe permitir pausar o detener.

---

## **2.2.2 Pausar, detener, ocultar**
**Nivel:** A  
**Resumen:** El usuario debe poder controlar contenido en movimiento.  
**Puntos a considerar:**  
- No permitir parpadeos mayores a 3 por segundo.  
- Proporcionar botón de pausa en carruseles y autoactualizaciones.  

---

## **2.3.1 Tres destellos o menos**
**Nivel:** A  
**Resumen:** No debe haber contenido que destelle > 3 veces por segundo.  
**Puntos a considerar:**  
- Evitar completamente el parpadeo.  
- Utilizar herramientas como PEAT para verificar.

---

## **2.4.1 Saltar bloques**
**Nivel:** A  
**Resumen:** Debe existir un mecanismo para saltar bloques repetitivos.  
**Puntos a considerar:**  
- Incluir “Saltar al contenido principal”.  
- Asegurar que los enlaces de salto sean visibles al recibir foco.  
- Usar landmarks ARIA con nombres únicos cuando haya múltiples.

---

## **2.4.2 Título de la página**
**Nivel:** A  
**Resumen:** Cada página debe tener un título útil y claro.  
**Puntos a considerar:**  
- Entre 50 y 75 caracteres.  
- El título debe describir el propósito de la página.

---

## **2.4.3 Orden del foco**
**Nivel:** A  
**Resumen:** El foco debe seguir una secuencia lógica.  
**Puntos a considerar:**  
- No usar `tabindex > 1`.  
- Mantener la alineación con el orden de lectura.

---

## **2.4.4 Propósito del enlace (en contexto)**
**Nivel:** A  
**Resumen:** El propósito de cada enlace debe ser claro.  
**Puntos a considerar:**  
- Evitar “clic aquí”.  
- Para enlaces con imágenes, el `alt` debe indicar el propósito.

---

## **2.4.5 Múltiples vías**
**Nivel:** AA  
**Resumen:** Debe haber al menos dos formas de localizar páginas.  
**Puntos a considerar:**  
- Búsqueda, menús, breadcrumbs u otras vías alternativas.

---

## **2.4.6 Encabezados y etiquetas**
**Nivel:** AA  
**Resumen:** Deben describir claramente el tema o propósito.  
**Puntos a considerar:**  
- Mantener consistencia en toda la interfaz.

---

## **2.4.7 Foco visible**
**Nivel:** AA  
**Resumen:** El foco debe ser claramente visible.  
**Puntos a considerar:**  
- Asegurar contraste suficiente entre el indicador de foco y el fondo.

---

## **2.4.11 Foco no oculto (mínimo)**
**Nivel:** AA  
**Resumen:** El foco no debe quedar oculto tras otros contenidos.  
**Puntos a considerar:**  
- Asegurar que los elementos permanezcan visibles al recibir foco.  
- Usar `scroll-padding` con elementos sticky.

---

## **2.5.1 Gestos con puntero**
**Nivel:** A  
**Resumen:** Los gestos complejos deben tener alternativas de un solo puntero.  
**Puntos a considerar:**  
- Ofrecer clic simple o doble clic como alternativa a arrastrar.

---

## **2.5.2 Cancelación del puntero**
**Nivel:** A  
**Resumen:** La acción no debe ejecutarse solo con el evento “down”.  
**Puntos a considerar:**  
- Permitir cancelar acciones.  
- Proporcionar confirmaciones cuando sea necesario.

---

## **2.5.3 Etiqueta en el nombre**
**Nivel:** A  
**Resumen:** El nombre accesible debe contener el texto visible del componente.  
**Puntos a considerar:**  
- El nombre accesible debe comenzar por el texto visible.

---

## **2.5.4 Activación por movimiento**
**Nivel:** A  
**Resumen:** Debe haber alternativas a la activación por movimiento.  
**Puntos a considerar:**  
- Permitir desactivar la detección de movimiento mediante ajustes del sistema.

---

## **2.5.7 Movimientos de arrastre**
**Nivel:** AA  
**Resumen:** Las funciones de arrastrar deben tener alternativas sin arrastre.  
**Puntos a considerar:**  
- Ofrecer métodos equivalentes sin arrastrar.  
- Simplificar interacciones.

---

## **2.5.8 Tamaño de objetivo (mínimo)**
**Nivel:** AA  
**Resumen:** Objetivos interactivos ≥ 24×24 CSS px o proporcionar suficiente espacio.  
**Puntos a considerar:**  
- Evitar activaciones accidentales.  
- Asegurar separación entre elementos.

---# 3. Principio: Comprensible

---

## **3.1.1 Idioma de la página**  
**Nivel:** A  
**Resumen:** Cada página debe indicar el idioma principal mediante el atributo `lang`.  
**Puntos a considerar:**  
- Usar códigos correctos: `lang="es"`, `lang="en-us"`, `lang="pt-br"`, etc.  
- Cada página del sitio debe declararlo explícitamente.

---

## **3.1.2 Idioma de las partes**  
**Nivel:** AA  
**Resumen:** Los fragmentos en otro idioma deben marcarse con el atributo `lang`.  
**Puntos a considerar:**  
- Aplicar `lang` a frases, citas o palabras extranjeras que cambien la pronunciación.  
- Evitar incorrectos cambios de idioma.

---

## **3.2.1 Al recibir foco**  
**Nivel:** A  
**Resumen:** Los elementos no deben cambiar automáticamente cuando reciben el foco.  
**Puntos a considerar:**  
- No realizar acciones ni cambios bruscos solo por enfocar un elemento.  
- Comprobar con navegación por teclado (sin ratón).

---

## **3.2.2 Al introducir datos**  
**Nivel:** A  
**Resumen:** Introducir datos no debe causar cambios de contexto inesperados.  
**Puntos a considerar:**  
- No enviar formularios automáticamente al rellenar un campo.  
- Mantener el foco en el mismo control salvo indicación explícita.  

---

## **3.2.3 Navegación consistente**  
**Nivel:** AA  
**Resumen:** Los mecanismos de navegación deben ser consistentes en todas las páginas.  
**Puntos a considerar:**  
- Mantener los menús en la misma ubicación.  
- Orden constante de elementos globales (logo, buscador, navegación principal).

---

## **3.2.4 Identificación consistente**  
**Nivel:** AA  
**Resumen:** Componentes con la misma función deben identificarse de forma coherente.  
**Puntos a considerar:**  
- Usar los mismos iconos/etiquetas para acciones iguales.  
- El `alt` de un mismo icono debe ser consistente.

---

## **3.2.6 Ayuda consistente**  
**Nivel:** A  
**Resumen:** Las opciones de ayuda deben presentarse de forma programática y consistente.  
**Puntos a considerar:**  
- Usar siempre los mismos mecanismos (contacto humano, FAQ, etc.).  
- Ubicación uniforme del acceso a ayuda.

---

## **3.3.1 Identificación de errores**  
**Nivel:** A  
**Resumen:** Los errores deben identificarse y describirse mediante texto.  
**Puntos a considerar:**  
- No usar solo color.  
- Relacionar los errores con campos mediante `aria-describedby`.  
- No deshabilitar el botón "Enviar".

---

## **3.3.2 Etiquetas o instrucciones**  
**Nivel:** A  
**Resumen:** Los campos deben tener etiquetas visibles y claras.  
**Puntos a considerar:**  
- Asociar programáticamente las etiquetas (`for` + `id`).  
- Proporcionar instrucciones para formatos específicos.  
- En grupos (teléfono, tarjeta): etiqueta de grupo + etiquetas individuales.

---

## **3.3.3 Sugerencias de error**  
**Nivel:** AA  
**Resumen:** Cuando sea apropiado, ofrecer sugerencias para corregir errores.  
**Puntos a considerar:**  
- Mostrar pistas claras.  
- Mover el foco al control con error al fallar la validación.  
- Marcar campos obligatorios visual y programáticamente (`aria-required`).

---

## **3.3.4 Prevención de errores (legal, financiero, datos)**  
**Nivel:** AA  
**Resumen:** Ofrecer confirmación antes de acciones importantes.  
**Puntos a considerar:**  
- Pantallas de revisión previa.  
- Confirmaciones antes de eliminar información.  
- Botón para validar que la persona ha revisado los datos.

---

## **3.3.7 Entrada redundante**  
**Nivel:** A  
**Resumen:** Evitar que el usuario tenga que repetir la misma información.  
**Puntos a considerar:**  
- Permitir selección de valores ya introducidos.  
- El contenido debe estar accesible en la misma página para copiar/pegar.

---

## **3.3.8 Autenticación accesible (mínimo)**  
**Nivel:** AA  
**Resumen:** La autenticación debe ser accesible sin requerir capacidades cognitivas excesivas.  
**Puntos a considerar:**  
- Permitir autenticación mediante teclado.  
- Ofrecer alternativas sin desafíos cognitivos complejos.  
- Usar sistemas modernos como magic links o autenticación biométrica.

---

# 4. Principio: Robusto

---

## **4.1.2 Nombre, rol y valor**  
**Nivel:** A  
**Resumen:** La tecnología debe poder interpretar nombre, rol y valor de cada componente.  
**Puntos a considerar:**  
- Usar elementos HTML nativos siempre que sea posible.  
- Para componentes personalizados, usar WAI-ARIA adecuadamente.  
- Asegurar operabilidad con teclado.

---

## **4.1.3 Mensajes de estado**  
**Nivel:** AA  
**Resumen:** Los mensajes de estado deben ser anunciados por lectores de pantalla automáticamente.  
**Puntos a considerar:**  
- Usar regiones vivas solo cuando sean necesarias.  
- Distinguir entre mensajes importantes y triviales.  
- No convertir mensajes en elementos enfocables (no son controles interactivos).

---

# Fin de la tabla WCAG 2.2 AA traducida

---
> **Atribución obligatoria**  
> Traducción del checklist “WCAG 2.2 AA Checklist” de **Raghavendra Satish Peri**, publicado originalmente en **DigitalA11Y** → https://digitala11y.com/  
> Traducción publicada con permiso del autor.