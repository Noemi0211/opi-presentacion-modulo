# AGENTS.md — Proyecto OPI · Presentación del módulo

Memoria permanente del proyecto **Ofimática (OPI)** · CFGS Documentación y Administración Sanitarias · Curso 2026-2027.

## Objetivo general

Transformar el documento oficial `Resumen de la programación del módulo OPI.pdf` en una experiencia de **bienvenida al módulo** en formato web (Markdown fuente + HTML final), con la misma línea visual que el resto del proyecto «Apuntes OPI».

- Módulo: **Ofimática (OPI)** · CFGS Documentación y Administración Sanitarias · **200 horas**.
- Profesora: Noemí Celaya Mingot · n.celayamingot@edu.gva.es.
- Destino final: **GitHub Pages** · acceso desde **Moodle/Aules** · mantenimiento desde **Markdown**.
- La presentación NO es una copia del documento oficial: transforma la información en una guía motivadora (qué es el módulo, qué se aprende, organización, unidades, evaluación, competencias, herramientas y consejos).
- Contenidos de unidades (UP01–UP09) se generarán en fases posteriores reutilizando este sistema.

## Arquitectura del proyecto

```
VSC/
├── AGENTS.md                     # Este archivo · memoria permanente
├── .gitignore                    # Excluye el PDF fuente (BY-NC-SA) y temporales
├── index.md                      # Presentación del módulo (fuente Markdown)
├── index.html                    # Presentación del módulo (HTML final)
├── cuestionarios/
│   └── 01-cuestionario-presentacion.gift    # Banco GIFT del quiz inicial (10 preguntas)
├── docs/                         # Documentación de proceso (reservado)
│   ├── instrucciones-aules.md    # Publicación + enlace del material en Aules
│   └── cuestionario-inicial-aules.md        # Importación y ajustes del quiz inicial
├── html/                         # Salidas HTML intermedias (reservado)
├── css/estilos.css               # CSS único y compartido de TODO el curso
├── js/navegacion.js              # Navegación compartida (menú, scroll-spy, TOC, volver arriba)
├── images/                       # Imágenes validadas del proyecto (raíz)
├── inventario-imagenes/
│   └── inventario-imagenes.md    # Catálogo de imágenes sugeridas
├── assets/                       # Recursos auxiliares (reservado)
├── templates/
│   └── plantilla-base.html       # Plantilla reutilizable para UP01–UP09
└── output/                       # Salidas de procesamiento (reservado)
```

Previsión de crecimiento (fases futuras): cada unidad `UP01/ … UP09/` contendrá su propio `index.md`, `index.html`, `inventario-imagenes.md` e `images/`, sobre el mismo `css/estilos.css`, `js/navegacion.js` y `templates/plantilla-base.html`.

## Diseño visual aprobado

Reutilización EXACTA del sistema de diseño del proyecto «Apuntes OPI» (`Hardware/Apuntes 26-27`). No modificar los estilos base sin permiso.

- Paleta: `#1A1F2E` (tinta) · `#4ECCA3` (acento) · `#F7F4EF` (fondo) · `#FFFFFF` (tarjetas) · `#667085` (texto secundario).
- Tipografías (Google Fonts): **Syne** (títulos) · **DM Sans** (cuerpo).
- Cabecera superior fija (`.header`), menú lateral fijo (`.sidebar`), contenido con scroll-spy, TOC automático, responsive ≤900px y accesible.
- Footer EXACTO en todas las páginas:
  `Material Moodle bilingüe de Vibecoding · HTML generado desde Markdown · CC BY-SA 4.0`
- Componentes base: `.hero`, `.card-grid/.card/.card__icon`, `.callout` (`--key --health --example --summary --reflect`), `.table-wrap`, `.image-placeholder`, `.timeline`, `.steps/.step`, `.toc`, `.page-nav`, `.ce-list`.
- Componentes propios de la presentación del módulo (AÑADIDOS al final de `css/estilos.css`, reutilizables por las unidades): `.stat`, `.weight-badge`, `.hbar` (barras de horas), `.eval-card`, `.up-chip`, `.tool-grid`, `.faq` (`details`), `.btn` (CTA).
- Logo del curso: recuadro «OP» (Ofimática · Presentación). Idiomas de las páginas de UP conservarán el mismo patrón.

## Tareas completadas

Cronológico:

1. **2026-09-15 · Extracción de fuentes.** Texto extraído de `Resumen de la programación del módulo OPI.pdf` (pdf-parse v1.1.1, Node 24) y leído el `PROMPT VSC PRES OPI.docx`.
2. **2026-09-15 · Estructura de carpetas.** Creados `docs/`, `html/`, `css/`, `js/`, `images/`, `inventario-imagenes/`, `assets/`, `templates/`, `output/` (con `.gitkeep`).
3. **2026-09-15 · AGENTS.md.** Memoria del proyecto creada (este archivo).
4. **2026-09-15 · CSS y JS compartidos.** `css/estilos.css` y `js/navegacion.js` creados a partir del sistema «Apuntes OPI», con componentes adicionales para la presentación.
5. **2026-09-15 · Plantilla reutilizable.** `templates/plantilla-base.html` preparada para UP01–UP09.
6. **2026-09-15 · Presentación del módulo.** `index.md` (fuente) y `index.html` (final) generados con las 10 secciones de la experiencia de bienvenida.
7. **2026-09-15 · Inventario de imágenes.** `inventario-imagenes/inventario-imagenes.md` con sugerencias y marcadores.
8. **2026-09-15 · Verificación.** Estructura de etiquetas balanceada (script Node), rutas `css/` y `js/` correctas desde el raíz, footer exacto presente, marcas `<!-- IMAGEN SUGERIDA -->` y `.image-placeholder` en su sitio. **FASE 1 (presentación) COMPLETADA.**
9. **2026-09-15 · Rúbricas completas.** Añadida la sección «Rúbricas de evaluación» (índice, `index.md` e `index.html`) con las tres rúbricas generales del documento oficial transcritas enteras (23 criterios × 4 niveles), la tabla de pesos de evidencias y la guía de lectura. Nuevos componentes CSS `.rubric`, `.rubric__head`, `.rubric__levels` y niveles coloreados `.c-10/.c-7/.c-4/.c-1` (verde/azul/ámbar/rojo). Enlace `#rubricas` añadido al menú lateral y TOC automático.
10. **2026-09-15 · Lista para publicar en GitHub Pages.** Creado `.gitignore` (excluye el PDF fuente, licencia BY-NC-SA) y `docs/instrucciones-aules.md` (pasos exactos de repositorio, GitHub Pages y enlazado en Aules). Repositorio git inicializado (rama `main`) y **commit inicial realizado: `54df32d`**. Pendiente de usuario: crear repo remoto, push y activar GitHub Pages.
11. **2026-09-15 · Publicación.** Repositorio público creado: `Noemi0211/opi-presentacion-modulo` (remote `origin`), push realizado y **GitHub Pages activado**. URL: `https://noemi0211.github.io/opi-presentacion-modulo/` (verificada HTTP 200 con la portada cargando). Pendiente de usuario: enlazar el recurso URL en Aules (ver `docs/instrucciones-aules.md`, paso 4).
12. **2026-09-15 · Cuestionario inicial.** Creado `cuestionarios/01-cuestionario-presentacion.gift` (10 preguntas tipo test × 4 opciones, 1 correcta; categoría `OFI/OPI/PRES/01-presentacion-modulo`; UTF-8 sin BOM, validado por script) y `docs/cuestionario-inicial-aules.md` (importación, montaje del quiz y ajustes: intentos ilimitados antes del cierre, mejor nota en el libro, revisión libre tras el cierre; la fecha de finalización la pone el usuario en la plataforma).
13. **2026-09-15 · «Siguiente» → cuestionario.** El `page-nav` final de la presentación apunta ahora al cuestionario inicial en Aules (`https://aules.edu.gva.es/fp/mod/quiz/view.php?id=11231945`) en lugar de la UP01 (índice e `index.md` actualizados). El enlace a la UP01 seguirá pendiente hasta generar su contenido.
14. **2026-09-19 · Primera imagen validada.** Sustituido en `index.html` el marcador `<!-- IMAGEN SUGERIDA: portada-bienvenida -->` / `.image-placeholder--hero` por la imagen definitiva `<figure class="image-hero"><img src="images/opi-portada-bienvenida.jpeg" …>`. Imagen propia de la autora renombrada a la convención `opi-portada-bienvenida.jpeg`; inventario actualizado con el estado VALIDADA.

## Tareas pendientes

- [ ] Validar imágenes definitivas y sustituir los marcadores `<!-- IMAGEN SUGERIDA -->` / `.image-placeholder`.
- [ ] Generar contenido de las unidades UP01 → UP09 (fases posteriores, una UP por fase).
- [ ] Conectar la navegación de la presentación con las páginas de las UP cuando se publiquen (el `page-nav` «Siguiente» de la portada apunta al cuestionario inicial en Aules; cuando exista UP01, decidir si el segundo enlace de la barra pasa a apuntarla).
- [ ] Decidir e incorporar MC/ADR para el bilingüismo es/val del material (pendiente).

## Estado actual para retomar (2026-09-15)

- GitHub Pages activo y verificado: `https://noemi0211.github.io/opi-presentacion-modulo/`.
- En Aules: el recurso URL de la presentación y el **Cuestionario inicial** (id `11231945`) ya están creados por el usuario (importaciones y ajustes según `docs/cuestionario-inicial-aules.md`).
- Repositorio `Noemi0211/opi-presentacion-modulo` · rama `main` · remote `origin` · cada cambio se commitea y se hace push.
- Acuerdo de trabajo: añadir una entrada cronológica en «Tareas completadas» por cada cambio; al retomar, leer este archivo y, si hay que continuar una fase, revisar también `docs/` y las guías de Aules.

## Decisiones importantes

- **Idioma de redacción:** castellano, coherente con el proyecto «Apuntes OPI» (el documento oficial está en valenciano; los títulos de las UP se traducen al castellano).
- **Fidelidad visual:** se COPIA el CSS/JS del proyecto «Apuntes OPI» para mantener la línea visual EXACTA; solo se AÑADEN componentes nuevos para la portada (documentados en `css/estilos.css`).
- **No incrustar imágenes del PDF:** se registran sugerencias en el inventario y se dejan marcadores visuales hasta validar imágenes con licencia compatible (CC BY-SA 4.0 / dominio público).
- **Contenido transformado, no copiado:** la presentación reescribe la programación didáctica en un lenguaje motivador y visual, conservando todos los datos oficiales (horas, pesos, RA, temporización).
- **Horas oficiales por UP** (aula): UP01 20 · UP02 45 · UP03 10 · UP04 35 · UP05 30 · UP06 12 aula + 18 dual · UP07 10 · UP08 10 · UP09 10 = 200 h.
- **Pesos de la nota final:** RA1 9% · RA2 25% · RA3 9% · RA4 15% · RA5 15% · RA6 15% · RA7 3% · RA8 6% · RA9 3%.
- **Mecanografía (RA2):** requisito imprescindible 200 ppm y ≤1 errada/min en la evaluación final; pulsaciones netas = PPM − (errores × 5).

## Inventario de imágenes

Resumen: el inventario completo está en `inventario-imagenes/inventario-imagenes.md` (9 imágenes conceptuales sugeridas para las secciones de la presentación). En el HTML solo hay marcadores `<!-- IMAGEN SUGERIDA -->` y `.image-placeholder`, nunca imágenes incrustadas.

## Próximos pasos

Fase recomendada: **generación de UP01 · Mantenimiento básico de equipos, aplicaciones y red** (20 h · RA1 · 1.ª evaluación), reutilizando `templates/plantilla-base.html`, `css/estilos.css` y `js/navegacion.js`. Detener la generación al finalizar cada fase y esperar instrucciones.