# 📱 Registro de Calificaciones — APK para Android

## ⚡ Opción 1: Build automático en GitHub (RECOMENDADO — sin instalar nada)

1. Crea un repositorio en GitHub (ej: `calificaciones-apk`)
2. Sube TODO el contenido de esta carpeta al repositorio
3. GitHub Actions compilará el APK automáticamente (~3 minutos)
4. Ve a tu repositorio → pestaña **"Releases"** → descarga el APK
   - O ve a **Actions** → último workflow → **Artifacts** → descarga `CalificacionesApp-debug`

## 🖥️ Opción 2: Compilar con Android Studio (local)

1. Instala [Android Studio](https://developer.android.com/studio)
2. Abre Android Studio → "Open an existing project" → selecciona esta carpeta
3. Espera que sincronice Gradle (~2 minutos, necesita internet la primera vez)
4. Menú: **Build → Build Bundle(s)/APK(s) → Build APK(s)**
5. El APK aparece en: `app/build/outputs/apk/debug/app-debug.apk`

## 📲 Instalación en Android

1. Copia el archivo `app-debug.apk` al teléfono/tablet (USB o WhatsApp)
2. En Android: **Ajustes → Seguridad** → activar **"Instalar apps desconocidas"**
3. Abre el APK desde el administrador de archivos
4. Toca **Instalar**

## ✅ Características de la app

- 📊 Registro de calificaciones por trimestre
- ✅ Control de asistencia con QR
- 📝 Reporte de tareas
- 🔗 Sincronización Tablet ↔ Laptop en tiempo real (al guardar)
- 💾 Funciona 100% offline — datos guardados localmente en el dispositivo
- 🔄 Auto-limpieza de IDs de sincronización obsoletos

## 📁 Estructura del proyecto

```
CalificacionesApp/
├── .github/workflows/build-apk.yml   ← Build automático en GitHub
├── app/
│   ├── src/main/
│   │   ├── assets/index.html          ← La app completa (HTML+JS)
│   │   ├── java/.../MainActivity.java ← WebView wrapper
│   │   ├── res/                       ← Iconos y recursos
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── build.gradle
├── settings.gradle
└── gradle.properties
```
