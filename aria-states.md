---
layout: default
title: "Ejemplos de estados ARIA"
permalink: /aria-states
---



Los estados ARIA permiten comunicar a los lectores de pantalla información dinámica o interactiva que no siempre es evidente visualmente.  
Esta página muestra ejemplos de buen uso y mal uso de los estados más comunes.

---

## aria-disabled

Indica que un elemento **no está disponible para interacción**.  
No sustituye al atributo HTML `disabled` cuando este existe.

### ✔️ Buen uso: elemento no nativo que simula un botón

```html
<div role="button" aria-disabled="true" tabindex="-1">
  Acción no disponible
</div>
```

<div role="button" aria-disabled="true" tabindex="-1" style="padding:8px; border:1px solid #aaa; color:#777;">
  Acción no disponible
</div>

**Por qué es correcto:**  
El elemento no es un `<button>` real, así que `aria-disabled` comunica el estado.

---

### ❌ Mal uso: sustituir `disabled` en un `<button>`

```html
<button aria-disabled="true">Enviar</button>
```

**Problema:**  
El botón sigue siendo interactivo para teclado y ratón.  
Debe usarse:

```html
<button disabled>Enviar</button>
```

---

## aria-hidden

Oculta un elemento **solo para tecnologías de asistencia**.  
No lo oculta visualmente.

### ✔️ Buen uso: icono decorativo

```html
<button>
  <span aria-hidden="true">🔍</span> Buscar
</button>
```

<button style="padding:8px; border:1px solid #333;">
  <span aria-hidden="true">🔍</span> Buscar
</button>

**Por qué es correcto:**  
El icono no aporta información.

---

### ❌ Mal uso: ocultar contenido necesario

```html
<p aria-hidden="true">Precio: 20€</p>
```

**Problema:**  
El lector de pantalla no podrá acceder a información esencial.

---

## aria-expanded

Indica si un elemento **desplegable** está abierto o cerrado.

### ✔️ Buen uso: botón que controla un panel

```html
<button aria-expanded="false" aria-controls="panel1">
  Mostrar detalles
</button>

<div id="panel1" hidden>
  Contenido adicional...
</div>
```

<button aria-expanded="false" aria-controls="panel1-demo" style="padding:8px; border:1px solid #333;">
  Mostrar detalles
</button>
<div id="panel1-demo" hidden style="margin-top:6px;">
  Contenido adicional...
</div>

**Por qué es correcto:**  
El estado refleja si el panel está visible o no.

---

### ❌ Mal uso: usarlo sin relación con un panel

```html
<button aria-expanded="true">Enviar</button>
```

**Problema:**  
No hay nada que expandir. El estado no tiene sentido.

---

## aria-checked

Indica el estado de elementos tipo **checkbox**, **switch** o **radio** cuando no son nativos.

### ✔️ Buen uso: casilla personalizada

```html
<div role="checkbox" aria-checked="false" tabindex="0">
  Acepto las condiciones
</div>
```

<div role="checkbox" aria-checked="false" tabindex="0" style="padding:8px; border:1px solid #333; width:220px;">
  Acepto las condiciones
</div>

**Por qué es correcto:**  
El elemento no es un `<input type="checkbox">`, así que ARIA comunica su estado.

---

### ❌ Mal uso: usarlo en un elemento que no es un control

```html
<p aria-checked="true">Texto cualquiera</p>
```

**Problema:**  
El estado no tiene sentido en un párrafo.

---

## aria-selected

Indica qué elemento está **seleccionado** dentro de un conjunto (listas, pestañas, opciones).

### ✔️ Buen uso: pestañas accesibles

```html
<div role="tablist">
  <button role="tab" aria-selected="true">General</button>
  <button role="tab" aria-selected="false">Accesibilidad</button>
</div>
```

<div role="tablist" style="display:flex; gap:10px; margin-bottom:10px;">
  <button role="tab" aria-selected="true" style="padding:6px; border:2px solid #333;">General</button>
  <button role="tab" aria-selected="false" style="padding:6px; border:1px solid #aaa;">Accesibilidad</button>
</div>

**Por qué es correcto:**  
El lector de pantalla sabe qué pestaña está activa.

---

### ❌ Mal uso: usarlo fuera de un contexto seleccionable

```html
<button aria-selected="true">Enviar</button>
```

**Problema:**  
Un botón no forma parte de un conjunto seleccionable.

---

## Resumen de buenas prácticas

- Usa `aria-disabled` solo cuando no exista un equivalente HTML.  
- Usa `aria-hidden` únicamente para contenido decorativo.
  - no uses `aria-hidden` si un elemento recibe el foco
- Usa `aria-expanded` para controles que abren o cierran paneles.  
- Usa `aria-checked` en controles personalizados.  
- Usa `aria-selected` en listas de selección o pestañas.  


---

