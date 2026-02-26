---
layout: default
title: "Ejemplos de roles ARIA"
permalink: /aria-roles
---

<!--  
  Ejemplo educativo para mostrar roles ARIA.
  Este archivo mezcla Markdown y HTML para asegurar
  que los roles se interpreten correctamente por lectores de pantalla.
-->

# Página de ejemplo: Roles ARIA

Esta página muestra ejemplos simples de roles ARIA aplicados a elementos HTML.  
Cada ejemplo incluye:

- Una breve explicación  
- El código correspondiente  
- El elemento real para que pueda ser leído por un lector de pantalla  

---

## Roles de estructura (landmark roles)

Los roles de estructura ayudan a los lectores de pantalla a entender la organización general de la página.

### role="banner"

```html
<div role="banner">
  <h1>Este es un encabezado dentro de un banner</h1>
</div>
```

<div role="banner" style="padding:10px; border:1px solid #ccc;">
  <h1>Este es un encabezado dentro de un banner</h1>
</div>

---

### role="main"

```html
<main role="main">
  <p>Contenido principal de la página.</p>
</main>
```

<main role="main" style="padding:10px; border:1px solid #ccc;">
  <p>Contenido principal de la página.</p>
</main>

---

### role="contentinfo"

```html
<footer role="contentinfo">
  <p>Información del sitio o pie de página.</p>
</footer>
```

<footer role="contentinfo" style="padding:10px; border:1px solid #ccc;">
  <p>Información del sitio o pie de página.</p>
</footer>

---

## Roles de encabezado (heading roles)

Los roles `heading` permiten crear encabezados con niveles personalizados.

### role="heading" aria-level="1"

```html
<div role="heading" aria-level="1">Encabezado simulado nivel 1</div>
```

<div role="heading" aria-level="1" style="font-size:1.6em; font-weight:bold;">
  Encabezado simulado nivel 1
</div>

---

### role="heading" aria-level="2"

```html
<div role="heading" aria-level="2">Encabezado simulado nivel 2</div>
```

<div role="heading" aria-level="2" style="font-size:1.4em; font-weight:bold;">
  Encabezado simulado nivel 2
</div>

---

### role="heading" aria-level="3"

```html
<div role="heading" aria-level="3">Encabezado simulado nivel 3</div>
```

<div role="heading" aria-level="3" style="font-size:1.2em; font-weight:bold;">
  Encabezado simulado nivel 3
</div>

---

## Roles de widgets simples

Aquí mostramos ejemplos de widgets básicos: botones, casillas de verificación y enlaces.

### role="button"

```html
<div role="button" tabindex="0">Botón ARIA</div>
```

<div role="button" tabindex="0" style="padding:8px; border:1px solid #333; width:120px; text-align:center;">
  Botón ARIA
</div>

---

### role="checkbox"

```html
<div role="checkbox" aria-checked="false" tabindex="0">
  Casilla ARIA sin marcar
</div>
```

<div role="checkbox" aria-checked="false" tabindex="0" style="padding:8px; border:1px solid #333; width:200px;">
  Casilla ARIA sin marcar
</div>

---

### role="link"

```html
<span role="link" tabindex="0">Enlace ARIA</span>
```

<span role="link" tabindex="0" style="color:blue; text-decoration:underline;">
  Enlace ARIA
</span>

---

