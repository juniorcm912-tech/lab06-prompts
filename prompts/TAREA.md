# Tarea: Mi prompt profesional

## Funcionalidad elegida

Registro de estudiantes y cálculo de promedio de notas con validación en Java Swing.

## Version 1: prompt basico

````text
Hazme un programa para calcular notas de alumnos en Java.

## Version 2:
Actúa como desarrollador Java. Crea un programa en Java Swing que permita ingresar el nombre de un estudiante y 3 notas, calcule el promedio y determine si está aprobado o desaprobado. Presenta el código organizado en clases.

## Version 3: prompt final
```text
Actúa como desarrollador Java sénior. Crea un programa de escritorio usando Java Swing para un sistema de gestión escolar que registre el nombre del estudiante y 3 notas (en escala de 0 a 20). Debe calcular el promedio y mostrar un mensaje mediante JOptionPane indicando si aprobó (nota >= 13) o desaprobó.

Restricciones:
- No uses librerías externas.
- Valida que las notas estén strictly en el rango de 0 a 20.
- Captura la excepción NumberFormatException si se ingresa texto en lugar de números y muestra una alerta con JOptionPane.
- Presenta primero una breve explicación de la arquitectura y luego el código fuente organizado en bloques limpios.

```
* **Qué cambié:** Agregué restricciones explícitas (sin librerías externas), manejo de excepciones ante texto, rango de notas (0 a 20) y un ejemplo del mensaje de error.
* **Por qué:** Para evitar que el programa colapse ante entradas inválidas del usuario.
* **Qué mejoró:** La IA generó un código robusto que no falla ante datos vacíos o letras y muestra cuadros de diálogo interactivos[cite: 1].

## Componentes del prompt final

| Componente | Texto de mi prompt |
|---|---|
| **Rol** | Actúa como desarrollador Java sénior. |
| **Instrucción** | Crea un programa de escritorio usando Java Swing para registrar 3 notas, calcular el promedio y determinar el estado del alumno. |
| **Contexto** | Sistema de gestión escolar con escala de notas de 0 a 20 y nota mínima de aprobación de 13. |
| **Ejemplo** | "Error: La nota ingresada debe ser un valor numérico entre 0 y 20." |
| **Formato** | Breve explicación de la arquitectura seguida de los bloques de código limpio en Java. |

## Evaluacion del resultado

| Criterio | Cumple (Sí / No) |
|---|---|
| ¿Utiliza Java Swing sin librerías externas? | Sí |
| ¿Valida que las notas estén estrictamente entre 0 y 20? | Sí |
| ¿Muestra avisos con JOptionPane ante datos inválidos o texto? | Sí |
| ¿Incluye la explicación de la arquitectura antes del código? | Sí |

## Errores que evite

1. **Ser demasiado general:** En la versión 1 no especifiqué el tipo de aplicación ni las tecnologías[cite: 1]. Lo evité definiendo claramente `Java Swing`, la escala de notas (0 a 20) y la nota mínima aprobatoria (13)[cite: 1].
2. **No definir manejo de excepciones / errores:** En las primeras iteraciones la IA no capturaba errores de tipeo[cite: 1]. Lo evité indicando explícitamente en las restricciones que debía capturar `NumberFormatException` y mostrar alertas con `JOptionPane`[cite: 1].
````
