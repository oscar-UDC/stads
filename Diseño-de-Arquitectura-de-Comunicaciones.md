# Diseño de Arquitectura de Comunicaciones

## Identificar los subsistemas que conformarán el sistema global.

- GameMaster: Planificador de niveles para el modo estandar
- LevelSelector: Selector de niveles, permite jugar a un puzle en concreto en vez de jugar a niveles aleatorios en el juego principal 
- Levels: Puzles individuales. 
- Leaderboards: Servidor externo que almacena los records de los usuarios globalmente.
- MainMenu: Menu principal desde el que se puede acceder al modo estandar, selector de niveles, leaderboards y highscores, 
- Highscores: Base de datos local que almacena los records personales.

## Hacer el diseño a alto nivel de cómo se conectarán los diversos elementos.

![arquitectura](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/d7b1280a-474f-4054-af4a-1d03408315ad)
