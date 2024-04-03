# Actividades

## Inciar sesión (Login)
- Punto de entrada: Arranque de aplicación cuando no hay usuario registrado.
- Descripción: Este es un componente que solo aparece la primera vez y te permite registrarte con Google Play para guardar tu progreso.

## Elegir nombre (Nickname)
- Punto de entrada: Login.
- Descripción: Este es un componente que solo aparece la primera vez y te permite seleccionar un nombre de usuario para que aparezca en la pantalla de 

## Menú principal
- Punto de entrada: Arranque de aplicación (despues de haber quedado registrado el correo y nickname).
- Descripción: Este es el menú inicial desde el que el usuario puede acceder al resto de pantallas.

## Highscores / Leaderboard
- Punto de entrada: Menú principal.
- Descripción: Estos dos componente los vamos a implementar con una misma activity y vamos a cargar datos distintos en funcion de lo que el usuario haya seleccionado.

## Configuración (Settings)
- Punto de entrada: Menú principal.
- Descripción:
 
## Jugar (UnityPlayerActivity)
- Punto de entrada: Menú principal.
- Descripción: Empieza una partida en modo de juego infinito.

## Selector de niveles (Level Selector)
- Punto de entrada: Menú principal.
- Descripción: Permite seleccionar un nivel para juagar en modo nivel individual. Al principio todos los niveles están bloqueados, luego según el usuario se los vaya encontrando en el modo infinito, se irán desbloqueando en esta pantalla para que pueda practicarlos.

## Nivel (Level)
- Punto de entrada: Selector de Niveles o Menú principal.
- Descripción: UnityPlayerActivity al finalizar también invoca la terminación de la actividad que la ha llamado, por lo que es necesario tener una Activity intermediaria para poder volver correctamente a la pantalla esperada.

## Pantalla de victoria
- Punto de entrada: Al finalizar un Nivel.
- Descripción: Esta pantalla se muestra cuando el usuario que ha terminado la partida.

## Pantalla de derrota
- Punto de entrada: Al finalizar un Nivel.
- Descripción: Esta pantalla se muestra cuando el usuario que ha terminado la partida.

# Fragments
Para esta aplicación no es necesario realizar navegación entre distintas funcionalidades ya que tiene un conjunto de funcionalidades muy sencillo y otras aplicaciones del mercado siguen el mismo modelo de pantallas individuales para cada lugar distinto.


# Servicios

## UnityBridge. Interfaz entre Unity y la aplicación de Android.

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





