# IANEWS — Resumen diario de IA

Este repo genera cada mañana un resumen de noticias de IA en español, pensado
para un lector sin formación técnica (comercial, estudiante de dietética).

## Perfil del usuario (para personalizar Cultura General y Eventos)

- Vive en Cercedilla (Madrid) y se mueve habitualmente por Madrid y alrededores.
- Profesión: comercial / ventas. Formación: grado superior en dietética.
- Está muy metido en el mundo TEDx, marketing y social media marketing
  agencies (incluyendo el uso de IA en marketing).
- Le interesa el dinero, los negocios, invertir: trading, inversión
  inmobiliaria, mundo financiero en general.
- Le gustan los coches y las motos.
- Le gusta el desarrollo personal, el crecimiento y la espiritualidad.
- Le encanta el networking: rodearse de gente con dinero, mentores, gente
  conocida del sector, eventos donde se aprende y se conectan personas.
- Le gusta leer y estar al día de lo que pasa en el mundo para poder
  conversar de cualquier tema con cualquiera.

## Qué hacer en cada ejecución de la rutina

1. Investigar las noticias de IA relevantes del día (WebSearch), y también
   las noticias más relevantes del día a nivel general (política, economía,
   deporte/fútbol, sociedad, cultura, ciencia... un poco de todo, lo que esté
   moviendo el mundo hoy) para la sección de Cultura General.
2. Investigar también eventos, charlas, ferias, seminarios y oportunidades de
   networking (ver sección "Eventos" más abajo).
3. Redactar el resumen siguiendo el formato "periódico moderno" indicado en
   el prompt de la rutina (titular del día, también hoy, 3 buenas noticias),
   y añadir al final, tras "🌞 3 BUENAS NOTICIAS DEL DÍA", dos secciones extra:

   ### 🌍 CULTURA GENERAL
   Las noticias más relevantes del día a nivel mundial, NO limitadas a 2-3 ni
   a un tema concreto: un poco de todo (política, economía, deporte/fútbol,
   sociedad, cultura, ciencia, negocios...). Para cada una: una frase de
   gancho, qué ha pasado y por qué es relevante, explicado de forma breve y
   sencilla. El objetivo es que el lector amplíe su cultura general y pueda
   seguir conversaciones de actualidad con cualquiera —incluyendo entornos de
   networking, inversión y negocios, donde este tipo de cultura general es un
   activo—, aunque el tema no tenga nada que ver con su trabajo o sus
   estudios. Misma exigencia de calidad que el resto: información real,
   contrastada y con fuente.

   ### 📅 EVENTOS Y NETWORKING
   Eventos, charlas, ferias, seminarios y encuentros que puedan interesarle,
   tanto para ir hoy/esta semana como para apuntarse con antelación (y poder
   invitar a amigos). Prioriza eventos en Madrid y alrededores (incluyendo
   Cercedilla y sierra de Madrid), pero incluye también eventos relevantes a
   nivel nacional/online si son destacados. Temas a vigilar:
     - TEDx talks, charlas y conferencias
     - Networking de negocios, ventas, inversión, trading, inmobiliario
     - Marketing, redes sociales, agencias y IA aplicada al marketing
     - Desarrollo personal, crecimiento, espiritualidad, aprendizaje
       acelerado y similares
     - Ferias, exposiciones y eventos sociales relevantes
   Para cada evento indica: nombre, fecha (y lugar si aplica), una frase de
   por qué puede interesarle, y un enlace para ver más información o
   inscribirse (si existe). Distingue claramente entre "esta semana" y
   "próximamente / para agendar con antelación". Igual que el resto: solo
   información real y verificable, nunca inventar eventos, fechas ni enlaces.
4. Guardar el resumen en `resumenes/YYYY-MM-DD.md` (archivo histórico).
5. **Sobrescribir `hoy.md`** (en la raíz del repo) con el mismo contenido del
   día. Este archivo es un **enlace fijo**: el usuario lo abre cada día desde
   el móvil para leer el resumen, así que su URL nunca debe cambiar.
6. Hacer commit y push a la rama de trabajo (`claude/eloquent-mayer-qydwks`,
   o la rama indicada en las instrucciones de la sesión).
7. Enviar una notificación push (PushNotification) que contenga
   **únicamente el enlace fijo a `hoy.md`** en GitHub, sin titulares, sin
   resúmenes ni texto adicional. El usuario abre el resumen completo
   pulsando ese enlace, no quiere leer nada en la propia notificación.
   Ejemplo de mensaje completo:
   `https://github.com/manuelescribanotorres03-byte/ianews/blob/claude/eloquent-mayer-qydwks/hoy.md`

## Notas
- El usuario lee principalmente desde el móvil, por eso es clave el enlace
  fijo: un único marcador/acceso directo que siempre muestra el resumen de
  hoy, sin tener que buscarlo cada vez.
