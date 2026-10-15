# Manual del Programador - Actividad 5 (SISTEMAPROYECTO)

## ¿Qué es una Estructura (struct) y cómo se usa la Flecha (->)?

### 1. ¿Qué es la estructura EntidadProyecto?
Una **"estructura"** (`struct`) es como armar una **"ficha de datos"** personalizada. Nos sirve para agrupar información de distinto tipo sobre una misma cosa en un solo lugar.

En nuestro código, la ficha **"EntidadProyecto"** guarda 3 datos juntos:
- **"id"** (`int`): Un número entero para identificar la ficha (por ejemplo: "101").
- **"nombre"** (`char[50]`): Un texto de hasta 50 letras para ponerle un nombre o descripción (por ejemplo: "Sensor Taller").
- **"metrica"** (`float`): Un número con coma decimal para guardar un valor de medición (por ejemplo: "24.5").

### 2. Modificar datos con Punteros y la Flecha (->)
Cuando le pasamos la ficha a la función **"cargarDatos()"**, no le enviamos una copia de toda la ficha porque eso ocuparía espacio de más en la memoria RAM. En su lugar, le enviamos la **dirección exacta** de memoria donde está guardada.

Como **"ptr"** guarda una dirección de memoria y no la ficha directamente, C++ no nos deja usar el punto normal. Por eso usamos el operador **"flecha"** (`->`):

**"Sintaxis:"** `ptr->metrica`

**"¿Qué significa en criollo?"** "Andá a la casilla de memoria guardada en **ptr** y escribí el dato directamente dentro de la ficha original".

### 3. ¿Por qué usamos `cin.ignore()`?
Después de leer el ID con `cin >> ptr->id`, queda un **"newline" invisible** (la tecla Enter) atrapado en el buffer de entrada. Si no lo sacamos, el siguiente `cin.getline()` lo lee como una línea vacía y el nombre sale en blanco.

`cin.ignore()` es como **"tirar a la basura"** ese Enter que quedó colgando antes de leer el nombre.




### 4. ¿Qué pasa en el `main`?
1. Se crea la ficha en el **stack** (memoria de corto plazo) con valores por defecto.
2. Se imprime el banner con el nombre del alumno.
3. Se llama a `cargarDatos(&miEntidad)` — el **`&`** le dice a la función "acá va la dirección donde está mi ficha".
4. Al volver, se imprimen todos los datos + la dirección RAM en hexadecimal.

### 5. La dirección en hexadecimal
Al final el programa muestra algo como `0x7ffd3a2b1c48`. Eso es la **dirección real en RAM** donde vive la struct. Cada vez que lo ejecutás va a ser **distinta** porque el sistema operativo usa ASLR (aleatorización de memoria) por seguridad.

---
