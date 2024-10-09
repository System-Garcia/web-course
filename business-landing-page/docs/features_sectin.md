# Sección de Features

En esta sección, se muestra una lista de características y una integración de un video (o una imagen de referencia). La estructura está dividida en dos partes principales: una lista de ítems que describen las características y un contenedor para un video. A continuación se detalla cada parte:

## Estructura HTML

```html
<!-- Lista de características e integración de video -->
<div class="features__content">
    <div class="features__list">
        <div class="feautures__item">
            <img src="./images/icons/figures.svg" alt="figures icon">
            <h3>OpenType Features Variable fonts</h3>
            <p>Slate helps you see how many more days you need to work to reach your financial goal.</p>
        </div>
        <div class="feautures__item">
            <img src="./images/icons/brush.svg" alt="brush icon">
            <h3>Design with real data</h3>
            <p>Slate helps you see how many more days you need to work to reach your financial goal.</p>
        </div>
        <div class="feautures__item">
            <img src="./images/icons/pencil.svg" alt="pencil icon">
            <h3>Fastest way to take action</h3>
            <p>Slate helps you see how many more days you need to work to reach your financial goal.</p>
        </div>
    </div>
    <div class="features__video">
        <!-- Video -->
        <!-- Como no tenemos el video, usamos una imagen de referencia -->
        <img src="./images/screen.svg" alt="video sobre features">
    </div>
</div>
```

## Explicación

- **`<div class="features__content">`**: Contenedor principal que agrupa la lista de características y el video.
- **`<div class="features__list">`**: Contenedor de la lista de características, que incluye tres ítems (cada uno es un `div` con la clase `feautures__item`).
- **`<div class="feautures__item">`**: Cada ítem contiene una imagen (`<img>`), un título (`<h3>`) y una descripción (`<p>`). La imagen es un ícono que representa cada característica.
- **`<div class="features__video">`**: Contenedor del video (o imagen de referencia). En este caso, se ha colocado una imagen (`screen.svg`) para representar el lugar del video.


## Estilos CSS
```CSS
/* Estilos para la sección de Features */
.features {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.features__title {
    font-size: 4.8rem;
    font-weight: 700;
    margin-bottom: 3rem;
}

.features__paragraph {
    font-size: 2.8rem;
    max-width: 60rem;
    margin-bottom: 5rem;
    color: #374754;
}

.features__content {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.features__list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    max-width: 65rem;
    gap: 2.4rem;
}

.feautures__item {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.features__video {
    max-width: 100rem;
    position: relative;
}

.features__video::after {
    content: '';
    display: block;
    background-image: url('./images/icons/play_icon.svg');
    width: 10rem;
    height: 10rem;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-size: cover;
    cursor: pointer;
}
```

## Explicación de CSS

- **`.features`**: Define la disposición general de la sección, usando `flex` para centrar el contenido.
- **`.features__title` y `.features__paragraph`**: Estilos para el título y el párrafo de introducción de la sección, definiendo tamaño de fuente y márgenes.
- **`.features__content`**: Define la disposición del contenido principal, centrado en la página.
- **`.features__list`**: Usa `grid` para distribuir los ítems en tres columnas de ancho uniforme (`1fr`).
- **`.feautures__item`**: Alinea cada ítem de la lista de manera vertical y centra el contenido.
- **`.features__video`**: Contenedor del video o imagen con un `position: relative` para posicionar el ícono de play.
- **`.features__video::after`**: Crea un ícono de "play" sobre la imagen del video, usando un `::after` pseudo-elemento para colocar la imagen en el centro del contenedor.

## Conceptos Nuevos

### Uso de Grid para la disposición de elementos

- **`display: grid`**: Permite organizar los elementos en una estructura de cuadrícula.
- **`grid-template-columns: repeat(3, 1fr)`**: Crea una cuadrícula con 3 columnas de igual ancho, cada una ocupando una fracción (`1fr`) del espacio disponible.
- **`gap: 2.4rem`**: Define el espacio entre los elementos de la cuadrícula.

El `grid` es una alternativa muy poderosa a `flexbox` cuando se necesita organizar elementos en filas y columnas, ya que facilita la disposición de elementos en layouts más complejos.

### Uso de Pseudo-elementos

- **`::after`**: Es un pseudo-elemento que permite agregar contenido decorativo después del contenido de un elemento.
- **`content: ''`**: Se utiliza para insertar contenido vacío, pero que puede tener estilos aplicados.
- **`background-image` y `position: absolute`**: Se combinan para colocar una imagen sobre el contenedor del video, en este caso un ícono de "play" centrado.

Los pseudo-elementos como `::after` son útiles para añadir elementos decorativos (como íconos) sin necesidad de agregar más elementos HTML, lo que hace el código más limpio.

### Integración de Video

- Aunque en este ejemplo se usa una imagen de referencia en lugar de un video real, el contenedor `.features__video` está diseñado para poder contener un video.
- En lugar de la etiqueta `<img>`, se podría utilizar una etiqueta `<video>` para incluir un video real, por ejemplo:

    ```html
    <video src="./videos/demo.mp4" controls></video>
    ```

- El atributo `controls` agrega controles de reproducción al video (play, pause, volumen, etc.).
- Al usar videos, es importante considerar la compatibilidad de formatos (`mp4`, `webm`, `ogg`) para asegurar que se reproduzcan en todos los navegadores.

## Notas

- La lista de características se muestra en forma de `grid`, lo cual es ideal para distribuir ítems de manera uniforme.
- Se utiliza `::after` para colocar un ícono de "play" sobre la imagen del video, mejorando la experiencia visual del usuario.
- Los estilos de `flex` y `grid` permiten que el diseño se mantenga alineado y responda bien a diferentes tamaños de pantalla.
- Incluir videos puede enriquecer la experiencia de usuario, pero es importante optimizarlos para mantener un buen rendimiento de la página.
