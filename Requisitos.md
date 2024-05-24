# Introducción
Este juego es una parodia de los anuncios comunmente vistos en aplicaciones móviles.

# Funcionalidades

## Iniciar partida.
- Como usuario quiero poder inciar una nueva partida y comenzar a jugar puzzles para divertirme con el juego

## Ver leaderboard
- Como usuario quiero poder ver el leaderboard y la posicion mi record para competir contra otros jugadores

## Ver leaderboard personal
- Como ususario quiero ver mi historial de record personales para ver mi mejoría en el tiempo

## Servir nivel
- Como sistema quiero que teniendo en cuenta los sensores del dispositivo, los niveles superados y los niveles todavía no vistos servir al usuario nuevos niveles nivel para mantener al usuario entretenido

## Jugar nivel
- Como usuario quiero jugar un puzzle para pasar el rato

# Analisis

En el apartado de Level Design se especifican los niveles a desarrollar, esta lista es modificable y se irá depurando segun avance el proyecto.

## Tareas Críticas

### Aplicación

- Planficador de niveles. sistema que se encarga de seleccionar los siguientes niveles en función de los sensores del dispositivo y progreso del juego
- Sistema de puntuación en base a la dificultad y velocidad de resolución del puzzle
- Elemento de fondo (minijuego de la bomba que "explota" si no reseteas el contador pulsando el botón)

### Comunicaciones

- Unity. Engine sobre en que se desarrollarán los minijuegos. Se hará uso de un servidor basado en sockets para intercambiar informacion entre ambos.
- Firebase OAuth. Auntenticación de los usuarios en la app.
- Firabase Storage. Guardado en la nube de nicknames y highscores 

## Tareas No Críticas

- Integración de Magnetometro. Para puzzles que dependan de la orientación del dispositivo.
- Integración de Giroscopio. Para puzzles que incluyan rotación des dispositivo.
- Integración de Sensor presión atmosferica. Para puzzles que requiran cambios de altitud.
- Leaderboard para comparar puntuciones entre usuarios

# Level Design

Lista de los potenciales niveles que se van a desarrollar para la aplicación.

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




