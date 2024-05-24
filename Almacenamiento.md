En la presente sesión, se abordará el tema de los componentes de la aplicación que requieren almacenamiento de datos, ya sea de forma local mediante Android Room para los datos de usuario y Datastore para las opciones de la aplicación, o a nivel global a través de Firebase para la gestión de la tabla de puntuaciones global.

## Almacenamiento local

**Android Room**

Dentro de Android Room, se almacena la puntuación local del usuario en la base de datos localscores.db. Esta base de datos contiene los siguientes registros:

- Nombre del usuario local que llevó a cabo la partida.
- Fecha de la partida.
- Puntuación obtenida en la partida.
- Duración de la partida.

**Datastore de configuración**

En cuanto al Datastore de Android, se guardan las opciones locales de la aplicación, que incluyen:

- Volumen de la aplicación.
- Idioma de la aplicación.
- Tema de color.

**Datastore de autenticacion**

También se alamcenará como una serie de claves valor la siguiente información:

- Clave: Id del usuario (obtenido mediante Firebase Auth)
- Valor: Nickname escogido por el usuario.

**Datastore de Unity**

Dado que Unity finaliza el proceso de la aplicación se pierde el estado por eso se ha decidido almacenar el ultimo estado del juego lo que permitirá a la aplicación enrutar al usuario a la pantalla adecuada (victoria, derrota, etc)

## Almacenamiento externo

**Firebase**

Por otro lado, en Google Firebase se gestionan los datos de puntuación a nivel global, los cuales son análogos a los registros de puntuación local:

- Nombre del usuario local que efectuó la partida.
- Fecha de la partida.
- Puntuación alcanzada en la partida.
- Duración de la partida.
