# Introducción
Este juego es una parodia de los anuncios comunmente vistos en aplicaciones móviles.

# Analisis

En el apartado de Level Design se especifican los niveles a desarrollar, esta lista es modificable y se irá depurando segun avance el proyecto.

## Tareas Críticas

### Aplicación

- Planficador de niveles. sistema que se encarga de seleccionar los siguientes niveles en función de los sensores del dispositivo y progreso del juego

### Comunicaciones

Ejemplo: funcionalidades indispensables para la operativa (e.g.,
autenticación, GPS).

- Magnetometro
- Giroscopio

## Tareas No Críticas

Dependencias de terceros, fuentes de datos externas (e.g.,
visualización mapas, cloud).

- Autenticación
- Leaderboard, Highscore
- Compartir en redes sociales records

# Level Design

## Level Placeholder
- Sensores necesarios: Ninguno
- Breve descripción: 

## Level Sopa de letras
- Sensores necesarios: Ninguno
- Breve descripción: El boton de saltar anuncio esta escondido entre una pantalla llena de distintas letras

## Level Input incorrecto
- Sensores necesarios: Ninguno
- Breve descripción: Hay N botones en pantalla junto con uno de "Omitir", al usuario pulsar en uno se acciona otro boton que el usuario claramente no pulso

## Level Error de Traducción
- Sensores necesarios: Ninguno
- Breve descripción: Las labels de los botones aparecen en chino (y se randomiza el orden de los botones cada vez)

## Level Omitir por detras
- Sensores necesarios: Giroscopio
- Breve descripción: Habrá un cubo en pantalla que en funcion del giroscopio rotará dejando ver el boton de omitir anuncio que estaba en la cara oculta

## Level Omitir modo oscuro
- Sensores necesarios: Brillo
- Breve descripción: Habrá un boton de omitir solo visible con el brillo al mínimo




