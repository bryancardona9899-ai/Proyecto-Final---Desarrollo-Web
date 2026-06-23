# Proyecto FInal | DESARROLLO WEB HTML Y CSS

Este proyecto consiste en una réplica estática y visualmente fiel de la página principal de Apple Latinoamérica, desarrollada exclusivamente con tecnologías nativas HTML5 y CSS3

## 1. Nombre del Proyecto
**Réplica visual de la landing page de Apple**  

## 2. Secciones Replicadas
- **Barra de navegación superior:** Menú horizontal oscuro con distribución usando Flexbox.
- **Hero principal oscuro:** Sección dedicada a la WWDC26 utilizando fondos oscuros y distribución centrada.
- **Sección destacada de teléfono:** Bloque claro promocional de un smartphone simulado.
- **Sección destacada de laptop:** Bloque degradado claro enfocado en computación portátil.
- **Cuadrícula de productos:** Sección grid responsiva de dos columnas (escritorio) que se transforma en una columna (móvil).
- **Banner promocional de entretenimiento:** Sección de estilo cinematográfico simulando Apple TV usando posicionamiento de CSS.
- **Notas legales:** Texto informativo pequeño con tipografía grisácea.
- **Footer estructurado:** Columnas organizadas con mapas de enlaces adaptables.

## 3. Conceptos Aplicados

### HTML5 Semántico
Se implementaron etiquetas estructurales clave para asegurar una arquitectura limpia y accesible:
* **Estructura jerárquica:** Uso estricto de etiquetas de bloque principales como `<header>`, `<main>`, `<section>`, `<article>` y `<footer>`.
* **Etiquetas multimedia:** Incorporación de la etiqueta `<video>` con atributos de optimización (`autoplay`, `loop`, `muted`, `playsinline`) para la sección Hero.
* **Agrupamiento estructurado:** Uso de listas no ordenadas (`<ul>` y `<li>`) para la gestión limpia de los enlaces del menú del footer.
* **Componentes:** Inclusión de imágenes vectoriales y recursos en formato `.jpg`/`.png` referenciados mediante rutas relativas organizadas.

## 4. Conceptos CSS Utilizados
El diseño visual se rige bajo los fundamentos del **Apple Design System**:
* **Variables y Arquitectura:** Normalización de la paleta de colores institucionales para textos primarios, para acentos azules y para fondos.
* **Tipografía del Sistema:** Uso de fuentes tipográficas nativas con configuraciones precisas de `letter-spacing` negativo y `line-height`.
* **Posicionamiento Avanzado:** Uso de propiedades `position: relative`, `position: absolute` y manejo de capas con `z-index` para superponer textos y botones sobre videos y carruseles.
* **Propiedades de Desbordamiento:** Uso de `overflow: hidden` para evitar el comportamiento de scroll no deseado, y `overflow-x: auto` junto con `scrollbar-width: none` para rieles horizontales limpios.

### 5. Flexbox
Utilizado primordialmente en:
- La **barra de navegación superior** para alinear el logotipo ficticio, los enlaces de categorías y la barra de búsqueda de forma horizontal (`display: flex`, `justify-content: space-between`, `align-items: center`).
- Los **grupos de botones de acción (CTA)** garantizando un espaciado uniforme (`gap`).

### 6. CSS Grid
Implementado directamente en:
- La **cuadrícula de productos**, definiendo estructuralmente `grid-template-columns: repeat(2, 1fr)` en resoluciones de escritorio para asegurar la perfecta simetría de las tarjetas promocionales.
- El **footer**, organizando los menús corporativos en 6 columnas horizontales balanceadas.

### 7. Responsive Design
A través de la directiva `@media (max-width: 768px)`, la página web se reestructura dinámicamente eliminando cualquier desbordamiento horizontal (`overflow-x: hidden`):
- La cuadrícula de productos pasa automáticamente de 2 columnas a **1 columna completa** optimizando la lectura táctil.
- Las columnas informativas del footer se contraen a 2 columnas verticales legibles para mitigar colapsos de texto.

## 8. Dificultades Encontradas
- * **Superposición en el Hero de Video:** Uno de los mayores retos fue lograr que el contenido de texto y los botones flotaran con precisión por encima del video en reproducción sin romper el flujo semántico.
- * **Optimización Escrita del Footer:** Replicar la sutileza del pie de página oficial de Apple requirió un ajuste minucioso. El texto tendía a verse tosco o sobredimensionado.
- * **Comportamiento del Carrusel:** Conseguir que los slides laterales se vieran sutilmente cortados en la periferia de la pantalla (emulando un carrusel infinito en carátulas de Apple TV+) requirió un manejo avanzado de contenedores con scroll horizontal nativo y anchos estáticos compartidos.
- * **Cuadricula de Productos:** Fue complicado alinear cada imagen dentro de los cuadros designados para cada uno y buscar el orden correcto, tambien como la posicion, color y visión correcta de cada producto. Cada ajuste llevo demasiado tiempo porque no se veian como se esperaba.
- * **Ajuste de Pantalla:** Fue complicado evitar que la página colapsara o se viera de manera erronea al cambiar el dispositivo de visualización
