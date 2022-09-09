<p align="center">
    <a href="https://webdriver.io/">
        <img alt="WebdriverIO" src="https://webdriver.io/assets/images/robot-3677788dd63849c56aa5cb3f332b12d5.svg" width="146">
    </a>
</p>

## Starter project basado en [WebDriverIO](https://webdriver.io/), [Appium](http://appium.io/), [Cucumber](https://cucumber.io/), [TypeScript](https://www.typescriptlang.org/), [Allure Report](https://docs.qameta.io/allure-report/), [Node.js](https://nodejs.org/en/)

### Requerimientos generales

- Instalar [Node.js](https://nodejs.org/es/download/)
- Instalar algún cliente git como por ejemplo [git bash](https://git-scm.com/downloads)
- Tener instalado Chrome 100 o la version del chrome del navegador(No Chromium)

### Requerimientos mobile

Descargar e instalar

- Java Development Kit [(JDK)](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133155.html)
  - Asegurarse de tener configurada la variable de entorno **JAVA_HOME** con la ruta de la JDK respectiva.
- [Appium](https://appium.io/downloads/) Desktop.
- [Android Studio](https://developer.android.com/studio/index.html) y dentro de la aplicación instalar.
  - **SDK Platform**: Android 10 o la versión necesaria.
  - **SDK tools**:
    - Android SDK Build Tools.
    - Andorid SDK Command Line Tools.
    - Android Emulator.
    - Android SDK Platform-tools.
    - Intel x86 Emulator accelerator.
  - Configurar al menos un emulador desde **Android Virtual Device Manager**.
  - Asegurarse de agregar las siguientes variables de entorno:
    - **ANDROID_HOME**: Agregar el directorio donde se aloja la SDK de Android, por ejemplo: *C:\Users\USERNAME\AppData\Local\Android\Sdk*.
    - Luego respetando el orden agregar estas variables de entorno:
      - **%ANDROID_HOME%**\emulator
      - **%ANDROID_HOME%**\platform-tools
      - **%ANDROID_HOME%**\tools
      - **%ANDROID_HOME%**\tools\bin
  - Iniciando el emulador desde la línea de comandos:
    - Listar los emuladores instalados:
      - emulator -list-avds
    - Iniciar el emulador:
      - emulator @nombre_emulador
    - Como alternativa a algún error se puede iniciar con el siguiente comando: **%ANDROID_HOME%**\emulator\emulator.exe -avd <nombre_emulador>
- **Appium Doctor**: Para validar que contamos con todo lo necesario para realizar nuestros Test de mobile debemos instalar y ejecutar.

  - npm install -g appium-doctor
    - Esto instalará el utilitario que nos permitirá validar que todo esté correctamente configurado.
  - appium-doctor --android
    - Si hemos realizado correctamente todos los pasos de arriba con este comando se mostrará un mensaje de éxito ya algunos warning.
    - En caso de algún error bloqueante, el mismo se mostrará en pantalla, se deberá corregir y volver a ejecutar hasta que esté todo ok.

- APK a probar.
  - Usamos para el ejemplo [la apk](https://github.com/webdriverio/native-demo-app/releases/download/v0.4.0/Android-NativeDemoApp-0.4.0.apk) provista por WebdriverIO.
  - Pueden ejecutar desde la línea de comandos lo siguiente como alternativa:
    - curl <https://github.com/webdriverio/native-demo-app/releases/download/v0.4.0/Android-NativeDemoApp-0.4.0.apk> --output Android-NativeDemoApp-0.4.0.apk
  - Para que el ejemplo funcione la apk debe estar dentro de la carpeta **/app** en la base de nuestro proyecto con el nombre configurado en la capability **app** del archivo [*config/wdio.mobile.conf.ts*](config/wdio.mobile.conf.ts).

### Instalación del framework de pruebas

#### **Clonar el repositorio:**

```bash

```

#### **Instalar las dependencias.**

```bash
npm install
```

#### **Para la ejecución de los test de web**

```bash
    npm run wdio-web
```

#### **Para la ejecución de los test de web usando docker**

```bash
    npm run wdio-web-docker
```

#### **Para la ejecución de los test de mobile**

```bash
    npm run wdio-mobile
```

#### **Para ejecutar el asistente de configuración (opcional para usar otros browsers o servicios):**

```bash
    npm init wdio .
```

#### **Para crear y abrir el reporte unificado de los resultados de los test**

```bash
    npm run open-report
```
