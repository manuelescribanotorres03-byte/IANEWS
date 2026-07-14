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
   la sesión (rama actual: `claude/vibrant-shannon-vzhiez`). **Importante:**
   el sistema que lanza cada sesión asigna un nombre de rama nuevo de forma
   aleatoria (no hay rama `main` en este repo), así que la rama "fija" puede
   cambiar de una sesión a otra. Antes de generar el enlace del punto 6,
   comprueba SIEMPRE cuál es la rama designada en las instrucciones de la
   sesión actual y úsala en la URL, aunque no coincida con la de más abajo.
6. Enviar una notificación push (PushNotification) con el siguiente formato
   exacto dentro de las etiquetas <routine_summary>:

   - **Primera línea:** titular corto del día (aparece como banner en el móvil).
   - **Segunda línea en blanco.**
   - **Enlace al resumen completo** (OBLIGATORIO, siempre en la segunda posición),
     sustituyendo `<rama-actual>` por la rama de trabajo real de la sesión:
     https://github.com/manuelescribanotorres03-byte/ianews/blob/<rama-actual>/hoy.md
     (última rama conocida: `claude/vibrant-shannon-vzhiez`)
   - Avance de 3-4 líneas con los puntos clave del día (titular, también hoy,
     buenas noticias).

   Ejemplo de estructura:
   ```
   <routine_summary>
   🗞️ [TITULAR BREVE DEL DÍA]

   👉 Lee el resumen completo aquí:
   https://github.com/manuelescribanotorres03-byte/ianews/blob/<rama-actual>/hoy.md

   📌 También hoy: [2-3 puntos clave en una línea cada uno]
   🌞 Buenas noticias: [1 frase]
   </routine_summary>
   ```

## Notas
- El usuario lee principalmente desde el móvil. El enlace debe aparecer siempre
  en la notificación, en lugar visible, para que pueda tocarlo directamente
  sin buscar nada.
- La intención original era que la URL de `hoy.md` fuera fija, pero como cada
  sesión recibe una rama nueva y no existe una rama `main` estable, el enlace
  cambia cada vez que el sistema asigna otro nombre de rama. Hasta que se
  resuelva esto (por ejemplo fijando un `main` real o un dominio propio),
  cada resumen debe avisar si el enlace ha cambiado respecto al anterior.
