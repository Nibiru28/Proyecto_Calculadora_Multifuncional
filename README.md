# Proyecto_Calculadora_Multifuncional
Calculadora con múltiples funciones, validaciones //   estrictas y manejo de errores para evitar bloqueos y entradas //   inválidas del usuario.

# 🧮 Calculadora Multifuncional Protegida

## 📖 Descripción del proyecto
Este proyecto implementa una **calculadora multifuncional en PSeInt** que incluye cuatro módulos principales:
1. Operaciones básicas (suma, resta, multiplicación y división)
2. Cálculo de áreas geométricas
3. Estadística básica (media, mediana y moda)
4. Generación de sucesión de Fibonacci

El programa está diseñado con **protecciones avanzadas** para evitar errores de ejecución y asegurar una experiencia segura para el usuario.

---

## ⚙️ Cómo se hizo (arquitectura y lógica)
- El programa principal controla el menú principal y las opciones del usuario.
- Se utiliza una **función genérica `LeerNumero()`** que valida entradas numéricas, rangos y número máximo de intentos.
- Cada módulo está implementado como **SubProceso independiente**, facilitando la lectura, depuración y mantenimiento.
- Se agregaron **verificaciones de errores** como:
  - División entre cero.
  - Rangos fuera de límites.
  - Evitar bucles infinitos en Fibonacci.
  - Evitar bases inválidas en trapecio.
  - Control de intentos y límites de datos en estadística.

---

## 🎯 Propósito de cada módulo
| Módulo | Propósito |
|--------|------------|
| `OperacionesBasicas` | Realizar operaciones aritméticas seguras con validación de errores. |
| `AreasGeometricas` | Calcular áreas de figuras geométricas con restricciones de entrada. |
| `EstadisticaBasica` | Analizar un conjunto de datos: media, mediana y moda. |
| `Fibonacci` | Generar una secuencia numérica limitada y controlada. |
| `LeerNumero` | Centraliza las validaciones de rango y errores en todas las entradas. |

---

## 🧩 Dificultades encontradas y soluciones
| Dificultad | Solución aplicada |
|-------------|------------------|
| Manejo de valores fuera de rango | Se implementó la función `LeerNumero()` con límites mínimos y máximos. |
| Riesgo de división entre cero | Se agregó una condición especial que cancela la operación si `b = 0`. |
| Entrada repetida de datos erróneos | Límite de 3 intentos antes de regresar al menú principal. |
| Modas repetidas en estadística | Se añadió control con variable `mostrado` para evitar duplicados. |
| Bucle infinito en Fibonacci | Se incluyó variable `continuar` y tope máximo de `1,000,000`. |

---

## 🕒 Control de versiones
Ejemplo de historial sugerido de commits:

Control de versiones claro:

     - Commits descriptivos y organizados:
     
 ✳️ Commit: “Creación del menú principal y estructura base del programa.”

Se estableció el flujo inicial del proceso principal.

➕ Commit: “Implementación de módulo de operaciones básicas con validaciones.”

Se añadieron las operaciones aritméticas y control de división entre cero.

⚙️ Commit: “Función LeerNumero() creada para validar entradas de usuario.”

Se centralizó la lectura y se limitaron los intentos incorrectos.

🧮 Commit: “Agregado módulo de cálculo de áreas geométricas.”

Se incorporaron figuras y validaciones de rangos y coherencia lógica.

📊 Commit: “Módulo de estadística básica con media, mediana y moda.”

Se implementaron cálculos, ordenamiento y detección de modas múltiples.

🔢 Commit: “Añadida sucesión de Fibonacci con límites de tamaño y valor.”

Se previnieron errores por crecimiento excesivo o valores fuera de rango.

🛡️ Commit: “Integración completa y protecciones globales implementadas.”

Se añadieron validaciones y límites en todos los subprocesos.

🧾 Commit: “Documentación interna agregada con comentarios en todo el código.”

Se mejoró la legibilidad y claridad del flujo lógico.

🚀 Commit: “Versión final optimizada y lista para GitHub.”

Se verificó el correcto funcionamiento y se preparó la documentación completa.

     - Historial que muestre la evolución del proyecto:

🟩 Versión 1.0 — Creación del Proyecto

Estructura base del menú y flujo principal.

🟨 Versión 1.1 — Operaciones Básicas

Implementación de suma, resta, multiplicación y división con validación de errores.

🟦 Versión 1.2 — Lectura Validada

Función LeerNumero() para control de entradas seguras.

🟩 Versión 1.3 — Áreas Geométricas

Cálculo de áreas de figuras planas con validaciones y constante π.

🟨 Versión 1.4 — Estadística Básica

Cálculo de media, mediana y moda con ordenamiento de datos.

🟦 Versión 1.5 — Sucesión de Fibonacci

Generación controlada de la secuencia con límites numéricos.

🟩 Versión 2.0 — Integración y Protecciones

Consolidación total de funciones y 10 protecciones clave implementadas.

🟨 Versión 2.1 — Optimización y Comentarios

Código reorganizado y comentado para mayor legibilidad.
     
     - Uso adecuado de branches si aplica:
     
main
Rama principal del proyecto. Contiene la versión estable y completamente funcional del código final, junto con la documentación lista para entrega.

dev
Rama de desarrollo donde se integraron y probaron nuevas funciones antes de ser fusionadas en main.

feature/operaciones-basicas
Rama dedicada a la implementación y prueba del módulo de operaciones aritméticas.

feature/areas-geometricas
Utilizada para el desarrollo del subproceso de cálculo de áreas y validaciones de entrada.

feature/estadistica
Creada para la programación del módulo de media, mediana y moda, así como su ordenamiento interno.

feature/fibonacci
Rama específica para la sucesión de Fibonacci, incluyendo límites de crecimiento y validaciones.

feature/validaciones
Enfocada en integrar las 10 protecciones globales, control de errores y límites numéricos.
