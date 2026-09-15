# Subir la presentación del módulo a Aules

Guía paso a paso para publicar el material (GitHub Pages) y enlazarlo en **Aules (Moodle)**.

> Aules NO almacena HTML con CSS/JS propios: el material web se publica en
> **GitHub Pages** y se enlaza desde Aules mediante un recurso *URL*.
> Reemplaza `TU-CUENTA` y `TU-REPO` por tus datos GitHub o usa las opciones alternativas del final.

---

## Paso 1 · Preparar el repositorio (una sola vez)

En PowerShell, dentro de `VSC/`:

```powershell
git init
git branch -M main
git add .
git status        # comprueba que el índice y la presentación entran, y que el PDF NO entra
git commit -m "Presentación del módulo OPI · portada (200 h · 9 UP)"
```

> Al hacer `git add` puede aparecer el aviso `LF will be replaced by CRLF`. Es normal en Windows; no requiere acción.

## Paso 2 · Crear el repositorio en GitHub

1. Entra en github.com → **New repository**.
2. Nombre: `TU-REPO` (ej.: `opi-presentacion-modulo`).
3. Visibilidad: **Public**.
4. **No** marques ninguna opción de inicialización (no README, no .gitignore) para no duplicar.
5. Conecta el repo local y sube los cambios:

```powershell
git remote add origin https://github.com/TU-CUENTA/TU-REPO.git
git branch -M main
git push -u origin main
```

## Paso 3 · Activar GitHub Pages

1. En GitHub: repo → **Settings** → **Pages** (menú lateral).
2. **Build and deployment** → *Source*: `Deploy from a branch` → rama `main` → carpeta `/ (root)` → **Save**.
3. Espera ~1 minuto. La URL será:

```
https://TU-CUENTA.github.io/TU-REPO/
```

4. Abre esa URL y verifica que se ve igual que al abrir `index.html` en local.

## Paso 4 · Enlazar el material en Aules

1. Entra en tu curso de Aules → activa **Edición** (engranaje superior derecho).
2. En la sección del módulo (haz clic en **+ Añade una actividad o un recurso**).
3. Elige **URL**.
4. Configura el recurso:
   - **Nombre del recurso:** `Presentación del módulo · Ofimática (OPI)`.
   - **URL externa:** `https://TU-CUENTA.github.io/TU-REPO/` (o `/index.html`).
   - **Apariencia:** panel desplegable. Recomendado: *Mostrar en la misma página* (o *nueva ventana* si prefieres que el alumnado mantenga Aules abierto). Añade `?lang=es` si quieres forzar el idioma.
   - **Rol de visualización / restricciones de acceso:** por defecto, visible para todo el alumnado.
   - **Finalización de actividad:** puedes marcarla manualmente cuando el alumnado confirme que ha leído la presentación.
5. **Guardar y mostrará al curso.**

> Alternativa si no quieres enviar a GitHub: crea una página de curso en Aules
> (recurso **Página**) y pega solo el contenido textual; perderás el diseño
> (CSS/JS) y la navegación. La vía recomendada es GitHub Pages.

## Paso 5 · Publicar futuras unidades

Cada UP (UP01…UP09) se generará en su carpeta sobre el mismo sistema. Para actualizar:

```powershell
git add .
git commit -m "Añade UP01 · Mantenimiento de equipos"
git push origin main
```

GitHub Pages se actualiza solo con el push. Los enlaces UP01–UP09 del menú lateral
empezarán a funcionar cuando existan sus `index.html`.

## Verificación final antes de publicar

- [ ] `index.html` abre en local sin errores de consola.
- [ ] Footer exacto: `Material Moodle bilingüe de Vibecoding · HTML generado desde Markdown · CC BY-SA 4.0`.
- [ ] Se ve correcto en móvil (menú lateral con el botón ☰).
- [ ] En GitHub Pages: la página carga con CSS y menú funcionales (las rutas son relativas).
- [ ] El PDF fuente **no** está en el repositorio (`.gitignore`).

## Notas de licencia

- Material web: **CC BY-SA 4.0** (footer y cabeceras de páginas).
- Documento original (PDF): CC BY-NC-SA 4.0. Queda fuera del repositorio para no
  mezclar licencias. Si se referencian imágenes suyas, deben recuperarse,
  redibujarse o sustituirse por recursos de licencia compatible.