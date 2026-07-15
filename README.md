# 📄 Hoja de Vida — Jhon Steeven Romero Nieves

Proyecto desarrollado con **HTML5** y **CSS3**, utilizando únicamente etiquetas semánticas y hojas de estilo externas. La estructura del documento evita el uso de etiquetas `<div>` y emplea principalmente porcentajes para lograr un diseño adaptable.

La interfaz está inspirada en una ventana de un editor de código, pero con una identidad visual propia basada en una paleta de colores morado y turquesa, efectos de transparencia y una barra superior personalizada.

---

# 📁 Estructura del proyecto

| Archivo / Carpeta | Descripción |
|-------------------|-------------|
| `index.html` | Estructura semántica de la hoja de vida. |
| `style/style.css` | Hoja de estilos principal del proyecto. |
| `style/normalize.css` | Reinicio de estilos del navegador. |
| `media/img/image.png` | Fotografía de perfil. |
| `media/img/fondop.jpg` | Imagen de fondo de la página. |
| `README.md` | Documentación del proyecto. |

---

# 🎨 Diseño

El proyecto utiliza un estilo moderno basado en el efecto **Glassmorphism**, combinando transparencia, desenfoque y una paleta de colores personalizada.

### Características visuales

- Fondo con imagen fija.
- Tarjeta principal con transparencia.
- Efecto Blur mediante `backdrop-filter`.
- Barra superior personalizada.
- Animaciones de entrada.
- Bordes suaves.
- Diseño responsive.

### Tipografías

- **Cormorant Garamond**
- **Nunito Sans**

### Paleta de colores

Las variables principales se encuentran en `:root`.

| Variable | Uso |
|----------|-----|
| `--ink` | Texto oscuro |
| `--paper` | Fondo claro |
| `--paper-dim` | Fondo secundario |
| `--burgundy` | Color principal (morado) |
| `--burgundy-dark` | Morado oscuro |
| `--gold` | Color de acento (turquesa) |
| `--line` | Líneas |
| `--line-soft` | Bordes suaves |

---

# 🪟 Barra superior personalizada

Aunque el HTML conserva la estructura de una ventana de editor:

```html
<ul class="window-dots">
    <li></li>
    <li></li>
    <li></li>
</ul>

<p class="tab">cv.html</p>
```

El CSS cambia completamente su apariencia:

```css
.window-dots{
    display: none;
}

.tab{
    font-family: "Cormorant Garamond", serif;
    font-style: italic;
}

.tab::before{
    content: "Curriculum · Vitae ";
    color: var(--gold);
    font-style: normal;
    font-size: 78%;
    letter-spacing: 0.14em;
    text-transform: uppercase;
}
```

De esta manera se ocultan los botones de la ventana y se agrega automáticamente el texto **"Curriculum · Vitae"** antes del nombre del archivo **cv.html**, conservando el mismo HTML pero cambiando completamente su apariencia mediante CSS.

---

# 📚 Secciones de la hoja de vida

El documento está organizado en las siguientes secciones:

- Información personal
- Perfil profesional
- Estudios
- Idiomas
- Habilidades

Todas las secciones utilizan etiquetas semánticas de HTML5 como:

- `<header>`
- `<main>`
- `<section>`
- `<article>`
- `<figure>`
- `<address>`
- `<footer>`

---

# 💻 Tecnologías utilizadas

- HTML5
- CSS3
- Normalize.css
- Google Fonts
- Flexbox
- CSS Grid

No se utilizó JavaScript.

---

# ✨ Características del CSS

El proyecto implementa diversas herramientas propias de CSS3:

- Variables CSS (`:root`).
- Flexbox.
- CSS Grid.
- Glassmorphism.
- Animaciones mediante `@keyframes`.
- `scroll-behavior`.
- `backdrop-filter`.
- Media Queries.
- Estilos para impresión (`@media print`).
- Compatibilidad con usuarios que prefieren reducir animaciones (`prefers-reduced-motion`).

---

# 📱 Diseño Responsive

El proyecto adapta automáticamente su distribución cuando el ancho de la pantalla es menor a **620px**.

Los principales cambios son:

- La tarjeta principal aumenta su ancho.
- La información personal se organiza verticalmente.
- Las columnas de estudios e idiomas pasan a una sola columna.
- El pie de página cambia a distribución vertical.

---

# ✏️ Personalización

## Modificar la información

Toda la información del currículum puede editarse desde:

```text
index.html
```

Allí se pueden modificar:

- Nombre
- Apellidos
- Correo electrónico
- Teléfono
- Ciudad
- Perfil profesional
- Estudios
- Idiomas
- Habilidades

---

## Cambiar la fotografía

Reemplazar el archivo:

```text
media/img/image.png
```

---

## Cambiar el fondo

Reemplazar el archivo:

```text
media/img/fondop.jpg
```

---

## Modificar los colores

Editar las variables ubicadas al inicio de:

```text
style/style.css
```

Dentro del bloque:

```css
:root{
    --ink: ...;
    --paper: ...;
    --paper-dim: ...;
    --burgundy: ...;
    --burgundy-dark: ...;
    --gold: ...;
    --line: ...;
    --line-soft: ...;
}
```

Al modificar estas variables se actualiza automáticamente toda la apariencia del sitio.

---

# 👨‍💻 Autor

**Jhon Steeven Romero Nieves**

Tecnólogo en Desarrollo de Sistemas Informáticos.

Proyecto realizado como práctica académica para fortalecer el uso de HTML5 semántico, CSS3, Flexbox, Grid, diseño responsive y organización de proyectos web mediante hojas de estilo externas.
