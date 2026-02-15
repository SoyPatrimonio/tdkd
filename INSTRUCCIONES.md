# Instrucciones — Proyecto Soy Patrimonio

## Estructura del Proyecto

```
final/
├── assets/img/          ← Imágenes del header/logo (agregar header.png aquí)
├── css/
│   ├── global.css       ← Estilos compartidos (MODIFICAR VARIABLES AQUÍ)
│   ├── inicio.css       ← Estilos de index.html
│   ├── Explorando -ciudad.css ← Estilos de línea de tiempo
│   ├── producion_cientifica.css
│   └── ... (demás páginas)
├── js/
│   ├── global.js        ← Funciones compartidas (menú, partículas, scroll)
│   ├── inicio.js        ← JS de index.html
│   └── ... (demás páginas)
├── imagenes/            ← Imágenes del contenido
├── index.html           ← Página principal
├── producion_cientifica.html
├── Explorando -ciudad.html ← Línea de tiempo
└── ... (demás páginas)
```

## 1. Cambiar el Header (Título por Imagen)

En **cualquier HTML**, busca el comentario `★★★ Cambiar aquí el título por imagen ★★★`:

```html
<!-- ★★★ Cambiar aquí el título por imagen ★★★ -->
<!-- <img src="assets/img/header.png" alt="Soy Patrimonio Logo" class="logo-img"> -->

<div class="logo-text">
    <h1>SOY PATRIMONIO</h1>
    <span>Descubre, Aprende y Protege</span>
</div>
```

**Para usar imagen:**
1. Coloca tu logo en `assets/img/header.png`
2. Descomenta la línea `<img ...>`
3. Comenta o elimina `<div class="logo-text">...</div>`
4. La imagen se adapta automáticamente (máx 180px de ancho, responsive)

## 2. Cambiar Colores y Tipografías

Abre `css/global.css` y modifica las **variables CSS** al inicio:

```css
:root {
    --primary-color: #2c3e50;    /* Color principal (azul oscuro) */
    --secondary-color: #e74c3c;  /* Color de acento (rojo) */
    --accent-color: #3498db;     /* Color secundario (azul) */
    /* ... más variables */
}
```

## 3. Modificar Contenido de Páginas

- **Textos del hero**: Busca `hero-title` y `hero-subtitle` en cada HTML
- **Producción Científica**: En `producion_cientifica.html`, secciones con clase `academic-section`
- **Línea de Tiempo**: En `Explorando -ciudad.html`, cada evento es un `<article class="timeline-event">`

### Agregar un evento a la línea de tiempo:
Copia un bloque y modifica:
```html
<article class="timeline-event" data-year="2025" role="listitem">
    <div class="timeline-marker"><i class="fas fa-star"></i></div>
    <div class="timeline-card">
        <div class="timeline-year-badge">2025 — Nuevo Evento</div>
        <div class="timeline-body">
            <div class="timeline-text">
                <h3>Tu Título</h3>
                <p>Tu descripción.</p>
            </div>
            <div class="timeline-media">
                <img src="imagenes/tu-imagen.jpg" alt="Descripción">
            </div>
        </div>
    </div>
</article>
```

## 4. Agregar Nuevas Páginas

1. Crea el archivo `.html` copiando la estructura de `index.html`
2. Incluye siempre:
   ```html
   <link rel="stylesheet" href="css/global.css">
   <script src="js/global.js"></script>
   ```
3. Agrega tu CSS específico y JS si es necesario

## 5. Footer y Navegación

El **header** y **footer** se repiten en cada página. Para actualizar enlaces:
- Modifica el `<nav class="nav-menu">` en todos los archivos HTML
- Modifica las columnas `<div class="footer-column">` igualmente
