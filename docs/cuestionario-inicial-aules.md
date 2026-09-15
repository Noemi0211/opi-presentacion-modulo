# Cuestionario inicial · Presentación del módulo OPI

Banco GIFT con **10 preguntas tipo test (4 opciones, 1 correcta)** sobre los contenidos de
la presentación del módulo: horas, unidades, evaluación, rúbricas y mecanografía.

- Fichero: `cuestionarios/01-cuestionario-presentacion.gift`
- Categoría que creará en el banco: `OFI/OPI/PRES/01-presentacion-modulo`
- Caracteres: **UTF-8 sin BOM** (importante para que las tildes se vean bien en Aules).

---

## Paso 1 · Importar las preguntas al banco

1. Aules: curso del módulo → **More** (⋮) → **Administración del curso** → ajustes
   desplegable → **Banco de preguntas** → pestaña **Importar**.
2. Formato: **Formato GIFT**.
3. Sube el fichero `01-cuestionario-presentacion.gift` (lo tienes local en `cuestionarios/`).
4. En **Importar categorías**: elige *La categoría actual va al fichero* (o *Desde el
   fichero* si prefieres respetar `$CATEGORY`). Recomendado: *Desde el fichero* → creará
   `OFI/OPI/PRES/01-presentacion-modulo` con las 10 preguntas.
5. **Importar**: debe confirmar "10 preguntas importadas". Las revisas en **Banco de
   preguntas** (no te olvides de pulsar el selector de categoría para mirar la correcta).

## Paso 2 · Crear el cuestionario

1. **Añade una actividad o un recurso** → **Cuestionario**.
2. **Nombre**: `Cuestionario inicial · Presentación del módulo OPI`.
3. **Descripción** (opcional): *"Responde a estas 10 preguntas sobre el módulo. Puedes
   repetirlo tantas veces como quieras hasta la fecha de cierre; se contará tu mejor
   resultado. Cuando cierre el plazo, sigue disponible en modo consulta."*

## Paso 3 · Añadir las preguntas

1. Botón de contenido → **Añadir una pregunta** → **desde el banco de preguntas**.
2. Categoría `OFI/OPI/PRES/01-presentacion-modulo` → **Añadir todas** (10 preguntas) → **Añadir pregunta seleccionada al cuestionario**.

## Paso 4 · Configuración para tus requisitos

En **Editar cuestionario** → **Administración del cuestionario** → **Editar ajustes**:

| Ajuste | Valor indicado | Para qué sirve |
|---|---|---|
| **Intentos permitidos** | *Il-limitado* (o un número alto, ej. 20) | Que pueda repetir tantas veces como quiera **antes** del cierre (hasta la fecha de finalización). |
| **Método de calificación** | *Calificación media* **NO** → elige **Nota más alta** | Que el libro de calificaciones guarde **el mejor resultado** obtenido. |
| **Tiempo límite** | *Sin límite* (desactivado) | Permite realizarlo sin presión; no bloquea la calidad del intento. |
| **Fecha de apertura / cierre** | Las configuras **manualmente en la plataforma** cuando quieras (deja el cierre vacío o pon tu fecha de finalización) | Controlas el plazo desde la propia actividad. |
| **El cuestionario solo permite 1 intento cada nº de horas** | Vacío (ilimitado) | Sin esperas entre intentos. |
| **Revisar opciones · Después de cerrar el cuestionario** | Marca: *El intento*, *Si la respuesta es correcta*, *Puntuaciones*, *Retroalimentación específica*, *Retroalimentación general* | Que al terminar el plazo el alumnado **pueda revisar siempre que quiera** sus respuestas, aciertos y explicaciones. |
| **Con comportamientos de pregunta** | *Retroalimentación diferida* (habilitada) | Entrega la corrección al acabar cada intento (la típica de recapitulación). |
| **Barajar dentro de las preguntas** | Sí (marcado) | Las opciones salen en orden distinto en cada intento. |
| **Presentar una pregunta por página** | Sí | Más claro para lectura en móvil. |

> Nota: cuando se cierra el cuestionario, Moodle impide **iniciar** intentos nuevos.
> Por eso se activan las opciones de revisión *en y después del cierre*: así el
> alumnado puede seguir abriendo el cuestionario y consultar sus intentos anteriores,
> sus aciertos y la retroalimentación las veces que quiera, sin que afecte a la nota.

**Resumen del comportamiento final:**
- Antes del cierre: intentos ilimitados, mejor nota en el libro de calificaciones.
- Después del cierre: acceso solo-consulta a intentos ya realizados (revisión libre).
- La fecha de finalización la introduces tú manualmente en *Editar ajustes*.

## Paso 5 · Verificación

- [ ] El banco muestra las 10 preguntas en `OFI/OPI/PRES/01-presentacion-modulo`.
- [ ] El cuestionario tiene las 10 preguntas añadidas.
- [ ] Método de calificación: **Nota más alta**.
- [ ] Intentos: ilimitados antes del cierre.
- [ ] Revisión activa para *Después de cerrar el cuestionario*.
- [ ] Prueba previa (o vista previa): las tildes y los símbolos se ven correctamente
      (confirma que el fichero estaba en UTF-8 sin BOM).