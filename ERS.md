# ESPECIFICACIÓN DE REQUISITOS DE SOFTWARE (ERS)
## Proyecto: Sistema Web para Gestión del Festival Estudiantil CampusFest

---

### 1. INTRODUCCIÓN Y DESCRIPCIÓN GENERAL
El sistema CampusFest proveerá una solución web integral full-stack para mitigar los problemas de la gestión manual del festival anual (inscripciones duplicadas, cupos excedidos y desorganización de la agenda.)
Centralizará la información para usuarios visitantes y administradores

---

### 2. REQUISITOS DE DISEÑO E IMPLEMENTACIÓN (RESTRICCIONES)
**Tecnologías Obligatorias (Etapa 1):** HTML5, CSS3, JavaScript Vanilla y Framework Bootstrap.
**Diseño Responsivo:** Menú horizontal y distribución multi-columna en escritorio; menú colapsable y tarjetas en una sola columna en móviles.
**Control de Estilos y Interfaz:**
**Libro de Marca:** Uso estricto de la paleta de colores y tipografía oficial de la Universidad CENFOTEC.
**Modo Oscuro/Claro:** Implementación obligatoria mediante Media Queries propias configuradas para adaptarse automáticamente según las preferencias del sistema operativo del usuario.
**Accesibilidad Web:**
    * Inclusión visual para personas con baja visión, ceguera y daltonismo.
    * Uso de elementos iconográficos claros en la interfaz para la correcta comprensión de personas sordas.

---

### 3. ESPECIFICACIÓN DE REQUISITOS FUNCIONALES (ETAPA 1)

#### RF-FE-01: Página de Inicio (Home)
* **Descripción:** La página principal del sitio web debe servir como la ventana de presentación del festival estudiantil.
* **Elementos obligatorios en pantalla:**
    1. Nombre oficial del festival ("CampusFest").
    2. Descripción breve del evento y fecha general de realización.
    3. Ubicación o lugar principal de las actividades.
    4. Sección destacada en cuadrícula (grid) que muestre de forma visual las **3 actividades principales** del festival.
    5. Elementos de navegación interactivos: Un botón/enlace directo hacia el catálogo de actividades y un botón/enlace directo al formulario de inscripción.

#### RF-FE-02: Página de Actividades (Catálogo Visual)
* **Descripción:** Interfaz que despliega de forma dinámica y visual la totalidad de los eventos disponibles organizados mediante tarjetas (cards).
* **Estructura de cada Tarjeta (Card):**
    * Nombre de la actividad y Categoría (Cultural, Deportiva, Tecnológica, Artística, Gastronómica o Recreativa).
    * Fecha, hora y lugar específico donde se llevará a cabo.
    * Indicador visual de cupo disponible simulado.
    * Botón interactivo de "Ver detalle" que redirija a la ficha técnica de la actividad.

#### RF-FE-03: Página de Detalle de Actividad
* **Descripción:** Vista detallada de una actividad específica seleccionada por el usuario visitante.
* **Información en pantalla:**
    * Nombre de la actividad, descripción completa y categoría correspondiente.
    * Fecha, hora exacta y lugar asignado.
    * Requisitos de participación particulares de la actividad.
    * Cupo máximo total (definido previamente por el administrador).
    * **Lógica de Cupos y Lista de Espera:** El sistema debe evaluar el cupo simulado. Si hay disponibilidad, se muestra un botón para proceder a la inscripción. Si el cupo está en 0, el sistema debe lanzar una **alerta visual** de disponibilidad agotada y cambiar el comportamiento del botón para permitir un registro bajo la condición de **"Lista de espera"** para posterior confirmación.