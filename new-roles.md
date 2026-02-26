---
layout: default
title: "Nuevos roles en ARIA 1.2"
permalink: /new-roles
---

# Página de ejemplo: Nuevos roles en ARIA 1.2

ARIA 1.2 introdujo nuevos roles semánticos pensados para mejorar la accesibilidad del contenido textual, especialmente en documentos, editores enriquecidos y contextos donde se generan estructuras dinámicas.

Estos roles permiten que lectores de pantalla interpreten correctamente elementos como texto destacado, superíndices, sugerencias de edición o anotaciones.

---

## role="caption"

Representa el título o leyenda asociada a una tabla, figura o bloque de contenido.

### ✔️ Buen uso: leyenda de una tabla

```html
<div role="table">
  <div role="caption">Ventas trimestrales 2025</div>
  <div role="row">
    <span role="cell">Q1</span>
    <span role="cell">120</span>
  </div>
</div>
```

<div role="table" style="border:1px solid #ccc; padding:10px; margin-bottom:10px;">
  <div role="caption" style="font-weight:bold; margin-bottom:6px;">Ventas trimestrales 2025</div>
  <div role="row">
    <span role="cell" style="display:inline-block; width:50px;">Q1</span>
    <span role="cell">120</span>
  </div>
</div>

**Por qué es correcto:**  
El rol `caption` comunica a tecnologías de asistencia que este texto describe la tabla.

---

### ❌ Mal uso: usarlo como título visual sin relación con un elemento

```html
<p role="caption">Título bonito</p>
```

**Problema:**  
No describe ninguna tabla o figura. El rol pierde sentido.

---

## role="strong"

Indica énfasis fuerte, equivalente semántico a `<strong>`.

### ✔️ Buen uso: enfatizar una advertencia

```html
<p>Este proceso es <span role="strong">irreversible</span>.</p>
```

<p>Este proceso es <span role="strong" style="font-weight:bold;">irreversible</span>.</p>

**Por qué es correcto:**  
El lector de pantalla anunciará el énfasis.

---

### ❌ Mal uso: usarlo para dar estilo visual sin intención semántica

```html
<p><span role="strong">Rojo</span> es mi color favorito.</p>
```

**Problema:**  
No hay énfasis real; solo se usa para estilo.

---

## role="subscript" y role="superscript"

Equivalentes semánticos a `<sub>` y `<sup>`.  
Útiles en editores donde no se puede usar HTML nativo.

### ✔️ Buen uso: fórmulas químicas y matemáticas

```html
<p>La fórmula del agua es H<span role="subscript">2</span>O.</p>
<p>Área = πr<span role="superscript">2</span></p>
```

<p>La fórmula del agua es H<span role="subscript" style="font-size:0.8em; vertical-align:sub;">2</span>O.</p>
<p>Área = πr<span role="superscript" style="font-size:0.8em; vertical-align:super;">2</span></p>

**Por qué es correcto:**  
Los lectores de pantalla anuncian “subíndice” o “superíndice”.

---

### ❌ Mal uso: usarlo para bajar o subir texto sin significado semántico

```html
<p><span role="subscript">hola</span> mundo</p>
```

**Problema:**  
No representa un subíndice real.

---

## role="mark"

Indica texto resaltado o marcado, equivalente a `<mark>`.

### ✔️ Buen uso: resaltar un fragmento importante

```html
<p>Este es un dato <span role="mark">muy relevante</span> para el informe.</p>
```

<p>Este es un dato <span role="mark" style="background:yellow;">muy relevante</span> para el informe.</p>

**Por qué es correcto:**  
El lector de pantalla anuncia que el texto está marcado.

---

### ❌ Mal uso: usarlo como sustituto de un color visual sin intención semántica

```html
<p><span role="mark">Azul</span> es mi color favorito.</p>
```

**Problema:**  
No hay “marcado” semántico.

---

## role="suggestion"

Representa una sugerencia de edición, similar a los cambios propuestos en Google Docs o Word.

### ✔️ Buen uso: sugerencia de reemplazo

```html
<p>El informe es <span role="suggestion">excelente</span>.</p>
```

<p>El informe es <span role="suggestion" style="background:#d0f0ff; border-bottom:1px dashed #00f;">excelente</span>.</p>

**Por qué es correcto:**  
El lector de pantalla anuncia que es una sugerencia, no texto definitivo.

---

### ❌ Mal uso: usarlo como estilo visual sin intención editorial

```html
<p><span role="suggestion">Hola</span> mundo</p>
```

**Problema:**  
No representa una sugerencia real.

---

## Elementos relacionados: `<ins>` y `<del>`

Aunque no son roles ARIA, son fundamentales para accesibilidad en documentos con cambios.

### ✔️ Buen uso: indicar texto añadido y eliminado

```html
<p>Se ha <del>cancelado</del> <ins>reprogramado</ins> el evento.</p>
```

<p>Se ha <del style="color:red;">cancelado</del> <ins style="color:green;">reprogramado</ins> el evento.</p>

**Por qué es correcto:**  
Los lectores de pantalla anuncian “eliminado” y “insertado”.

---

### ❌ Mal uso: usarlos solo para estilo visual

```html
<p><del>Rojo</del> es mi color favorito.</p>
```

**Problema:**  
No representa un cambio editorial.

---

## Resumen de buenas prácticas

- Usa `caption` solo para describir tablas o figuras.  
- Usa `strong` para énfasis real, no para estilo.  
- Usa `subscript` y `superscript` para notación científica o matemática.  
- Usa `mark` para resaltar información importante.  
- Usa `suggestion` para cambios propuestos en editores.  
- Usa `<ins>` y `<del>` para cambios reales en documentos.  
- Evita usar estos roles para fines puramente visuales.

---
