# Guía de usuario para principiantes — Tarea Semana 2

Bienvenido
---------
Esta guía breve está pensada para personas que exploran el proyecto por primera vez. Explica qué hace la aplicación, cómo navegarla y cómo probar la aplicación paso a paso.

Qué es esta aplicación
----------------------
El programa consiste en una colección de vistas Razor (ejercicios) construida sobre .NET 10. Cada "Ejercicio" es una página demostrativa que ilustra un comportamiento o componente web sencillo (formularios, scripts, estilos, etc.). El Ejercicio 13 es una pequeña herramienta de consulta de estado de envíos (simulada).

Requisitos mínimos
------------------
- .NET SDK 10 instalado.
- Navegador moderno (Chrome, Edge, Firefox).
- (Opcional) Visual Studio 2026 para editar y depurar.

Arrancar la aplicación
----------------------
1. Abrir terminal en la carpeta raíz del proyecto (donde está `WebSystemExample.csproj`).
2. Ejecutar:
   - `dotnet restore`
   - `dotnet run`
3. Abrir el navegador en la URL que muestre la consola (p. ej. `https://localhost:5001`).

Si usas Visual Studio 2026:
- Abrir la solución y ejecutar con __F5__ o desde el menú __Debug > Start Debugging__.

Navegación básica
-----------------
- Página principal: `/` o `/Home/Index`
- Privacidad: `/Home/Privacy`
- Lista de ejercicios: `/Home/Ejercicio1` … `/Home/Ejercicio19`
- Ejercicio 13 (ejemplo): `/Home/Ejercicio13`

Tour práctico — Ejercicio 13
----------------------------
Propósito: consultar el "estado" de un envío mediante un código (simulado, en memoria).

<img width="1892" height="894" alt="image" src="https://github.com/user-attachments/assets/ff4e31dd-f923-410f-9cc1-85d174cb484e" />

Archivos clave:
- Vista: `Views/Home/Ejercicio13.cshtml`
- Script: `wwwroot/js/ejercicio13.js`

Cómo usarlo:
1. Abrir `/Home/Ejercicio13`.
2. Introducir un código de seguimiento en el campo (por ejemplo `ENV001`, `ENV002`, `ENV003`, `ABC123`, `XYZ999`).
3. Pulsar el botón “Buscar”.
4. Verás un mensaje:
   - Advertencia si el campo está vacío.
   - Éxito si el código existe (muestra el estado).
   - Error si no se encuentra el código.

Probar rápidamente (valores de ejemplo)
- `ENV001` → "En tránsito"
- `ENV002` → "En reparto"
- `ENV003` → "Entregado"
- `ABC123` → "En tránsito"
- `XYZ999` → "Entregado"
