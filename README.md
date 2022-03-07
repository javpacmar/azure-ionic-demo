# azure-ionic-demo

- [1. Backend](#1-backend)
  - [1.1. NestJS](#11-nestjs)
- [2. Frontend](#2-frontend)
  - [2.1. Ionic](#21-ionic)
  - [2.2. Desarrollo de Ionic en Android](#22-desarrollo-de-ionic-en-android)
  - [2.3. Instalación del plugin `@capacitor/push-notifications`](#23-instalación-del-plugin-capacitorpush-notifications)
  - [2.4. Crear proyecto en Firebase Cloud Messaging (FCM)](#24-crear-proyecto-en-firebase-cloud-messaging-fcm)
  - [2.5. Uso del plugin push-notifications de Capacitor](#25-uso-del-plugin-push-notifications-de-capacitor)

## 1. Backend

### 1.1. NestJS

Paso 1: [Instalación de NestJS](https://docs.nestjs.com/)

```powershell
npm i -g @nestjs/cli
nest new project-name
```

Paso 2: Crear un nuevo endpoint para la notificación

## 2. Frontend

### 2.1. Ionic

Paso 1: [Instalación del CLI Ionic](https://ionicframework.com/docs/intro/cli#install-the-ionic-cli)

```powershell
npm install -g @ionic/cli
```

Paso 2: Crear el proyecto Ionic

```powershell
ionic start
cd ./project
npx cap init # Esto permite cambiar el nombre de la app y su id
```

### 2.2. Desarrollo de Ionic en Android

Para la creación de la app en Android he seguido el [tutorial](https://ionicframework.com/docs/developing/android).

Si a la hora de hacer build de la aplicación en Android Studio da fallo, usar en terminal `ionic capacitor sync android` y volver a buildear.

Cada vez que se quiera actualizar la aplicación de Android se debe ejecutar:

```powershell
ionic capacitor copy android
```

Si se quiere abrir el proyecto en Android Studio, se puede hacer por consola con:

```powershell
ionic capacitor open android
```

### 2.3. Instalación del plugin `@capacitor/push-notifications`

He seguido los pasos de la [web](https://capacitorjs.com/docs/apis/push-notifications).

```powershell
npm install @capacitor/push-notifications
npx cap sync
```

### 2.4. Crear proyecto en Firebase Cloud Messaging (FCM)

Para mandar las notificaciones en la API se usa Firebase Cloud Messaging de Google. Mirar las [instrucciones](https://firebase.google.com/docs/cloud-messaging/android/client) para crear un proyecto.

Agregar esta línea en las dependencias de gradle:

```java
implementation 'com.google.firebase:firebase-iid'
```

### 2.5. Uso del plugin push-notifications de Capacitor

Ejemplo que nos da la página [web de Capacitor](https://capacitorjs.com/docs/guides/push-notifications-firebase).
