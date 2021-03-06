# Reddit Place Bot para r/Mexico

Bot para Reddit [/r/place](https://www.reddit.com/r/place/) de r/México.

Bot creado por [Zequez](https://github.com/Zequez/reddit-placebot)

## Instalación

1. Descargar NodeJS. [Click aquí para descargarlo.](https://nodejs.org/es/download/)
2. Descargar los archivos del git. Hay 2 opciones para hacer esto:
    1. Abre terminal (Mac o Linux) o CMD (Windows) y escribe ```git clone https://github.com/alexherce/reddit-placebot``` (Recomendado, pero si estas en Windows usa la opción 2, es mas fácil)
    2. Descargar como zip y descomprimir. [Click aquí para descargar el zip](https://github.com/alexherce/reddit-placebot/archive/master.zip)
3. En terminal (Mac y Linux) o CMD (Windows), ve al folder que descargaste (y descomprimiste, si fue el caso) usando ```cd```. [Ve estas instrucciones si no sabes como](http://es.wikihow.com/cambiar-directorios-en-el-Command-Prompt)
4. Escribe ```npm install``` y da enter. Continúa leyendo las instrucciones

## Configuración

1. Abre el archivo `users.example.json`, cambia los datos con tus usuarios y passwords. NOTA: puedes tener más de 1 cuenta, pero la última línea no debe llevar coma al final. Para que funcione con r/place, la cuenta debe haber sido abierta antes del 31 de marzo del 2017
2. Guarda el archivo como `users.json`
3. Si ejecutaste previamente el bot, borra los archivos `queues.json` y `cookies.json` antes de correrlo de nuevo

## Dibujar en r/place con el bot

El bot por default dibuja el archivo [`official_target.bmp`](https://raw.githubusercontent.com/alexherce/reddit-placebot/master/official_target.bmp) de este repositorio en r/place. Todos los bots por default usan este archivo para mantener coordinación. Si quieres poner algo con todos los bots de r/mexico, entra al Discord del sub.

Si quieres dibujar otra cosa, abre el archivo `config.js` y cambia `autoupdateRemoteTarget: false`. Eso hará que el bot use `target.bmp` como mapa para dibujar en r/place en lugar de jalar el `official_target.bmp` de este repositorio. Edita `target.bmp` a tu gusto.

NOTA: De preferencia no cambies el target, así todos en r/mexico podemos dibujar lo mismo en coordinación.

Cada que sea tiempo de dibujar un pixel, el bot bajara la imagen de este git, comparara los pixeles y encontrara el primero que no concuerde para después pintarlo de acuerdo a la imagen.

## IMPORTANTE: Sobre los colores

Si editas los targets BMP, necesitas usar los mismos colores que están en el archivo `colors.js`. Ahí puedes encontrar los códigos RGB para los colores permitidos en r/place. El bot NO adivina similitudes de color. Si un color en los BMP no concuerda, dibujara un pixel blanco en 0, 0 (un pixel desperdiciado).

El color `#ff00ff` (magenta) en los targets es la manera de indicarle al bot que lo ignore. De esta manera puedes delimitar el área a dibujar. Todo lo que este de color `#ff00ff` lo ignorara.

## Uso

Para usar, simplemente escribe en la terminal/cmd:
```
  npm run start
```
NOTA: Necesitas estar sobre el folder que descargaste de este git en el paso 2.

Esto correrá el bot, si no encuentra nada que dibujar, esperará a que algo cambie para luego corregirlo.

Para detener el bot, usa CTRL + C en la terminal/cmd donde se estaba ejecutando.

## License

MIT
