# Proyecto: Sistema Proyecto — LPR 2026

**Escuela de Educación Secundaria Técnica N° 1 - Vicente López**  
**Curso:** 5° Año 3° División — Especialidad Informática / Programación  
**Materia:** Laboratorio de Programación (LPR)  
**Profesor:** Prof. York Mansilla Muñoz  
**Estudiante:** Alexander Luca Veit

## 📌 Descripción de la Actividad

Esta actividad corresponde a la configuración inicial del Entorno de Desarrollo Integrado (IDE) y la primera compilación nativa en C++. Los estudiantes configuran su espacio de trabajo en Visual Studio Code, estructuran el repositorio profesionalmente con control de versiones en Git, y compilan su primer binario de consola utilizando el compilador GCC/G++ en Windows 10/11.

Además, el proyecto aborda el **modelado de datos con `struct` y punteros** (Actividad 5: Modelado de datos con Structs y Punteros), aplicando pasaje por dirección para cargar y mostrar información desde la memoria Stack.

## 🗂 Estructura del Repositorio

```text
sistemaproyecto/
├── src/                # Código fuente y binario compilado
│   ├── main.cpp        # Código fuente en C++ (structs + punteros)
│   └── main.exe        # Ejecutable generado
├── capturas/           # Capturas de pantalla del proceso
│   └── ejecucion_struct.png
├── docs/               # Documentación
│   ├── InformeEEST1_LPR2026_ACT05_G03_v1.0.0.pdf
│   └── manuales/
│       ├── manual_programador_v1.0.0.pdf
│       └── manual_programador_v1.0.0.md
├── .gitignore
├── LICENSE             # Licencia MIT
└── README.md
```

## 💻 Implementación

El programa se encuentra en `src/main.cpp`:

- **Estructura de datos:** Se define `EntidadProyecto` con `id`, `nombre[50]` y `metrica` (float), pensada como modelo base para un Proyecto Integrador Anual.
- **Paso por dirección:** Se declara `void cargarDatos(EntidadProyecto* ptr);` y se invoca con `cargarDatos(&miEntidad);` para modificar directamente la estructura en memoria.
- **Acceso con operador flecha:** Dentro de `cargarDatos()` se accede a los miembros con `ptr->id`, `ptr->nombre` y `ptr->metrica`.
- **Ingreso de datos:** Se utiliza `cin >>` para enteros/float, `cin.ignore()` para limpiar el buffer y `cin.getline()` para leer cadenas con espacios.
- **Visualización:** Muestra los datos cargados y la dirección hexadecimal de la estructura en RAM.

## 🛠️ Requisitos e Instalación

Para compilar y ejecutar este proyecto en Windows 10/11:

- **Visual Studio Code:** Con las extensiones oficiales C/C++ (Microsoft) y C/C++ Extension Pack.
- **Compilador MinGW (GCC/G++):** Configurado correctamente en las variables de entorno (`PATH` del sistema).
- **Git for Windows:** Para la gestión del repositorio y sincronización con GitHub.

## ▶️ Comandos para compilar y ejecutar (PowerShell - VS Code)

Asegurate de abrir la terminal integrada de VS Code (`Ctrl + Ñ`) y estar parado en la raíz de la carpeta `sistemaproyecto`.

### Verificar el compilador

```bash
g++ --version
```

### Compilar el código fuente modular

```bash
g++ ./src/main.cpp -o ./src/sistema.exe
```

### Ejecutar la aplicación

```bash
./src/sistema.exe
```

## 🧪 Evidencias

El repositorio incluye capturas del proceso en la carpeta `capturas/`:

- `ejecucion_struct.png` - Ejecución del programa mostrando el ingreso y visualización de datos con structs y punteros

## 📚 Documentación

- **Informe:** `docs/InformeEEST1_LPR2026_ACT05_G03_v1.0.0.pdf`
- **Manuales:** `docs/manuales/manual_programador_v1.0.0.pdf` y `docs/manuales/manual_programador_v1.0.0.md`

## 👤 Autor

- **Alexander Luca Veit** — Programador / Estudiante  
  GitHub: [Xen-alt10](https://github.com/Xen-alt10)  
  Repositorio: [sistemaproyecto](https://github.com/Xen-alt10/sistemaproyecto)

## 📄 Licencia

Este proyecto está bajo licencia [MIT](LICENSE). Copyright (c) 2026 Xen-alt10.
