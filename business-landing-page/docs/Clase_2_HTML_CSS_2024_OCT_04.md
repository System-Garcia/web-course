# Revisión y Continuación del Curso de HTML y CSS

## Introducción

Antes de continuar con los nuevos temas, es fundamental asegurarnos de que todos los conceptos sobre **HTML y CSS** estén claros. **¿Alguien tiene alguna duda?** No queremos avanzar sin resolver cualquier pregunta que haya surgido. Es importante que todos los fundamentos estén bien comprendidos, ya que sobre ellos construiremos el resto del curso.

Ahora, procederemos con un repaso rápido y seguiremos con los nuevos temas para hoy.

---

## 1. Estado Actual del Proyecto

### 1.1. **Repaso del Proyecto Actual**

- **Inspección de elementos**: Utilizaremos las herramientas de desarrollador del navegador (como Chrome DevTools) para analizar la estructura HTML y CSS del proyecto.
- Revisaremos cómo la página está dividida en **contenedores** y **bloques**, observando la jerarquía de elementos y su disposición.
- Analizaremos cómo el CSS afecta visualmente estos elementos: colores, espaciados, tipografía, etc.

### 1.2. **Importancia del Diseño Mobile-First**

El diseño **Mobile-First** consiste en crear el sitio web inicialmente para pantallas pequeñas, y luego adaptarlo a dispositivos de mayor tamaño.

- **Tráfico móvil**: Actualmente, el tráfico web desde dispositivos móviles (smartphones y tablets) representa entre un **55% y 65%** del total.
- **Tráfico desde escritorio**: Los dispositivos de escritorio (PC y laptops) generan entre **35% y 45%** del tráfico web.

#### ¿Por qué Mobile-First?

- **Viewport**: Es necesario configurar el `<meta name="viewport">` para garantizar que el diseño se ajuste adecuadamente a las pantallas móviles.
- **Escalabilidad**: Diseñar para móviles y luego escalar hacia pantallas más grandes permite una experiencia de usuario más fluida y consistente.
  
  **Conceptos clave**:
  - **Media Queries**: Usamos las media queries en CSS para aplicar reglas específicas según el tamaño de la pantalla.

  **Tarea:** Asegurar que el proyecto actual sea **responsive** en dispositivos pequeños usando la metodología Mobile-First.

---

## 2. Flexbox y sus Propiedades CSS

Flexbox es un modelo de diseño en CSS que facilita la disposición de elementos en filas o columnas y su alineación eficiente.

### 2.1. **Explicación General de Flexbox**

- **Unidimensional**: Permite distribuir elementos en una única dirección, ya sea horizontal (filas) o vertical (columnas).

## Reglas del `display: flex`

- Nosotros podemos establecer cuál eje será el principal, ya sea como eje horizontal o vertical.
- Los flex items se ordenarán en la dirección del eje establecido como principal.
- La propiedad `justify-content` manipula los elementos en el eje principal y `align-items` en el eje secundario.

### 2.2. **Justify-content**: Controla la alineación horizontal de los elementos dentro del contenedor.

- `flex-start`: Alinea los elementos al inicio.
- `flex-end`: Alinea los elementos al final.
- `center`: Alinea los elementos en el centro.
- `space-between`: Distribuye los elementos con espacio entre ellos.
- `space-around`: Espacios iguales alrededor de los elementos.

### 2.3. **Align-items**: Controla la alineación vertical dentro del contenedor.

- `flex-start`: Alinea los elementos al principio.
- `flex-end`: Alinea los elementos al final.
- `center`: Centra verticalmente los elementos.
- `stretch`: Estira los elementos para llenar el contenedor.

### 2.4. **Flex-direction**: Define la dirección en la que los elementos se organizan.

- `row`: Los elementos se organizan en una fila.
- `row-reverse`: Fila invertida.
- `column`: Los elementos se organizan en una columna.
- `column-reverse`: Columna invertida.

### 2.5. **Order y Align-self**

- **Order**: Define el orden de los elementos. Por defecto, todos tienen `order: 0`. Puedes cambiar este valor para reorganizar los elementos.
- **Align-self**: Permite alinear individualmente un elemento dentro de su contenedor, ignorando `align-items`.

### 2.6. **Flex-wrap, Flex-flow y Align-content**

- **Flex-wrap**: Controla si los elementos deben mantenerse en una sola línea o dividirse en varias líneas.
  - `nowrap`: Todos los elementos permanecen en una sola línea.
  - `wrap`: Los elementos se envuelven a una nueva línea si es necesario.
  - `wrap-reverse`: Similar a `wrap`, pero en sentido inverso.

- **Flex-flow**: Combinación de `flex-direction` y `flex-wrap` en una sola propiedad.

- **Align-content**: Controla la alineación de varias líneas dentro del contenedor. Solo funciona cuando hay más de una línea.

**Ejercicio práctico:** Usar Flexbox para crear una sección responsive del proyecto, aplicando un diseño Mobile-First.

---

## 3. Introducción a HTML Semántico

### 3.1. **¿Qué es HTML Semántico?**

El **HTML semántico** utiliza etiquetas que describen claramente el contenido, mejorando la accesibilidad y el SEO.

Ejemplos:
- `<header>`: Define la cabecera de una página o sección.
- `<footer>`: Define el pie de página.
- `<article>`: Define un contenido independiente y autocontenido.
- `<section>`: Agrupa contenido relacionado en secciones.

### 3.2. **Diferencias entre `div` y Elementos Semánticos**

- **`div`** es una etiqueta genérica que no aporta significado adicional.
- **Etiquetas semánticas** como `<section>`, `<article>`, y `<aside>` proporcionan contexto y mejoran la legibilidad del código y la accesibilidad.

**Ejercicio práctico:** Reestructurar una página HTML usando etiquetas semánticas para mejorar la claridad.

---

## 4. Selectores, Propiedades y Valores en CSS

### 4.1. **Selectores**:
- **Elementos**: `p { color: blue; }`
- **Clases**: `.mi-clase { font-size: 16px; }`
- **ID**: `#mi-id { background-color: yellow; }`
- **Combinados**: `.contenedor p { margin: 10px; }`
- **Pseudo-clases**: `a:hover { color: red; }`

### 4.2. **Propiedades**:
- **color**, **background-color**, **font-size**, **margin**, **padding**, **border**.

### 4.3. **Valores**:
- Colores (`red`, `#ff0000`, `rgb(255, 0, 0)`), unidades (`px`, `%`, `em`), palabras clave (`center`, `flex`).

**Ejercicio**: Crear selectores y aplicar distintas propiedades y valores.

---

## 5. Metodología BEM (Block, Element, Modifier)

### 5.1. **¿Qué es BEM?** X

BEM es una convención para nombrar clases en CSS que facilita la legibilidad y mantenibilidad del código. Divide las clases en:
- **Bloques (`.block`)**: Componente principal.
- **Elementos (`.block__element`)**: Partes del bloque.
- **Modificadores (`.block--modifier`)**: Variaciones del bloque o elemento.

**Ejercicio práctico:** Aplicar la metodología BEM a una sección del proyecto para mejorar la estructura del CSS.
```html 
<div class="profile-card">
  <div class="profile-card__avatar">
    <img src="avatar.jpg" alt="User Avatar">
  </div>
  <div class="profile-card__info">
    <h2 class="profile-card__name">John Doe</h2>
    <p class="profile-card__bio">Web developer with 5 years of experience in front-end development.</p>
  </div>
  <button class="profile-card__button profile-card__button--primary">Follow</button>
  <button class="profile-card__button profile-card__button--secondary">Message</button>
</div>
```
---

## 6. Próxima Parte: Git

En la próxima clase, introduciremos **Git**, una herramienta fundamental de control de versiones.

### Lo que veremos:

- **Inicializar un repositorio**: `git init`.
- **Comandos básicos**: `git add`, `git commit`, `git push`.
- **Trabajo colaborativo**: Clonar repositorios y trabajar en equipo usando Git y GitHub.

---

## Notas Finales

1. **Mobile-First**: Prioriza siempre el diseño para pantallas pequeñas, escalando hacia dispositivos más grandes con media queries.
2. **HTML Semántico y BEM**: Son buenas prácticas que mejorarán la estructura, accesibilidad y SEO de tus proyectos, haciéndolos más fáciles de mantener.

Recuerda que estos conceptos son claves para cualquier desarrollo moderno y profesional de sitios web.