# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Tokens y ventana de contexto

### 1. Conteo de tokens

| Texto                              | Caracteres | Tokens |
| ---------------------------------- | ---------- | ------ |
| Los estudiantes programan en Java. | 35         | 7      |
| The students program in Java.      | 29         | 6      |
| desafortunadamente                 | 18         | 4      |

## Ejercicio 3: Temperatura

### Tabla de resultados del simulador

| Temperatura | % de BiblioTec | Nombres en los 5 intentos                             |
| ----------- | -------------- | ----------------------------------------------------- |
| 0           | 100.0%         | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5         | 62.4%          | BiblioTec, LibroYa, BiblioTec, PrestaLibro, BiblioTec |
| 1           | 42.1%          | BiblioTec, LectoGo, LibroYa, PrestaLibro, NubeDeTinta |
| 1.8         | 31.8%          | LectoGo, PaginaLibre, BiblioTec, NubeDeTinta, LibroYa |

**Explicacion:**
Al subir la temperatura, los porcentajes de probabilidad se reparten entre mas opciones, haciendo que salgan nombres mas variados y raros en cada intento. El simulador nunca inventa un nombre nuevo porque la temperatura solo altera el nivel de riesgo/variabilidad al elegir entre las opciones que ya conoce, no le agrega nuevo conocimiento al modelo.

## Ejercicio 4: Prompt vago vs estructurado

## Ejercicio 5: Anatomia de un prompt

## Ejercicio 6: Del prompt basico al profesional
