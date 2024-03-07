# Crear juego de Unity

Habilitáis el plugin de Android en Unity Hub

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/6587b72b-fc50-4c25-beae-7a065c78b424)

Poneis modo Android

En File > Build Settings

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/e976ccb2-d867-4dd4-99a0-4271150edd76)

Y hacéis el juego
# Exportar juego como aplicación de Android

En Build Settings otra vez lo configurais asi:

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/ebddddde-21ed-4ece-8ae0-052b315b27fb)

Abajo en player settings hay que cambiar mas cosas: 

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/4c00a1cd-2479-4075-8ed2-b696883690b5)

Poned exactamente eso

Y finalmente le dais a Export de la pantalla anterior
# Convertir juego de Android en librería

Abrid el proyecto de unity

Haceis build de gradle (el icono del martillo)

En la vista de Project vais a UnityLibrary > build > outputs > aar > unityLibrary-debug.aar

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/a2b82f53-fcd1-4016-9cb4-02050a4e2695)

Ese fichero es el juego
# Integrar con aplicación de Android Nativa

Copiais el .aar en la carpeta libs

Y para meterlo como dependencia:

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/dcdbd0e4-09a1-4719-9aba-37dc9b8a452f)

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/5ef7e57f-6380-488f-90fa-fc76904da7c0)

Y para lanzar el juego se hace con el intent:

![image](https://github.com/Diego-a-lopez/ScapeTheAds/assets/72018929/c759f52e-9af4-4827-87bf-d4b22a0b3fc1)

```java
val intent = Intent(this, UnityPlayerActivity::class.java)  
startActivity(intent)
```

Como Unity le llama siempre UnityPlayerActivity a su main si vamos a tener varias librerías de juegos es importante editar el nombre de la clase antes de hacer build de la librería