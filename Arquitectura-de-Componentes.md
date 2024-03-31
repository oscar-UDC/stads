# Actividades

- Login
Este es un componente que solo aparece la primera vez y te permite registrarte con Google Play para guardar tu progreso.

- Selecionar nickname
Este es un componente que solo aparece la primera vez y te permite seleccionar un nombre de usuario para que aparezca en la pantalla de Highscores / Leaderboar

- Highscores / Leaderboar
Estos dos componente los vamos a implementar con una misma activity y vamos a cargar datos distintos en funcion de lo que el usuario haya seleccionado

# Fragments
Para esta aplicación no es necesario realizar navegación entre distintas funcionalidades ya que tiene un conjunto de funcionalidades muy sencillo y otras aplicaciones del mercado siguen el mismo modelo de pantallas individuales para cada lugar distinto.


# Servicios

- UnityBridge. Interfaz entre Unity y la aplicación de Android
Habrá un servició que se encargará de la gestión de un Servidor con la funcion de intermediario entre el juego de Unity y la app mediante mensajes json entre ellos.

Android indicará el modo de juego que el usuario ha seleccionado:

```json
{
	"gamemode": "infinite"
}
```
o
```json
{
	"gamemode": "level",
	"level": 1
}
```
Y el juego de Unity mandará datos del progreso del jugador en el juego, por ejemplo:

Para el modo de juego infinito se mandarán estos datos al terminar la partida:
```json
{
	"type": "InfiniteMode",
	"stage": 10, // Niveles superados
	"clearTime": 600000, // Duración de la partida en segundos
	"score": 500 // Puntuación total
}
```

Si durante el modo infinito el usuario ve un nuevo tipo de juego:
```json
{
	"type": "LevelUnlocked",
	"level": 2
}
```

Para el selector de niveles se mandarán estos datos al terminar la partida:
```json
{
	"type": "LevelClear",
	"level": 2
}
```

```json
{
	"type": "LevelFailed",
	"level": 2
}
```





