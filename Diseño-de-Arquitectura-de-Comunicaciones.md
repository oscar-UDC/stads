# Diseño de Arquitectura de Comunicaciones

## Identificar los subsistemas que conformarán el sistema global.

- GameMaster: Planificador de niveles para el modo estandar
- LevelSelector: Selector de niveles, permite jugar a un puzle en concreto en vez de jugar a niveles aleatorios en el juego principal 
- Levels: Puzles individuales. 
- Leaderboards: Servidor externo que almacena los records de los usuarios globalmente.
- MainMenu: Menu principal desde el que se puede acceder al modo estandar, selector de niveles, leaderboards y highscores, 
- Highscores: Base de datos local que almacena los records personales.
- Autenticación: Permite recuperar los datos de usuarios para mantener el progreso en caso de desinstalar, instalar en otro dispositivo
- Gestion de sensorica: Para independizar la aplicación de los posibles cambios de sensores entre diferentes teléfonos se dispondrá de una clase intermediaria para su gestión. Sensores a gestionar:
	* Camara
	* Brújula
	* Giroscopio
	* Acelerómetro

## Hacer el diseño a alto nivel de cómo se conectarán los diversos elementos.

![arquitectura](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/44831e84-0d11-413f-ab76-3e414717743b)
