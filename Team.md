A continuación se detallan el reparto de roles y de funcionalidades para el desarrollo del proyecto. Las funcionalidades se reparten del siguiente modo: una tarea crítica y varios levels para cada uno. Se espera que la lista de levels cambie y aumente con el tiempo, en función de los requisitos de tamaño de la aplicación.

# Roles finales

## CEO (Director ejecutivo) y CXO (Responsable de experiencia de usuario)
- Encargado: Diego Antonio Lopez
- Roles
	- Testing
	- UI/UX
- Tareas realizadas
	- Pantallas
		- Leaderboard/Highscores
		- Home
		- Settings
	- Funcionalidades
		- Theme (oscuro/claro,  Cambio de tema dinámico con el tema del dispositivo)
		- Idioma (Asociar el cambio de idioma desde la pantalla settings a la variable DataStore)
		- Implementación de la base de datos para guardar los scores locales  (AndroidRoom)
		- Musica (Añadir música y linkearlo con las preferencias locales de DataStore y gestionar que se pause o haga release)
		- Componentes generales (cardColumnBackground y Botones)
		- Server API REST (abandonado y cambiado por firestore)
	- Minijuegos
		- Shake Level / Rompe muros (acelerómetro)
## CTO (Responsable de tecnologías no-Android)
- Encargado: Daniel Silva Iglesias
- Roles
	- Arquitectura
	- Integraciones
	- Sensórica
	- Documentación
- Tareas realizadas
	- Pantallas
		- Login
		- Nickname
		- Home (rediseño)
		- Level Selector (version final)
	- Funcionalidades
		- Navegación de la aplicación
		- Estructuración de la aplicación en Composeables, Activities y Services
		- Almacenamiento en local (Nicknames y Game State)
		- Almacenamiento externo (Firebase Firestore)
		- Integración con Firebase (OAuth y Firestore)
		- Mejoras UI/UX (Iconos, fuente, imágenes, i18n, figuras custom)
		- Primer juego de Unity con sensores
		- Integración Unity-Android
		- Guías para la integración del juego en [Android](https://github.com/Diego-a-lopez/ScapeTheAds/wiki/Gu%C3%ADa-para-embeber-juegos-de-Unity-(como-librer%C3%ADas)-en-Android-nativo)
		- Documentación
		- Puntuaciones globales
		- Arreglo de bugs
	- Minijuegos
		- Esquivar bloques
		- Cerrar cubos


## COO (Responsable de operaciones)
- Encargado: Juan Ramil Díaz
- Roles
	- Uso de sensores 
	- Validación funcional
	- Arquitectura Unity, integración de niveles
	- Documentación Unity
- Tareas realizadas
	- Pantallas
		- Level selection
		- Defeat
		- Victory
	- Funcionalidades
		- BombTimer: escena de Unity que controla el tiempo que transcurre hasta que se pierde el juego
		- GameHandler: escena que gestiona la carga de las distintas escenas de juegos. Aleatorización de la selección de niveles en el modo infinito. Selección de nivel concreto en el modo selección de nivel
		- Soporte en la creación del servicio de conexión con Unity (UnityBridge)
		- DataStore preferences: implementacion de DataStore para la gestión de las variables de los ajustes
	- Minijuegos
		-Compass game (brújula)



# Roles iniciales

## CEO – Director ejecutivo **(Diego Antonio López López)**
- CEO = Chief Executive Officer.
- Coordinación, representación.
- Gestión del ciclo de vida.
- Documentación general.
- Arquitectura e integración de submódulos.
- Testing.

Funcionalidades para Diego:

- Planeador de niveles, detección de los sensores del dispositivo y encolado de los niveles
- Level Mira al norte
- Level Omitir modo oscuro

## COO - Responsable de operaciones **(Daniel Silva Iglesias)**
- COO = Chief Operation Officer.
- Arquitectura.
- Validación funcional.

Funcionalidades para Daniel:

- Elemento de fondo, la bomba que "explota" si no reseteas el contador pulsando el botón
- Level Sopa de letras
- Level Omitir por detrás

## CTO - Responsable de tecnologías no-Android **(Juan Ramil Díaz)**
- CTO = Chief Technology Officer (nombrar segundo del CEO)
- Uso de sensores y hardware embebido.
- Geolocalización y posicionamiento.
- Integración de APIs de terceros.

Funcionalidades para Juan:

- Sistema de puntuación en base a la dificultad y velocidad de resolución del puzzle
- Level saca foto a objeto de color
- Level Rompe la pared
## CXO - Responsable de experiencia de usuario **(Daniel Silva Iglesias)**
- CXO = Chief Experience Officer.
- Usabilidad.
- Experiencia de usuario (UX): menús, feedback, contenido multimedia.
- Funcionalidades sociales.