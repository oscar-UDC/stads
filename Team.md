A continuación se detallan el reparto de roles y de funcionalidades para el desarrollo del proyecto. Las funcionalidades se reparten del siguiente modo: una tarea crítica y varios levels para cada uno. Se espera que la lista de levels cambie y aumente con el tiempo, en función de los requisitos de tamaño de la aplicación.

# Roles finales

## CEO (Director ejecutivo) y CXO (Responsable de experiencia de usuario)
- Encargado: Diego Antonio Lopez
- Roles
	- Testing
	- UI/UX
- Tareas realizadas
	- Pantallas
	- Funcionalidades
	- Minijuegos

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
		- Almacenamiento externo (Firebase Storage)
		- Integración con Firebase (OAuth y Storage)
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
- Tareas realizadas
	- Pantallas
	- Funcionalidades
	- Minijuegos



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