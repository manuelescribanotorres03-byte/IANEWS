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
5. Hacer commit y push a la rama de trabajo (`claude/eloquent-mayer-qydwks`,
   o la rama indicada en las instrucciones de la sesión).
6. Enviar una notificación push (PushNotification) con el enlace fijo a
   `hoy.md` en GitHub, p. ej.:
   `https://github.com/manuelescribanotorres03-byte/ianews/blob/claude/eloquent-mayer-qydwks/hoy.md`
   El primer mensaje de la notificación debe ser breve (titular del día);
   el resto puede incluir el enlace y un resumen corto de "también hoy" y
   "buenas noticias".

## Notas
- El usuario lee principalmente desde el móvil, por eso es clave el enlace
  fijo: un único marcador/acceso directo que siempre muestra el resumen de
  hoy, sin tener que buscarlo cada vez.
