# Estructuras de Datos y Algoritmos

## Lenguaje: `JavaScript`

### Configuración de Carpetas y Challenges

Cada tipo de code challenge tiene instrucciones ligeramente diferentes. Consulta las notas y ejemplos a continuación para ver las instrucciones de cada tipo de tarea de DS&A.

### Estructura de Datos: Nueva implementación

- Crea una nueva carpeta dentro de `javascript`, con el nombre de la estructura de datos y completa tu implementación allí
  - p.ej., `linked-list`
- Implementación (la estructura de datos "clase")
  - La implementación de la estructura de datos debe llamarse `index.js`
  - Tu implementación se debe completar como una Clase ES6 adecuada y exportarse como un módulo de node
    - El nombre de la clase debe ser `ProperCase`
    - Los métodos de clase deben ser `camelCase`

    ```javascript
    class LinkedList {
      constructor() {
        // código
      }

      methodName() {
        // código
      }

    }
    module.exports = LinkedList;
    ```

- Tests
  - Crea una carpeta llamada `__tests__` y dentro de ella crea un archivo de test llamado `[data-structure].test.js`
    - p.ej. `__tests__/linked-list.test.js`
    - Tus test deberán requerir la estructura de datos que estás testeando
      - p.ej., `const LinkedList = require('../índice');`

### Estructura de Datos: Ampliación de una implementación

- Trabaja dentro de la implementación de la estructura de datos
- Crea un nuevo método dentro de la clase que resuelva el code challenge
  - Recuerda, tendrás acceso a `this` dentro de tus métodos de clase
- Tests
  - Tendrás una carpeta llamada `__tests__` y dentro de ella, un archivo de test llamado `[data-structure].test.js`
    - p.ej. `__tests__/linked-list.test.js`
    - Añade más a los tests ya escritos para esta estructura de datos para abarcar tu(s) nuevo(s) método(s)

### code challenge / Algoritmo

Los code challenges deben completarse dentro de una carpeta llamada `code-challenges` la cual está dentro de `javascript`

- Configuración Diaria:
  - Crea una nueva carpeta dentro de `javascript`, con el nombre del code challenge
    - Cada tarea de code challenge identifica el nombre de la rama que se va a utilizar, por ejemplo, 'find-maximum-value'
    - Para mayor claridad, crea tu carpeta con el mismo nombre, asegurándote de que esté en `kebab-case`
    - p.ej., para un challenge llamado 'find-maximum-value', crea la carpeta: `code-challenges/find-maximum-value`
  - Implementación del code challenge
    - Cada code challenge necesita que se escriba una función, por ejemplo, "find maximum value"
    - Nombra el archivo con el nombre del challenge, en `kebab-case`
      - p.ej., `find-maximum-value.js`
    - Recordatorio: Tu archivo de challenge necesitará la estructura de datos que estás utilizando para implementarla
      - p.ej. `const LinkedList = require('../linked-list');`
    - El nombre de la función del challenge depende de ti, pero se recomienda que utilices camel case
      - p.ej. `function findMaximumValue(list) { ... }`
    - Asegúrate de exportar tu función para que puedas escribir los tests
  - Tests
    - Crea una carpeta llamada `__tests__` y dentro de ella crea un archivo de test llamado `[challenge].test.js`
      - p.ej., `__tests__/find-maximum-value.test.js`
      - Tu archivo de test necesitará el archivo de challenge que se encuentra en el directorio anterior, el cual tiene tu función exportada
        - p.ej. `const reverse = require('../find-maximum-value.js');`

## Ejecutando los Tests

Si configuras las carpetas de acuerdo con las instrucciones anteriores, la ejecución de los tests se convierte en una cuestión de decidir qué tests quieres ejecutar.  Jest hace un buen trabajo al encontrar los archivos de test que coinciden con lo que especificaste en el comando test

Desde la carpeta `data-structures-and-algorithms/javascript`, ejecuta los siguientes comandos:

- **Ejecuta todos los tests posibles** - `npm test`
- **Ejecuta un test para una estructura de datos** - `npm test linked-list`
- **Ejecuta un test para un challenge en específico** - `npm test reverse-ll`

#### Tests en Tiempo Real

Ten en cuenta que cuando envíes tu código a GitHub, todos tus tests se ejecutarán automáticamente. Estos resultados deben coincidir con los tuyos y se encontrarán en la pestaña **Actions**
