# Desarrollo de Interfaces

## Parte 1: Selección de colores para la interfaz

Este es el primer paso para realizar la interfaz al completo. Este apartado consiste en definir una paleta base para tu interfaz.

### 1.1. Selección de los colores base

Comienza seleccionando un color principal, conocido como **color base**, que será un pilar del diseño. Este color debe elegirse en función de la interfaz que vayas a realizar, con el diseño del mismo. Una vez definido el color base, pasa a utilizar herramientas de selección de colores automáticas vistas en clase (Ej: www.coolors.co) para ampliar la paleta seleccionando tres colores adicionales:

- Un color secundario complementario al color base.
- Un color terciario complementario al color base y al secundario.
- Un color cuaternario complementario a estos últimos.

### 1.2. Creación de Paletas Monocromáticas

Una vez seleccionados los 4 colores iniciales, se pide que generes una **paleta monocromática** de cinco tonalidades por cada color. Estas tonalidades deben explorarse ajustando fundamentalmente el contraste para crear variaciones útiles en diferentes contextos de diseño.

Utiliza las herramientas vistas en clase (Ej: www.paletton.com) para generar estas paletas y realiza ajustes manuales si es necesario. Asegúrate de capturar los valores exactos de cada tonalidad (en formato HEX o RGBA).

### 1.3. Creación de Paletas de Gradientes

Pasamos a continuación a la generación de **2 paletas de gradientes** para la interfaz.

- **Gradientes para un overlay**: Crea un gradiente que pueda usarse como fondo semi-transparente en elementos superpuestos, como modales o filtros de imágenes.
  - El gradiente se conformará con una de las paletas monocromáticas creadas anteriormente, con proporción de los colores monocromáticos a vuestra elección.
  - Para crear el gradiente utiliza alguna de las herramientas vistas en clase (Ej: cssgradient.io).
  - Este gradiente deberá permitir que el contraste con respecto al texto de encima pase las pruebas de accesibilidad vistos en clase (Ej: webaim.org/resources/contrastchecker/ o coolcontrast.vercel.app).
  
- **Gradientes para un texto titular**: Diseña una paleta de gradientes que se aplicará al texto titular de la interfaz o el cual se quiera resaltar. Se pide que:
  - Los gradientes por realizar deben estar compuestos de la combinación (en la proporción y cantidad que estimes) de los 4 colores elegidos (con sus monocromáticos).

### 1.4. ACLARACIONES

- Recuerda que la selección de quien es el color primario, secundario y de acentuación final depende de la proporción total de color que finalmente apliques y elijas a la interfaz utilizando la regla **60-30-10**.
- Se recomienda que para las pruebas a la hora de observar cómo casan los diferentes colores (tanto en armonía como en contraste), generes una interfaz de prueba simple (div con algunos títulos, subtítulos, texto, imágenes, cartas o botones) para poder visualizar e ir probando como van a ir casando los diferentes colores. La proporción de color que elijas final determinará quien es tu color primario, secundario y de acentuación.
- Ten cuidado a la hora de estudiar el contraste. Asegúrate de que la selección final pase todos los test de contraste, utilizando las herramientas mencionadas (Ej: webaim.org/resources/contrastchecker/ o coolcontrast.vercel.app).
- El 4º color que has elegido, podrás no usarlo o usarlo también como un color adicional de acentuación si así lo consideras para tu interfaz.

---

## Parte 2: Selección de la tipografía para la interfaz

En este apartado se te pedirá la selección de **tipografías** de tu interfaz. Se desarrolla a continuación el paso a paso de cómo realizarlo.

### 2.1. Selección de Tipografías

- Elige una tipografía que utilizarás en los **títulos principales** de la interfaz. Esta fuente debe ser legible, atractiva y alineada con el propósito del diseño.
- Elige una segunda tipografía que complemente a la tipografía base. Esta fuente se utilizará en el **contenido principal**, como párrafos, subtítulos o elementos secundarios de la interfaz.

**Nota**: Utiliza herramientas como [fontjoy.com](https://fontjoy.com/) para analizar combinaciones armónicas.

### 2.2. Definición de Escalas Tipográficas

- Define una **escala tipográfica** con poco contraste entre los tamaños de texto, utilizando las herramientas vistas en clase ([baseline.is](https://baseline.is/tools/type-scale-generator/)).
- Define una segunda escala tipográfica, siendo esta una única escala mayor a la seleccionada anteriormente. Utiliza la misma herramienta para seleccionarla.

### 2.3. Variables para diseño tipográfico fluido

- Utilizando la herramienta [fluid-type-scale.com](https://www.fluid-type-scale.com/), genera los valores necesarios para que los tamaños de fuente se ajusten automáticamente según el tamaño de la pantalla.
- Configura los siguientes parámetros en la herramienta:
  - Base size: 16px (para interfaces pequeñas) y 19px (para interfaces grandes).
  - Minimum viewport width: 320px.
  - Maximum viewport width: 1440px.
- Copia los valores generados y guárdalos.

---

## Parte 3: Definición de Variables Globales en CSS

En este apartado, trabajarás en la configuración inicial de tu proyecto web, incluyendo la estructura de carpetas y la creación de un archivo específico para almacenar las **variables globales en CSS**.

### 3.1. Generación de la Estructura del Proyecto

Crea una carpeta para el proyecto con la siguiente estructura:

/assets/images
/assets/icons
/css/…
/pages/index.html
/pages/… (otros archivos HTML según las páginas de la interfaz)

- **/assets**: Contendrá los recursos multimedia necesarios para el proyecto, divididos en subcarpetas:
  - **/images**: Almacena imágenes usadas en la interfaz.
  - **/icons**: Almacena iconos específicos.
- **/css**: Almacena todos los archivos CSS relacionados con el proyecto.
- **/pages**: Almacena las páginas HTML del proyecto, comenzando con index.html.

### 3.2. Creación de Archivos CSS

En la carpeta **/css**, crea tantos archivos CSS como interfaces tengas en el proyecto. Por ejemplo, si tienes una interfaz para la página de inicio y otra para un formulario de contacto, deberás crear archivos como `home.css` y `contact.css`.

Además, crea un archivo adicional denominado `variables.css`. Este archivo será exclusivo para definir **variables globales de CSS** que puedan ser reutilizadas en todas las interfaces.

### 3.3. Definición de Variables Globales

En el archivo **variables.css**, agrega las siguientes categorías de variables globales:

- **Colores**: Define las variables de color relacionadas con la paleta creada en el apartado 1.1.
- **Tipografías**: Define variables para las fuentes seleccionadas y las escalas tipográficas generadas en el apartado 2.1 y 2.2. Para obtenerlas, haz uso de la página [Google Fonts](https://fonts.google.com/).
- **Espaciados**: Define cinco tipos de espaciados diferentes. Estos pueden ser utilizados para márgenes, paddings o separación entre elementos.

### 3.4. ACLARACIONES

- Para utilizar las variables globales en otros CSS, tendrás que utilizar la regla **@import**.

---

## Parte 4: Maquetación de la interfaz opción 1: Ficha de entrenador Pokémon

En esta sección se pedirá una primera interfaz relativa a la creación de una tarjeta personal de un entrenador Pokémon ficticio, donde muestra información sobre él, su equipo Pokémon, logros y habilidades.

### 4.1. Composición de la interfaz

- **Encabezado**:
  - Icono de una **pokeball** a elección.
  - Título que indique: **Ficha de Entrenador**.
  - Identificador del entrenador.
  
- **Sección "Sobre mí"**:
  - Presenta al entrenador Pokémon con una breve descripción (nombre, región de origen, especialidad, etc.).
  - Fondo con un gradiente que refleje la temática (por ejemplo, los colores del entrenador o su tipo favorito de Pokémon).
  - **Avatar del entrenador**. Una imagen del avatar del entrenador Pokémon.

- **Sección "Equipo Pokémon" con cartas**:
  - Muestra una carta por cada Pokémon en su equipo. Cada carta debe incluir:
    - Una imagen del Pokémon.
    - Nombre del Pokémon.
    - Tipo (por ejemplo: Agua, Fuego) (como tag).

- **Sección "Logros"**:
  - Lista o galería de insignias, torneos ganados o medallas obtenidas, utilizando íconos o imágenes pequeñas.

- **Pie de página**:
  - Enlaces a redes sociales y contacto del entrenador (ficticio o temático, como un correo @pokemon.com).

- **Fondo de la página**:
  - La tarjeta no deberá ocupar el 100% de la web, sino que deberá estar centrada.
  - El espacio restante se destinará a rellenarlo con una imagen como **background** aplicando un **overlay (gradiente)**.

### 4.2. Animaciones de la interfaz

- **Rotación**: El icono de la pokeball del Encabezado debe estar rotando.
- **Sheen**: Cada 10 segundos, de manera escalonada, todos los Pokémon de la sección **Equipo Pokémon** deben realizar la animación de sheen.
- **Ampliación**: Al hacer hover sobre los **Logros**, estos deben ampliarse.
