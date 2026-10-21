# Prompt para mejorar «Preguntas de Sara»

Copia todo lo que hay debajo de la línea y pégalo en un chat nuevo abierto sobre este repositorio.

---

Quiero mejorar mi app «Preguntas de Sara». Háblame siempre en español y sin tecnicismos: no soy programador experto.

## Qué es la app

- Juego de cartas de preguntas para dos personas (una amiga y yo), con un solo móvil que se va pasando. No hay cuentas, ni servidor, ni código de partida.
- Todo está en un único archivo, `index.html` (HTML, CSS y JavaScript sin librerías), más `manifest.webmanifest` y los iconos para instalarla en la pantalla de inicio desde GitHub Pages.
- Modos: Preguntillas (con niveles ligero, profundo y muy profundo, o «subiendo»), Princess treatment o bare minimum, Adivina mi respuesta, ¿Qué prefieres?, Opiniones polémicas, Red flag o green flag, Yo nunca, Verdad o reto, ¿Quién es más probable?, Completa la frase, Termómetro, Dos verdades y una mentira y Mezcla de todo.
- Las cartas están en el objeto `DATA`, los nombres y colores de cada modo en `MODES` y las reglas en `RULES`.
- El orden de cada mazo y por dónde vamos se guardan en el propio móvil (`localStorage`, claves que empiezan por `sm.`). **Eso no se puede perder**: cualquier cambio tiene que respetar esas claves o migrarlas sin borrar el progreso.
- Estilo actual: fondo oscuro morado (#1E1633), un color vivo por modo, tipografías Lilita One (títulos) y Nunito (texto).

## Skills que quiero que uses

- **ux-heuristics**: auditoría de usabilidad y accesibilidad (Nielsen, Krug, contraste, tamaño de botones).
- **refactoring-ui**: jerarquía visual, espaciados, colores y sombras de las cartas y la portada.
- **microinteractions**: cómo se siente repartir, pasar y barajar cartas (animaciones, respuesta al toque, el «momento» de la app).
- **frontend-design**: dirección visual, para que tenga personalidad propia y no parezca una plantilla.
- Si están disponibles, también **web-design-guidelines** (repaso de detalles de interfaz) y **webapp-testing** (probar la app con Playwright y sacar capturas).

## Fase 1 — Análisis (sin cambiar nada)

1. Lee `index.html` entero y explícame en pocas líneas cómo funciona hoy.
2. Abre la app en un navegador con tamaño de móvil (390×844) y haz capturas de: portada, la pantalla de reglas de un modo, una carta de cada tipo distinto (pregunta normal, «¿Qué prefieres?», «Yo nunca», verdad o reto, una con veredictos) y el final del mazo.
3. Pasa **ux-heuristics**: ¿se entiende a la primera qué hacer? ¿cómo se pasa de carta, se vuelve atrás o se sale? ¿botones de al menos 44 px? ¿contraste suficiente sobre cada color de modo? ¿funciona con lector de pantalla y con «reducir movimiento»? Puntúa cada problema por gravedad.
4. Pasa **refactoring-ui** a la portada y a las cartas: jerarquía, espacios, si los 13 colores conviven bien y si el texto largo de algunas cartas se lee cómodo.
5. Pasa **microinteractions** a repartir, pasar, barajar y elegir modo.
6. Revisa los textos de las cartas y de las reglas: erratas, frases que suenan raras o a traducción, cartas repetidas o casi iguales, cuántas cartas tiene cada modo y qué modos se quedan cortos.
7. Enséñame un resumen con las capturas y una nota de 0 a 10 por apartado.

## Fase 2 — Plan (y espera mi aprobación)

Prepara una lista de mejoras en tres bloques, cada una con **impacto** (alto/medio/bajo) y **esfuerzo** (poco/medio/mucho):

- **Diseño**: portada, cartas, transiciones, coherencia de colores, el logo cuando te lo pase (icono y portada).
- **Contenido**: cartas nuevas para los modos más cortos, pulir textos, equilibrar niveles de Preguntillas, reglas más cortas y claras.
- **Enganche y funcionalidad**: ideas pensadas para dos personas con un móvil, por ejemplo marcar cartas favoritas, saltar una carta, llevar la cuenta de aciertos en «Adivina mi respuesta», un temporizador opcional, añadir cartas propias o que funcione sin conexión.

No toques código hasta que te diga qué mejoras quiero.

## Fase 3 — Implementación por bloques

- Empieza por lo de **alto impacto y poco esfuerzo**.
- Trabaja en una rama, un bloque cada vez, y al acabar cada bloque abre la app en el navegador, haz capturas de antes y después y enséñamelas.
- Mantén la app en un solo archivo y sin dependencias nuevas salvo que me lo consultes.
- No pierdas el progreso guardado en el móvil (claves `sm.` de `localStorage`).
- Comprueba que se sigue pudiendo instalar en la pantalla de inicio y que se ve bien en móviles pequeños (360 px de ancho) y con el texto del sistema más grande.
- Al final, haz una auditoría rápida otra vez con **ux-heuristics** para confirmar que ha mejorado la nota.

## Avisos

- **Contenido**: hay modos atrevidos (Opiniones polémicas, Yo nunca, Verdad o reto). Si la app la pudiera usar alguien menor de edad, las cartas subidas de tono deben ir aparte y poder desactivarse. Los retos no pueden implicar nada peligroso, ilegal, ni presionar a hacer algo que la otra persona no quiera; añade siempre la opción de pasar carta sin penalización.
- **Privacidad**: las respuestas pueden ser muy personales. Nada de enviar datos fuera del móvil, ni analíticas, ni servicios externos (salvo las fuentes de Google que ya usa, y si las quitas mejor, para que funcione sin conexión).
- **Sin trucos para enganchar**: nada de rachas que castiguen, notificaciones insistentes ni cosas que te hagan sentir mal por no jugar.
