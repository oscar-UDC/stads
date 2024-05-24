# Autenticación - Firebase Authentication

Vamos a integrar el sistema de autenticación de Firebase en nuestra aplicación

Firebase permite autenticarse de varias maneras

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/71b4576b-539d-4538-9626-73c6de3d3adf)

En nuestro caso vamos a utilizar la autenticación de Google, pero vamos a dejar habilitados los sistemas de autenticación mediante correo y contraseña y en modo anónimo por si son necesarios en un futuro

# Almacenamiento externo - Firebase Firestore

También vamos a usar la base de datos NoSQL que nos ofrece Firebase. 

En la base de datos vamos a almacenar los highscores de los usuarios de nuestra aplicación. Tambien servirá de registro de los nicknames que ya han sido escogidos ya que cuando un usuario establece su nickname se generará un nuevo highscore en esta base de datos con puntuación 0.

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/272254bd-7cde-4704-9440-5b3c61b72d94)



