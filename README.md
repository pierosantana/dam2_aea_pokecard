# Proyecto: Ficha de Entrenador Pokémon

## Parte 1: Selección de colores para la interfaz

Este es el primer paso para realizar la interfaz completa. En este apartado, se define una **paleta base** para la interfaz.

### 1.1. Selección de los colores base
Comienza seleccionando un **color principal** (color base), que será el pilar del diseño. Este color debe elegirse según la interfaz que vayas a realizar.

Una vez definido el color base, utiliza herramientas de selección de colores automáticas (Ej: [Coolors](https://coolors.co)) para ampliar la paleta, eligiendo tres colores adicionales:
- 🌟 Un **color secundario** complementario al color base.
- 🔶 Un **color terciario** complementario al color base y al secundario.
- 🔸 Un **color cuaternario** complementario a los anteriores.

### 1.2. Creación de Paletas Monocromáticas
Genera una **paleta monocromática** de cinco tonalidades para cada color seleccionado. Asegúrate de ajustar el contraste para crear variaciones útiles en diferentes contextos de diseño. 

Utiliza herramientas como [Paletton](https://paletton.com) para generar estas paletas y realiza ajustes manuales si es necesario.

### 1.3. Creación de Paletas de Gradientes
Genera **2 paletas de gradientes** para la interfaz:
- 🎨 **Gradientes para un overlay**: Crea un gradiente que pueda usarse como fondo semi-transparente en elementos como modales o filtros de imágenes. Utiliza alguna de las paletas monocromáticas creadas anteriormente.
- 🖋️ **Gradientes para un texto titular**: Diseña un gradiente para resaltar el texto titular de la interfaz. Los gradientes deben estar compuestos por una combinación de los 4 colores seleccionados.

### 1.4. Aclaraciones
- Recuerda usar la regla **60-30-10** para la proporción de colores en la interfaz.
- Para verificar el contraste, usa herramientas como [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) o [CoolContrast](https://coolcontrast.vercel.app).
  
## Parte 2: Selección de la tipografía para la interfaz

### 2.1. Selección de Tipografías
- ✍️ **Tipografía principal**: Elige una tipografía que se utilizará en los títulos principales. Debe ser legible y alineada con el propósito del diseño.
- 🖋️ **Tipografía secundaria**: Selecciona una fuente complementaria para el contenido principal, como párrafos y subtítulos. Puedes usar herramientas como [FontJoy](https://fontjoy.com) para analizar combinaciones armónicas.

### 2.2. Definición de Escalas Tipográficas
- **Escala tipográfica básica**: Define una escala con poco contraste entre tamaños de texto usando [Baseline](https://baseline.is/tools/type-scale-generator/).
- **Escala tipográfica mayor**: Crea una segunda escala con un tamaño mayor. Usa la misma herramienta para obtenerla.

### 2.3. Variables para diseño tipográfico fluido
Usa [Fluid Type Scale](https://www.fluid-type-scale.com/) para generar los valores de tamaños de fuente que se ajustarán automáticamente según el tamaño de la pantalla. Configura los siguientes parámetros:
- Base size: 16px (para interfaces pequeñas) y 19px (para interfaces grandes).
- Minimum viewport width: 320px.
- Maximum viewport width: 1440px.

## Parte 3: Definición de Variables Globales en CSS

### 3.1. Generación de la Estructura del Proyecto
Crea una carpeta para el proyecto con la siguiente estructura:

- **/assets**: Contendrá los recursos multimedia necesarios para el proyecto, divididos en subcarpetas:
  - **/images**: Almacena imágenes usadas en la interfaz.
  - **/icons**: Almacena iconos específicos.
- **/css**: Almacena todos los archivos CSS relacionados con el proyecto.
- **/pages**: Almacena las páginas HTML del proyecto, comenzando con index.html.


### 3.2. Creación de Archivos CSS
En la carpeta `/css`, crea archivos CSS para cada interfaz. Además, crea un archivo adicional denominado `variables.css` para almacenar las variables globales.

### 3.3. Definición de Variables Globales
En el archivo `variables.css`, define las siguientes variables:
- 🎨 **Colores**: Variables relacionadas con la paleta creada.
- 🖋️ **Tipografías**: Variables para las fuentes y escalas tipográficas.
- 📏 **Espaciados**: Define cinco tipos de espaciados para márgenes, paddings, etc.

### 3.4. Aclaraciones
Usa la regla `@import` para utilizar las variables globales en otros archivos CSS.

## Parte 4: Maquetación de la interfaz

### 4.1. Composición de la interfaz

#### **Encabezado**:
- ⚽ Icono de una **Pokébola** a elección.
- 🏷️ **Título**: "Ficha de Entrenador".
- 💳 **Identificador** del entrenador.

#### **Sección "Sobre mí"**:
- 📜 Breve descripción del entrenador: nombre, región de origen, especialidad, etc.
- 🎨 **Fondo con un gradiente** temático.
- 🧑‍⚖️ **Avatar** del entrenador.

#### **Sección "Equipo Pokémon"** con cartas:
- 🃏 Una carta por Pokémon, incluyendo:
  - 🖼️ **Imagen** del Pokémon.
  - 🏷️ **Nombre**.
  - 🔹 **Tipo** (por ejemplo: Agua, Fuego).

#### **Sección "Logros"**:
- 🏅 Lista de **insignias**, torneos ganados, medallas obtenidas.

#### **Pie de página**:
- 🌐 **Enlaces** a redes sociales y contacto del entrenador.

#### **Fondo de la página**:
- 🖼️ La tarjeta no ocupará el 100% de la página, sino que estará centrada.
- 🎨 El espacio restante se llenará con una **imagen de fondo** aplicando un overlay (gradiente).

### 4.2. Animaciones de la interfaz
- 🔄 **Rotación**: El icono de la Pokébola en el encabezado debe rotar.
- 🌟 **Sheen**: Cada 10 segundos, los Pokémon de la sección "Equipo Pokémon" deben realizar la animación de **sheen**.
- 🧑‍🎤 **Ampliación**: Al hacer hover sobre los logros, estos deben **ampliarse**.

---
