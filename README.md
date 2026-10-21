# Preguntas de Sara

Juego de cartas para dos personas: preguntillas, princess treatment o bare minimum, verdad o reto y más modos. Se juega con un solo móvil, pasando cartas.

Es una sola página (`index.html`) sin dependencias. Para usarla en el móvil, publícala con GitHub Pages y añádela a la pantalla de inicio.

Las cartas están en el objeto `DATA` dentro de `index.html`.

Funciona sin internet: `sw.js` guarda la app y las fuentes en el móvil la primera vez que se abre con conexión. Si cambias `sw.js`, sube el número de `CACHE` para que los móviles descarguen la versión nueva.
