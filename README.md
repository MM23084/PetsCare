# PetsCare

Aplicación Android para el cuidado y registro de mascotas.

Resumen
-------
PetsCare es una aplicación Android (Java) creada para registrar mascotas, sus datos principales y recordatorios básicos (vacunas, citas, notas). El proyecto fue desarrollado originalmente durante el bachillerato y ahora planeas retomarlo y mejorarlo.

Estado
------
- Lenguaje principal: Java
- Plataforma: Android (Android Studio / Gradle)
- Repositorio: MM23084/PetsCare

Características principales
--------------------------
- Registrar y editar mascotas (nombre, especie/raza, edad, notas)
- Listado de mascotas con acceso a detalles
- Registro de recordatorios simples (vacunas, consultas)
- Interfaz básica con Activities y layouts en XML

Capturas
--------
(Agrega capturas a la carpeta `screenshots/` y actualiza las rutas aquí)
- screenshots/home.png
- screenshots/pet_detail.png
- screenshots/add_pet.png

Requisitos
----------
- Android Studio (recomendado la versión estable más reciente)
- JDK 8/11 (según configuración del proyecto)
- Gradle (usa el Gradle Wrapper incluido: `./gradlew`)
- Emulador o dispositivo Android (revisa el `minSdkVersion` en `app/build.gradle`)

Instalación y ejecución
-----------------------
1. Clona el repositorio:
   git clone https://github.com/MM23084/PetsCare.git
   cd PetsCare

2. Abre el proyecto en Android Studio:
   - File → Open... → selecciona la carpeta del proyecto.
   - Espera a que sincronice Gradle y descargue dependencias.

3. Ejecuta la app:
   - Desde Android Studio: Run (Play) en un emulador o dispositivo.
   - Línea de comandos:
     ./gradlew assembleDebug
     ./gradlew installDebug   # instala en dispositivo/emulador conectado
   - En Windows usa `gradlew.bat` en vez de `./gradlew`.

Estructura recomendada del proyecto
----------------------------------
- app/
  - src/
    - main/
      - java/... (Activities, Adapters, modelos)
      - res/ (layouts, drawables, values)
      - AndroidManifest.xml
  - build.gradle (módulo)
- build.gradle (root)
- gradle/ (wrapper)
- screenshots/ (opcional: capturas)
- README.md

Buenas prácticas sugeridas
--------------------------
- Trabajar en branches por feature: `feature/<nombre-feature>`
- Commits pequeños y descriptivos
- Pull requests para revisiones antes de merge
- Añadir tests unitarios y de UI (JUnit, Espresso)

Mejoras propuestas (prioriza según tiempo)
------------------------------------------
Alta prioridad
- Persistencia local con Room (SQLite)
- Notificaciones para recordatorios programados
- Guardado y carga de imágenes de mascotas (storage local o Firebase Storage)

Media prioridad
- Reorganizar a arquitectura MVVM (ViewModel + LiveData)
- Validaciones y mejor manejo de errores
- Internacionalización (es/EN) y soporte a accesibilidad

Baja prioridad / Extra
- Migración parcial o total a Kotlin
- Integración con Firebase (autenticación, sincronización)
- Tests automáticos y CI (GitHub Actions)

Recuperación del código perdido (comandos útiles)
-------------------------------------------------
Si trabajaste localmente y crees que perdiste commits:
- git reflog          # busca referencias locales recientes
- git fsck --lost-found
- git checkout -b recover/<fecha> <sha>  # si encuentras el sha adecuado

Si solo tienes un APK antiguo:
- Puedes extraer recursos con herramientas como `apktool` (último recurso).

Licencia
--------
Si no tienes preferencia, recomiendo MIT. Puedo añadir un `LICENSE` con el texto si quieres.

Cómo contribuir
---------------
1. Crea una branch por cada feature o bugfix: `git checkout -b feature/nombre`.
2. Haz commits claros.
3. Abre PRs pequeños para revisión.
4. Usa issues para planificar tareas.

Contacto
--------
Proyecto por: MM23084

Notas finales
-------------
He creado este README de base; puedo:
- Añadirlo al repositorio en una branch y abrir un PR por ti.
- Generar una lista de issues con las mejoras priorizadas.
- Analizar el código fuente del repo si me das acceso para generar un plan de migración (Room, MVVM, tests).
