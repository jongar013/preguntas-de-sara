# Preguntas de Sara

Juego de cartas para dos personas: preguntillas, princess treatment o bare minimum, verdad o reto y más modos. Se juega con un solo móvil, pasando cartas.

Es una sola página (`index.html`) sin dependencias. Para usarla en el móvil, publícala con GitHub Pages y añádela a la pantalla de inicio. Después de abrirla una vez con internet, funciona sin conexión gracias a `sw.js`.

Las cartas están en el objeto `DATA` dentro de `index.html`. Con el corazón de cada carta se guardan en el mazo «Vuestras favoritas».

Si cambias `index.html`, sube la versión de `CACHE` en `sw.js` para que los móviles descarguen la nueva.
