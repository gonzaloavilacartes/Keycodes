# Keycodes

Este proyecto es una simple aplicación web que muestra información sobre la tecla presionada en el teclado. Utiliza HTML, CSS y JavaScript para capturar eventos de teclado y mostrar los valores de `key`, `keyCode` y `code` de la tecla presionada.

## Características

- **Detección de Teclas**: Captura eventos de teclado y muestra información detallada sobre la tecla presionada.
- **Interfaz Dinámica**: Actualiza la interfaz en tiempo real para mostrar los valores de `key`, `keyCode` y `code`.

## Estructura de Archivos

- `index.html`: El archivo HTML principal que contiene la estructura de la página.
- `style.css`: Archivo CSS para los estilos de la página.
- `script.js`: Archivo JavaScript que maneja la lógica de detección de teclas y actualización de la interfaz.

## Uso

1. **Clonar el repositorio**:
    ```sh
    git clone <repository-url>
    ```

2. **Abrir [index.html](http://_vscodecontentref_/0) en un navegador web** para ver la aplicación en funcionamiento.

## Código JavaScript

El archivo [script.js](http://_vscodecontentref_/1) contiene el siguiente código:

```javascript
const insert = document.getElementById('insert')

/* Agregamos un detector de eventos 'keydown' que es cuando se presiona una tecla del teclado */
window.addEventListener('keydown', (event) => {

    /* 'console.log(event)' Esto imprimirá por consola varios datos sobre la tecla presionada
    De los cuales eligiremos los que necesitamos, en este caso:

        key: d
        keyCode: 68
        code: keyD
    */

    /* *Linea 20* Si la 'key' es ' ' (cadena vacía) entonces coloca 'Space' de lo contrario pone el valor 'key' */

    insert.innerHTML = `
    <div class="key">
        ${event.key === ' ' ? 'Space' : event.key}
        <small>event.key</small>
    </div>

    <div class="key">
        ${event.keyCode}
        <small>event.keyCode</small>
    </div>

    <div class="key">
        ${event.code}
        <small>event.code</small>
    </div>
    `
})
