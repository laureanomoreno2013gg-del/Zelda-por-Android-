ZELDA OOT ANDROID — APK BUILDER

Este paquete NO es un APK. Contiene el workflow de GitHub Actions que compila el APK desde el código fuente Shipwright-Ports.

PASOS DESDE ANDROID:
1. Sube el contenido de tu proyecto Shipwright-Ports a un repositorio GitHub propio.
2. Copia este archivo:
   .github/workflows/build-android-apk.yml
   a la misma ruta dentro del repositorio.
3. Asegúrate de que también exista:
   .github/workflows/apt-deps.txt
   (ya viene en el ZIP original de Shipwright-Ports).
4. En GitHub, abre Actions.
5. Selecciona "Build Zelda OOT Android APK".
6. Pulsa "Run workflow".
7. Cuando finalice correctamente, abre el workflow y descarga el artefacto:
   Zelda-OOT-Android-ARM64-debug

El APK es una compilación debug ARM64 y se firma automáticamente con la clave de depuración de Android. No es una release oficial.

ROM Y DATOS:
- No se incluye ni se sube la ROM al repositorio.
- El workflow genera soh.o2r, que contiene datos internos del proyecto, no los datos completos del juego.
- Al iniciar el APK, importa desde la app los datos extraídos de tu propia copia compatible del juego.

IMPORTANTE:
- GitHub Actions debe estar habilitado para tu repositorio.
- El proyecto fuente debe conservar CMakeLists.txt, Android/, soh/, scripts/, patches/, docs/ y .github/workflows/apt-deps.txt.
- Los submódulos se descargan desde sus repositorios upstream durante la compilación.
- Si el workflow falla, comparte el primer error rojo del log para corregirlo.
