# Android Room

Para Android Room fue necesario coordinar las dependencias instaladas para no producir errores en el código. En concreto, se cambió Android Core:

```gradle
implementation(androidx.core:core-ktx:1.12.0) > implementation(androidx.core:core-ktx:1.9.0)
```

Y se añadieron las librerías de Android Room compatibles con ese Android Core:

```gradle
val room_version = "2.6.1"

implementation("androidx.room:room-runtime:$room_version")
annotationProcessor("androidx.room:room-compiler:$room_version")
implementation("androidx.room:room-ktx:$room_version")
kapt("androidx.room:room-compiler:$room_version")
```
