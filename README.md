# Hoja de Vida — Jhon Steeven Romero Nieves

Misma estructura HTML de siempre (semántica, sin `<div>`, todo en
porcentajes), pero con una **identidad visual propia**, distinta a la
versión "editor de código" y a la versión editorial que ya tienes.

## Archivos

| Archivo             | Contenido |
|-----------------------|---------|
| `index.html`          | Estructura del CV con la información de Jhon |
| `css/style.css`        | Estilo nuevo: paleta vino/dorado, tipografía serif + sans |
| `css/normalize.css`    | Reset del navegador (agrégalo si no lo tienes) |
| `media/img/foto-jhon.jpg` | Ruta donde va la foto real de Jhon |
| `README.md`            | Este documento |

## 1. Cambios en esta entrega

- **Se eliminó la sección de Competencias** (tanto del HTML como del CSS: `.competencias`, `.comp-list` y su regla responsive ya no existen).
- **Se eliminó la sección de Experiencia** (HTML `.experience`/`.exp-entry` y las reglas CSS `.experience-list`, `.exp-role`, `.exp-place`, `.exp-desc` ya no existen).
- **Se rediseñó por completo el CSS** para que se vea distinto al tuyo, manteniendo el mismo HTML (mismas clases, mismos `id`) en las secciones que sí quedaron: Información personal, Perfil, Estudios, Idiomas y Habilidades.

## 2. Nueva identidad visual

| | Tu versión (editor de código) | Esta versión |
|---|---|---|
| Concepto | ventana de Mac con barra de título y pestaña `cv.html` | membrete formal, sin la simulación de ventana |
| Tipografía display | Space Grotesk | **Cormorant Garamond** (serif itálica) |
| Tipografía cuerpo | Inter | **Nunito Sans** |
| Tipografía mono | JetBrains Mono | *(no se usa)* |
| Color | tinta azul + verde-azulado + ámbar | **vino (`--burgundy`) + dorado (`--gold`)** |
| Indicadores de nivel | rombos girados 45° (idiomas) y círculos (skills) | **barras rectangulares delgadas**, mismo estilo para ambas secciones |
| Encabezados de sección | `Space Grotesk` sin adorno | serif con una regla dorada debajo, en mayor tamaño |
| Skill tags | píldora con borde | texto simple, sin cápsula, con barra de nivel al lado derecho |

### Un detalle técnico interesante
El HTML **sigue teniendo** `<ul class="window-dots"><li></li>...</ul>` (los
tres puntos de Mac) y `<p class="tab">cv.html</p>`, porque no tocamos la
estructura. Lo que cambia es el CSS:

```css
.window-dots{ display: none; }   /* los tres puntos se ocultan */

.tab{
  font-family: "Cormorant Garamond", serif;
  font-style: italic;
}
.tab::before{ content: "Curriculum · Vitae "; } /* reemplaza el ícono "</>" */
```

Es un buen ejemplo de que el mismo HTML puede verse completamente distinto
solo cambiando el CSS — la meta del ejercicio de separar ambos archivos.

## 3. Todo sigue en porcentajes

Se mantiene la misma disciplina que en las versiones anteriores: `width`,
`padding`, `margin`, `gap`, `font-size` y `border-radius` en `%`. Las
excepciones son las mismas de siempre (`border-width` y `box-shadow`, que
la spec de CSS no admite en `%` bajo ninguna circunstancia) — están
documentadas con más detalle en el README de la versión original si lo
necesitas de nuevo.

`.window` está en `width: 60%` en escritorio y pasa a `92%` en el
`@media (max-width: 620px)`.

## 4. Cómo editar

- Datos de contacto, perfil, estudios, experiencia, idiomas y habilidades: directo en `index.html`, igual que antes.
- Niveles de idioma/skill: clase `on` en cada `<li class="dot">` (con `on` se ve relleno en dorado o vino, sin ella vacío).
- Foto: reemplaza `media/img/foto-jhon.jpg`.
