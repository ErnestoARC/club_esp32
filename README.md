# CLUB ESP32 🤖

## Bienvenidos al Club de Programación ESP32 🎉

Este club de programación tiene la finalidad de reunir unidades de procesamiento humanas con el objetivo de adquirir conocimientos para la programación del microcontrolador **ESP32**. Este dispositivo presenta características óptimas para el desarrollo de proyectos relacionados con automatización de sistemas y conectividad inteligente.

La interacción dentro del club será gestionada en un entorno colaborativo, donde las unidades humanas podrán intercambiar información, optimizar procesos de aprendizaje y ejecutar proyectos de manera eficiente. El progreso será autogestionado, asegurando una adquisición incremental de conocimiento.

Nivel de experiencia: irrelevante. El objetivo principal es aumentar la capacidad de procesamiento y aprendizaje en un entorno grupal.

## Prerrequisitos Hardware ⚙️

Antes de comenzar a programar con el ESP32, es importante asegurarse de contar con los siguientes elementos de hardware:

1. **Placa de desarrollo ESP32**: Cualquier modelo compatible (como ESP32-WROOM-32, ESP32-S3, etc.).
2. **Cable USB**: Para conectar la placa ESP32 a tu computadora y cargar los programas.
3. **Computadora**: Con sistema operativo compatible (Windows, macOS o Linux) y puertos USB disponibles.
4. **Protoboard y cables**: Para realizar conexiones rápidas y probar componentes externos como sensores y LEDs.
5. **Componentes electrónicos adicionales (opcional)**: Sensores, botones, LEDs, resistencias, y otros periféricos que requiera cada proyecto acá publicado.

## Prerrequisitos Software 💻

1. **[Python 3.x](https://www.python.org/)** 🐍: Algunas herramientas de programación y carga de firmware del ESP32 dependen de Python, por lo que es necesario instalar esta versión del lenguaje en el sistema anfitrión. 

    * **Verificar que python está instalado** - En una terminal ejecutar el comando: *python3 --version*
    * Si el computador no reconoce que python está instalado, se recomienda instalar desde la appStore de windows o siguiendo las instrucciones descritas en el sitio web oficial de python. En caso de usar macOS, es necesario despues de instalar python, ejecutar "*Install Certificates.command*" desde el centro de aplicaciones del sistema operativo

2. **[GIT 3.x](https://git-scm.com/)** 🐙: Sistema de control de versiones distribuido, indispensable para la gestión del código fuente y la colaboración en proyectos de programación.

    * **Configurar nombre de usuario git**: En una terminal ejecutar el comando: *git config --global user.name "ejemplo"*
    * **Configurar email de usuario git**: En una terminal ejecutar el comando: *git config --global user.email ejemplo@gmail.com*
    * **Verificar cuenta de usuario git**: En una terminal ejecutar el comando: *git config --list*

3. **[ESPRESSIF-IDE + ESP-IDF](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/windows-setup.html)** 🛠️: Framework oficial para desarrollar aplicaciones en el ESP32. **Espressif IDE** es una plataforma de desarrollo oficial basada en Eclipse que facilita el trabajo con ESP-IDF.

    * **Configurar ESP-IDF** - Despues de instalar, iniciar el Espressif-IDE y usar el ESP-IDF Manager para activar una o más versiones de ESP-IDF en el entorno Espressif-IDE.

4. **[Visual Studio Code + ESP-IDF](https://code.visualstudio.com/)** 🛠️: 

    * **Descarga e instala Visual Studio Code**

    * **Instala los requisitos del sistema de ESP-IDF según tu sistema operativo**

        * [Windows]((https://visualstudio.microsoft.com/es/visual-cpp-build-tools/)): Puede ser necesario instalar las herramientas de compilación de C++. 
        * [macOS](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/macos-setup.html#install-prerequisites): Verifica que tu sistema tenga instalados los paquetes necesarios.
        * [Linux](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/linux-setup.html#install-prerequisites): Verifica que tu sistema tenga instalados los paquetes necesarios.

    * **Instalar extensión ESP-IDF**: En Visual Studio Code, abre la vista de extensiones haciendo clic en el ícono de extensiones en la barra de actividad a un lado de la ventana de Visual Studio Code, o utiliza el comando Ver: Extensiones (atajo: ⇧ ⌘ X o Ctrl+Shift+X)

    * **Configurar ESP-IDF**: En el icono de "ESP-IDF Explorer" en la barra lateral del Visual Studio Code, dar clic y seguir los pasos de instalación express.

## Versionado 📌

Para nombrar las diferentes versiones de los diferentes paquetes de codigo encapsulados en este repositorio, se utiliza [SemVer](http://semver.org/).

El versionado **SemVer** (Semantic Versioning) es un sistema utilizado para gestionar y comunicar los cambios en el software de manera clara y coherente. Este sistema se basa en un esquema de numeración que consta de tres componentes: **MAJOR.MINOR.PATCH**. 

- **MAJOR**: Incrementa cuando se realizan cambios incompatibles en la API.
- **MINOR**: Incrementa cuando se añaden funcionalidades de manera retrocompatible.
- **PATCH**: Incrementa cuando se realizan correcciones de errores de manera retrocompatible.

Este enfoque permite a los desarrolladores y usuarios entender rápidamente el impacto de una nueva versión, facilitando la gestión de dependencias y la integración de cambios. La adopción de SemVer promueve buenas prácticas en el desarrollo de software y mejora la comunicación entre equipos y usuarios.

## Gestión de Ramas Git 🌿

En este proyecto, utilizaremos un enfoque GitFlow simplificado para la gestión de ramas en este repositorio. Solo existirán dos ramas permanentes: **develop** y **main**. La rama **main** contendrá la versión estable del proyecto, mientras que **develop** se utilizará para integrar los cambios y desarrollos en curso. Para el desarrollo de nuevas funciones y proyectos, crearemos ramas de **feature**, que se basarán en **develop**. Una vez que se complete el desarrollo en estas ramas, se realizarán fusiones a **develop** para su revisión y pruebas, garantizando así un flujo de trabajo organizado y eficiente. Las ramas intermedias como **hotfix** y **release**, no serán usadas.

## Convenciones 📜

Para mantener la claridad y la coherencia en nuestro proyecto de lenguaje C, adoptaremos las siguientes convenciones de nombres para diversos elementos: 

1. **Nombres de ramas repositorio** *snake_case*: Nombres en minúsculas y separados por guiones bajos. Usar prefijos para organizar las ramas **feature/**, ejemplos :

    * **feature/usb/hid**: Nueva rama creada para desarrollar un proyecto ejemplo de conectividad usb modo HID
    * **feature/usb/cdc**: Nueva rama creada para desarrollar un proyecto ejemplo de conectividad usb modo CDC
    * **feature/freertos/semaphores**: Nueva rama creada para desarrollar un proyecto ejemplo de FreeRTOS y manejo de semaforos

2. **commits**:  usar la convencion [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/)

    * **feat**: cuando se añade una nueva funcionalidad.
    * **fix**: cuando se arregla un error.
    * **chore**: tareas rutinarias que no sean específicas de una feature o un error como por ejemplo añadir contenido al fichero .gitignore o instalar una dependencia.
    * **test**: si añadimos o arreglamos tests.
    * **docs**: cuando solo se modifica documentación.
    * **build**: cuando el cambio afecta al compilado del proyecto.
    * **ci**: el cambio afecta a ficheros de configuración y scripts relacionados con la integración continua.
    * **style**: cambios de legibilidad o formateo de código que no afecta a funcionalidad.
    refactor: cambio de código que no corrige errores ni añade funcionalidad, pero mejora el código.
    * **perf**: usado para mejoras de rendimiento.
    * **revert**: si el commit revierte un commit anterior. Debería indicarse el hash del commit que se revierte.


3. **Nombres de carpetas** *snake_case*: Nombres en minúsculas y separados por guiones bajos (por ejemplo, `src`, `include`, `lib`).

4. **Nombres de archivos** *snake_case*: Al igual que las carpetas, los nombres de los archivos serán en minúsculas y usarán guiones bajos para separar las palabras, con la extensión correspondiente, como `.c` para archivos de código y `.h` para archivos de encabezado (por ejemplo, `mi_archivo.c`, `mi_archivo.h`).

5. **Nombres de variables** *snake_case*: minúsculas y usarán guiones bajos para separar las palabras (por ejemplo, `numero_de_intentos`, `valor_maximo`).

6. **Nombres de constantes** *k_snake_case*: iniciando con la letra k seguido de guiones bajos para separar las palabras (por ejemplo, `k_quectel_comando_at1`, `k_constante_pi`).

7. **Nombres de DEFINE** *UPPER_CASE_SNAKE_CASE*: Las macros se definirán en mayúsculas con palabras separadas por guiones bajos, facilitando su identificación (por ejemplo, `MAX_BUFFER_SIZE`, `ENABLE_FEATURE`).

8. **Nombres de funciones** *camelCase*: Comenzando con minúscula y capitalizando la primera letra de cada palabra subsiguiente (por ejemplo, `numeroDeIntentos`, `valorMaximo`).


## Estructura de Carpetas 📂

La estructura de carpetas está diseñada para organizar de manera eficiente los diferentes componentes del código. La siguiente disposición es recomendada: 

- **src/**: Esta carpeta contendrá todos los archivos de código fuente `.c` que implementan la lógica del programa.
- **include/**: Aquí se almacenarán los archivos de encabezado `.h`, que declararán las funciones y estructuras utilizadas en los archivos de código fuente.
- **lib/**: Esta carpeta se utilizará para incluir bibliotecas externas o personalizadas que el proyecto requiera.
- **bin/**: En esta carpeta se almacenarán los archivos ejecutables generados tras la compilación del proyecto.
- **tests/**: Aquí se incluirán los archivos relacionados con las pruebas, como los scripts de prueba y los archivos de configuración.
- **docs/**: Esta carpeta contendrá la documentación del proyecto, incluyendo guías de usuario, descripciones de la API y cualquier otro material relevante.

## Contribuciones al Proyecto 🤝

Para contribuir al proyecto, es necesario solicitar permisos como colaborador. Es fundamental mantener las reglas descritas en este documento y actuar siempre con el ánimo de aportar buenas ideas que fomenten el crecimiento y desarrollo del proyecto. Valoramos las contribuciones constructivas y alentamos a todos a participar de manera activa y positiva. Juntos, podemos hacer de este proyecto una iniciativa exitosa y enriquecedora para todos los involucrados.


## Licencia 📄

Este proyecto se distribuye bajo la licencia **MIT**. Esto significa que puedes usar, copiar, modificar y distribuir el código fuente de manera libre, siempre que incluyas el aviso de copyright y la declaración de licencia en todas las copias o partes sustanciales del software. La licencia MIT es una de las más permisivas y permite el uso del proyecto en proyectos comerciales y no comerciales, fomentando así la colaboración y el intercambio de conocimientos en la comunidad.

## Autores ✒️

Esta es la lista de todos los colaboradores de este proyecto:

* **[Ernesto](https://github.com/ErnestoARC)**
* **[Felipe]()**
* **[Santiago]()**
* **[Edward]()**
* **[Victor]()**
* **[Gustavo]()**
* **[Luz]()**

## Expresiones de Gratitud 🎁

* Invita una cerveza 🍺 o un café ☕ a alguien del equipo. 
* Respeta los comentarios en los archivos .h y .c para mantener el origen de la información y sus autores