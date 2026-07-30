# IANEWS — Resumen diario de IA

Este repo genera cada mañana un resumen de noticias de IA en español, pensado
para un lector sin formación técnica (comercial, estudiante de dietética).

## Qué hacer en cada ejecución de la rutina

1. Investigar las noticias de IA relevantes del día (WebSearch).
2. Redactar el resumen siguiendo el formato "periódico moderno" indicado en
   el prompt de la rutina (titular del día, también hoy, 3 buenas noticias).
3. Guardar el resumen en `resumenes/YYYY-MM-DD.md` (archivo histórico).
4. **Sobrescribir `hoy.md`** (en la raíz del repo) con el mismo contenido del
   día. Este archivo es un **enlace fijo**: el usuario lo abre cada día desde
   el móvil para leer el resumen, así que su URL nunca debe cambiar.
5. Hacer commit y push a la rama de trabajo (`claude/zen-brown-568jp6`,
   o la rama indicada en las instrucciones de la sesión, si difiere de esta).
6. Enviar una notificación push (PushNotification) con el siguiente formato
   exacto dentro de las etiquetas <routine_summary>:

   - **Primera línea:** titular corto del día (aparece como banner en el móvil).
   - **Segunda línea en blanco.**
   - **Enlace al resumen completo** (OBLIGATORIO, siempre en la segunda posición):
     https://github.com/manuelescribanotorres03-byte/ianews/blob/claude/zen-brown-568jp6/hoy.md
   - Avance de 3-4 líneas con los puntos clave del día (titular, también hoy,
     buenas noticias).

   Ejemplo de estructura:
   ```
   <routine_summary>
   🗞️ [TITULAR BREVE DEL DÍA]

   👉 Lee el resumen completo aquí:
   https://github.com/manuelescribanotorres03-byte/ianews/blob/claude/zen-brown-568jp6/hoy.md

   📌 También hoy: [2-3 puntos clave en una línea cada uno]
   🌞 Buenas noticias: [1 frase]
   </routine_summary>
   ```

## Notas
- El usuario lee principalmente desde el móvil. El enlace debe aparecer siempre
  en la notificación, en lugar visible, para que pueda tocarlo directamente
  sin buscar nada.
- La URL de `hoy.md` es fija y nunca cambia: es el único marcador que el
  usuario necesita para leer el resumen de cada día.
- Si las instrucciones de la sesión indican una rama distinta a la que
  aparece arriba (por ejemplo, porque el sistema reasignó la rama de
  trabajo), usa siempre la rama indicada en la sesión y actualiza este
  archivo (rama y enlaces) para que quede sincronizado de cara a la
  siguiente ejecución.
