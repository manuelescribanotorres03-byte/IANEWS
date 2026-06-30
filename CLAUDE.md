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
   la sesión (a fecha de la última ejecución: `claude/vibrant-shannon-miz4rc`).
6. Enviar una notificación push (PushNotification) con el siguiente formato
   exacto dentro de las etiquetas <routine_summary>:

   - **Primera línea:** titular corto del día (aparece como banner en el móvil).
   - **Segunda línea en blanco.**
   - **Enlace al resumen completo** (OBLIGATORIO, siempre en la segunda posición),
     usando la rama de trabajo actual de la sesión:
     https://github.com/manuelescribanotorres03-byte/ianews/blob/claude/vibrant-shannon-miz4rc/hoy.md
   - Avance de 3-4 líneas con los puntos clave del día (titular, también hoy,
     buenas noticias).

   Ejemplo de estructura:
   ```
   <routine_summary>
   🗞️ [TITULAR BREVE DEL DÍA]

   👉 Lee el resumen completo aquí:
   https://github.com/manuelescribanotorres03-byte/ianews/blob/claude/vibrant-shannon-miz4rc/hoy.md

   📌 También hoy: [2-3 puntos clave en una línea cada uno]
   🌞 Buenas noticias: [1 frase]
   </routine_summary>
   ```

   ⚠️ Importante: si en una futura ejecución las instrucciones de la sesión
   indican una rama distinta a la de arriba, hay que actualizar este archivo
   (los dos enlaces de esta sección) para que apunten a la nueva rama. El
   "enlace fijo" para el usuario es conceptualmente fijo, pero su URL exacta
   depende de la rama activa de cada sesión, así que debe mantenerse
   sincronizada aquí.

## Notas
- El usuario lee principalmente desde el móvil. El enlace debe aparecer siempre
  en la notificación, en lugar visible, para que pueda tocarlo directamente
  sin buscar nada.
- La URL de `hoy.md` es fija y nunca cambia: es el único marcador que el
  usuario necesita para leer el resumen de cada día.
