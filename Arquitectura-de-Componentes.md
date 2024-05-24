# Actividades

## Inciar sesión (Login)
- Punto de entrada: Arranque de aplicación cuando no hay usuario registrado.
- Descripción: Este es un componente que solo aparece la primera vez y te permite registrarte con Google Play para guardar tu progreso.

## Menú principal
- Punto de entrada: Arranque de aplicación (despues de haber quedado registrado el correo y nickname).
- Descripción: Este es el menú inicial desde el que el usuario puede acceder al resto de pantallas.

## Nivel (Level)
- Punto de entrada: Selector de Niveles pulsando un botón cualquiera o Menú principal pulsando en jugar al modo infinito.
- Descripción: UnityPlayerActivity al finalizar también invoca la terminación de la actividad que la ha llamado, por lo que es necesario tener una Activity intermediaria para poder volver correctamente a la pantalla esperada.

# Fragments y Composeables

Vamos a utilizar Jetpack Compose para toda la aplicación, lo que significa que todos los elementos de la interfaz de usuario serán Composeables. Un Composeable es similar a un fragment, por lo que los trataremos en esta sección.

## Elegir nombre (Nickname)
- Punto de entrada: Login.
- Descripción: Este es un componente que solo aparece la primera vez y te permite seleccionar un nombre de usuario para que aparezca en la pantalla de 

## Highscores / Leaderboard
- Punto de entrada: Menú principal.
- Descripción: Estos dos componente los vamos a implementar con una misma activity y vamos a cargar datos distintos en funcion de lo que el usuario haya seleccionado.

![ScoresComentado](https://github.com/Diego-a-lopez/ScapeTheAds/assets/71869193/aa7d7529-caa1-4a2e-a1ff-398b0aafbe89)

## Configuración (Settings)
- Punto de entrada: Menú principal.
- Descripción: Este componente permite configurar el volumen de la aplicación y el idioma de sus textos.
 
![SettingsComentado](https://github.com/Diego-a-lopez/ScapeTheAds/assets/71869193/59b74912-1402-4bd6-849c-510f8bcaa1c8)


## Jugar (UnityPlayerActivity)
- Punto de entrada: Menú principal.
- Descripción: Empieza una partida en modo de juego infinito.

![NivelComentado](https://github.com/Diego-a-lopez/ScapeTheAds/assets/71868889/5636ea4a-6d0c-4094-9483-1835c39fe879)

## Selector de niveles (Level Selector)
- Punto de entrada: Menú principal.
- Descripción: Permite seleccionar un nivel para jugar en modo nivel individual. Al principio todos los niveles están bloqueados, luego según el usuario se los vaya encontrando en el modo infinito, se irán desbloqueando en esta pantalla para que pueda practicarlos.

![LevelSelectorComentado](https://github.com/Diego-a-lopez/ScapeTheAds/assets/71868889/1c6d5482-e001-4063-9ea7-7173e276584b)

## Pantalla de victoria
- Punto de entrada: Al superar un Nivel.
- Descripción: Esta pantalla se muestra cuando el usuario ha terminado la partida.

## Pantalla de derrota
- Punto de entrada: Al finalizar un Nivel.
- Descripción: Esta pantalla se muestra cuando el usuario ha terminado la partida.

# Servicios

## UnityBridge. Interfaz entre Unity y la aplicación de Android.

- Servicio iniciado mediante onStartCommand() ya que Unity finaliza la actividad desde la que fue llamado con lo que se podría finalizar el Servicio inesperadamente y dejar a medias el procesamiento de datos.
- Funcionalidad: Servicio que se encargará de la gestión de un Servidor con la funcion de intermediario entre el juego de Unity y la app mediante mensajes json entre ellos.

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

# LocalScoreManager

Usamos una clase llamada LocalScoreManager que conecta con SharedPreferences para guardar en esta interfaz los highscores locales, es decir, los que registra el usuario en sus partidas, y para obtenerlos cuando el usuario los quiera revisar.

# HighScoreViewModel

Usamos un ViewModel llamado HighScoreViewModel que conecta con el backend, para guardar en él los highscores del usuario en la base de datos global, y para poder cargarlos en la aplicación.

# Corrutinas

## Corrutina de guardado de datos del juego

- El juego de Unity mandará datos sobre la partida del jugador que se guardarán en la Android Room y el backend. Las llamadas al API pueden relentizar el procesaminedo de datos del Servidor de Unity (UnityBridge) por lo que se ejecutara en una corrutina de GlobalScope. Se liberarán recursos tan pronto de hallan guardado datos en la Android Room y el backend o ocurra un error, por lo que una GlobalScope es adecuada para realizar el trabajo.

## Corrutinas de actualizacion de scores

- Cuando el jugador termine una partida se realizará una corrutina para actualizar las puntuaciones globales (si la puntuación supera el record anterior) y locales

## Corrutinas de autenticación

- Vamos a usar corrutinas para recuperar datos como el nickname en la pantalla del menú principal y para almacenar el usuario mientras el usuario selecciona su nickname la primera vez que se registra



