---
layout: default
title: "Ejemplos de atributos ARIA de nombre y descripción"
permalink: /aria-labels
---



Esta página muestra ejemplos prácticos de cómo usar correctamente los atributos ARIA que proporcionan **nombre accesible** y **descripciones adicionales**.  
Incluye casos de buen uso y mal uso para entender cómo afectan a la experiencia con lectores de pantalla.

---

## 🟦 aria-label

`aria-label` **proporciona un nombre accesible explícito**, pero **sobrescribe completamente** el texto visible del elemento.

### ✔️ Buen uso: icono sin texto visible

```html
<button aria-label="Buscar">
  <svg aria-hidden="true">...</svg>
</button>
```

<button aria-label="Buscar" style="padding:8px; border:1px solid #333;">
  🔍
</button>

**Por qué es correcto:**  
El botón no tiene texto visible; `aria-label` aporta el nombre accesible.

---

### ❌ Mal uso: sobrescribir el texto visible

```html
<a href="documento.pdf" aria-label="Abre en nueva ventana">
  Descargar informe anual
</a>
```

<a href="#" aria-label="Abre en nueva ventana" style="color:blue; text-decoration:underline;">
  Descargar informe anual
</a>

**Problema:**  
El lector de pantalla **no leerá “Descargar informe anual”**, sino solo *“Abre en nueva ventana”*.  
Esto destruye el significado del enlace.

### ✔️ Versión correcta

```html
<a aria-label="Descargar informe anual (Abre en ventana nueva)" href="documento.pdf" target="_blank">
  Descargar informe anual
  
</a>
<a href="documento.pdf" target="_blank">
  Descargar informe anual
  <span class="visually-hidden"> abre en nueva ventana)</span>
</a>
```
<a aria-label="Descargar informe anual (Abre en ventana nueva)" href="documento.pdf" target="_blank" style="color:blue; text-decoration:underline;">
  Descargar informe anual
  
</a>
<a href="documento.pdf" target="_blank" style="color:blue; text-decoration:underline;">
  Descargar informe anual
  <span class="visually-hidden"> abre en nueva ventana)</span>


**Por qué es correcto:**  
El texto visible sigue siendo el nombre accesible.  
La información adicional se da visualmente sin interferir con el nombre.

---

## 🟩 aria-labelledby

`aria-labelledby` **apunta a uno o varios elementos existentes** para construir el nombre accesible.  
Es preferible a `aria-label` cuando **ya existe texto visible**.

### ✔️ Buen uso: asociar un campo a su etiqueta

```html
<label id="lbl-email">Correo electrónico</label>
<input type="email" aria-labelledby="lbl-email">
```

<label id="lbl-email">Correo electrónico</label>
<input type="email" aria-labelledby="lbl-email" style="display:block; margin-top:4px;">

**Por qué es correcto:**  
El nombre accesible proviene del texto visible.

---

### ✔️ Buen uso: combinar varios textos

```html
<h2 id="titulo-seccion">Datos personales</h2>
<label id="lbl-nombre">Nombre completo</label>

<input aria-labelledby="titulo-seccion lbl-nombre">
```

**Resultado accesible:**  
El lector de pantalla anuncia:  
**“Datos personales Nombre completo, campo de texto”**

---

### ❌ Mal uso: apuntar a elementos que no existen

```html
<input aria-labelledby="no-existe">
```

**Problema:**  
El campo queda **sin nombre accesible**, lo que lo hace inusable.

---

## 🟨 aria-describedby

`aria-describedby` **no da nombre**, sino **descripción adicional**.  
Se usa para instrucciones, ayudas contextuales o mensajes de error.

### ✔️ Buen uso: ayuda contextual

```html
<label for="pass">Contraseña</label>
<p id="help-pass">Debe tener al menos 8 caracteres.</p>

<input id="pass" type="password" aria-describedby="help-pass">
```

<label for="pass2">Contraseña</label>
<p id="help-pass2">Debe tener al menos 8 caracteres.</p>
<input id="pass2" type="password" aria-describedby="help-pass2" style="display:block; margin-top:4px;">

**Resultado accesible:**  
“Contraseña, campo de texto. Debe tener al menos 8 caracteres.”

---

### ❌ Mal uso: usarlo para sustituir el nombre

```html
<input aria-describedby="texto">
<p id="texto">Nombre completo</p>
```

**Problema:**  
El campo **no tiene nombre**, solo descripción.  
Los lectores de pantalla no lo anuncian correctamente.

---

## 🟧 aria-description

`aria-description` añade **descripción accesible no visible**, pensada para casos donde no quieres mostrar texto en pantalla pero sí aportar contexto adicional.

### ✔️ Buen uso: aclaración accesible sin mostrar texto

```html
<button aria-label="Enviar" aria-description="Envía el formulario y guarda los cambios">
  Enviar
</button>
```

<button aria-label="Enviar" aria-description="Envía el formulario y guarda los cambios" style="padding:8px; border:1px solid #333;">
  Enviar
</button>

**Por qué es correcto:**  
El nombre accesible es “Enviar”.  
La descripción añade contexto útil sin saturar la interfaz.

---

### ❌ Mal uso: usarlo para reemplazar instrucciones visibles

```html
<input aria-label="Nombre" aria-description="Introduce tu nombre completo">
```

**Problema:**  
La descripción debería complementar, no sustituir instrucciones que deberían ser visibles.

---

## 🟪 Otros atributos relacionados

### `title` (no recomendado como nombre accesible)

```html
<button title="Cerrar">✖</button>
```

**Problema:**  
Muchos lectores de pantalla **no usan `title` como nombre**.  
Debe usarse solo como *tooltip*, no como nombre accesible.

---

### `aria-hidden="true"`

Oculta elementos a tecnologías de asistencia.

✔️ Correcto para iconos decorativos  
❌ Incorrecto si contiene información necesaria

```html
<span aria-hidden="true">★</span>
```

---

## 🧭 Resumen de buenas prácticas

- Usa **`aria-label` solo cuando no haya texto visible**.  
- Usa **`aria-labelledby` siempre que puedas**: es la opción preferida.  
- Usa **`aria-describedby` para instrucciones, ayudas y errores**.  
- Usa **`aria-description` para descripciones accesibles no visibles**.  
- No uses `title` como sustituto de un nombre accesible.  
- No ocultes información relevante con `aria-hidden`.

---

