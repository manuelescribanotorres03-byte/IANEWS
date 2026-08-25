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
5. Hacer commit y push a la rama de trabajo indicada en las instrucciones de
   la sesión (a fecha de la última ejecución: `claude/nifty-brahmagupta-7dspsl`).
   Esta rama puede cambiar de una sesión a otra si el arnés (harness) asigna
   una nueva; cuando eso ocurra, actualiza también el enlace de abajo para
   que apunte siempre a la rama activa.
6. Enviar una notificación push (PushNotification) con el siguiente formato
   exacto dentro de las etiquetas <routine_summary>:

   - **Primera línea:** titular corto del día (aparece como banner en el móvil).
   - **Segunda línea en blanco.**
   - **Enlace al resumen completo** (OBLIGATORIO, siempre en la segunda posición):
     https://github.com/manuelescribanotorres03-byte/ianews/blob/claude/nifty-brahmagupta-7dspsl/hoy.md
   - Avance de 3-4 líneas con los puntos clave del día (titular, también hoy,
     buenas noticias).

   Ejemplo de estructura:
   ```
   <routine_summary>
   🗞️ [TITULAR BREVE DEL DÍA]

   👉 Lee el resumen completo aquí:
   https://github.com/manuelescribanotorres03-byte/ianews/blob/claude/nifty-brahmagupta-7dspsl/hoy.md

   📌 También hoy: [2-3 puntos clave en una línea cada uno]
   🌞 Buenas noticias: [1 frase]
   </routine_summary>
   ```

## Notas
- El usuario lee principalmente desde el móvil. El enlace debe aparecer siempre
  en la notificación, en lugar visible, para que pueda tocarlo directamente
  sin buscar nada.
- La URL de `hoy.md` es fija mientras la rama de trabajo no cambie: es el
  único marcador que el usuario necesita para leer el resumen de cada día.
  Si el arnés asigna una rama nueva a la sesión, actualiza el enlace en este
  archivo (punto 6 de arriba) en la misma ejecución para que siga siendo
  válido.
