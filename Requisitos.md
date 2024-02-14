# Introducción
Este juego es una parodia de los anuncios comunmente vistos en aplicaciones móviles.

# Funcionalidades

## Iniciar partida.
- El usuario incia una nueva partida y le comeinzan a servir niveles

## Ver leaderboard
- El usuario puede ver el leaderboard y la posicion de su record propio

## Servir nivel
- El sistema teniendo en cuenta los sensores del dispositivo, los niveles superados y los niveles todavía no vistos sirve al usuario un nuevo nivel

## Ver leaderboard personal

# Analisis

En el apartado de Level Design se especifican los niveles a desarrollar, esta lista es modificable y se irá depurando segun avance el proyecto.

## Tareas Críticas

### Aplicación

- Planficador de niveles. sistema que se encarga de seleccionar los siguientes niveles en función de los sensores del dispositivo y progreso del juego
- Sistema de puntuación en base a la dificultad y velocidad de resolución del puzzle

### Comunicaciones


## Tareas No Críticas

- Unity. Game engine sobre el que se va a desarrollar los puzzles del juego.
- Magnetometro. Para puzzles que dependan de la orientación del dispositivo.
- Giroscopio. Para puzzles que incluyan rotación des dispositivo.
- Sensor presión atmosferica. Para puzzles que requiran cambios de altitud.
- Autenticación para recuperar datos del usuario (highscore, logros)
- Leaderboard para comparar puntuciones entre usuarios
- Compartir en redes sociales highscores

# Level Design

Lista de los potenciales niveles que se van a desarrollar para la aplicación.

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

## Level Mira al norte
- Sensores necesarios : Brújula
- Breve descripción : En este nivel se le mandará al usuario a mirar al norte y con una tolerancia de 20º cuando este mirando al norte aparecerá en botón de cerrar el ad

## Level Rompe la pared
- Sensores necesarios : acelerómetro
- Breve descripción : En este nivel se le pedirá al usuario que agite el teléfono para "derribar" una pared tras la que se esconde el botón de cerrar ad
## Level saca foto a objeto de color

- Sensores necesarios : Cámara
- Breve descripción : En este nivel se le pedirá al usuario que haga una foto de un objeto de color x para que aparezca el boton de cerra el ad




