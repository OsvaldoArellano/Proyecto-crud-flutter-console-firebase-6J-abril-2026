Configurar Firebase CLI para Flutter es un paso esencial para automatizar la vinculación de tus apps sin tener que configurar manualmente archivos JSON o Plist. Aquí tienes la hoja de ruta clara para lograrlo.

---

## 1. Software Necesario y Preparación
Para manejar el CLI de Firebase, el motor principal es **Node.js**, el cual incluye automáticamente **npm** (Node Package Manager).

### ¿Cómo verificar si ya tienes Node.js y npm?
Abre tu terminal (PowerShell, CMD o Terminal de macOS/Linux) y escribe:
* `node -v`
* `npm -v`

> **Versión recomendada:** Se sugiere utilizar la versión **LTS (Long Term Support)** de Node.js (actualmente la v20 o v22), ya que ofrece la mayor estabilidad para herramientas de desarrollo.

---

## 2. Instalación de Node.js y npm (Paso a Paso)
Si los comandos anteriores no devolvieron una versión, sigue estos pasos:

1.  **Descarga:** Ve al sitio oficial [nodejs.org](https://nodejs.org/).
2.  **Instalador:** Descarga el instalador para tu sistema operativo (Windows .msi, macOS .pkg).
3.  **Configuración:** Ejecuta el instalador. Asegúrate de que la casilla **"Add to PATH"** esté marcada (esto permite usar los comandos de forma global).
4.  **Finalización:** Reinicia tu terminal para que reconozca los nuevos comandos.

---

## 3. Instalación Global de Firebase CLI
Una vez que `npm` funciona, instalaremos las herramientas de Firebase de forma global para que puedas usarlas en cualquier carpeta de tu computadora.

**Comando de instalación:**
```bash
npm install -g firebase-tools
```
*El flag `-g` indica que la instalación es **global**.*

---

## 4. Comandos de Uso Frecuente (Firebase Tools)

### A. Acceder con tu cuenta de Google
Para vincular tu terminal con tu consola de Firebase:
```bash
firebase login
```
* Esto abrirá una ventana en tu navegador. Selecciona tu cuenta de Google y acepta los permisos.
* Si ya iniciaste sesión y quieres cambiar de cuenta, usa `firebase logout` y luego `firebase login`.

### B. Implementación en un Proyecto (Inicialización)
Para preparar tu directorio local y conectarlo con un proyecto en la consola:
1.  Navega en la terminal hasta la carpeta raíz de tu proyecto Flutter.
2.  Ejecuta:
```bash
firebase init
```
* **Selección:** Usa las flechas y la barra espaciadora para elegir qué servicios usarás (Firestore, Functions, Hosting, etc.).
* **Proyecto:** Elige "Use an existing project" y selecciona el proyecto que ya creaste en la Console Firebase.

---

## 5. Integración Específica con Flutter (FlutterFire CLI)
Aunque ya tengas Firebase CLI, Flutter requiere un paso adicional para generar el archivo de configuración `firebase_options.dart`.

1.  **Instala el activador de Dart:**
    ```bash
    dart pub global activate flutterfire_cli
    ```
2.  **Configura el proyecto:**
    Desde la raíz de tu proyecto Flutter, corre:
    ```bash
    flutterfire configure
    ```
    Este comando te preguntará qué plataformas quieres soportar (Android, iOS, Web) y registrará automáticamente las apps en tu consola de Firebase, descargando los identificadores necesarios.



---

### Resumen de Comandos Rápidos
| Acción | Comando |
| :--- | :--- |
| Instalar CLI | `npm install -g firebase-tools` |
| Iniciar Sesión | `firebase login` |
| Vincular Proyecto | `firebase init` |
| Configurar Flutter | `flutterfire configure` |
| Listar Proyectos | `firebase projects:list` |

¿Ya tienes creado tu proyecto en la consola web de Firebase o necesitas que te guíe en la creación desde el navegador?
