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

### Comparación de resultados

| Criterio                            | Prompt vago | Prompt estructurado |
| ----------------------------------- | ----------- | ------------------- |
| Menciona el objetivo del sistema    | No          | Sí                  |
| Menciona a los usuarios principales | No          | Sí                  |
| Tiene exactamente 3 funcionalidades | No          | Sí                  |
| Está en 3 párrafos                  | No          | Sí                  |
| Lo usaría en un informe real        | No          | Sí                  |

**Observación:**
El prompt estructurado permite obtener un resultado preciso, organizado y listo para utilizar en un documento formal, mientras que el prompt vago genera una respuesta imprecisa y con una extensión impredecible.

## Ejercicio 5: Anatomia de un prompt

### Componentes del prompt final

| Componente      | Texto de mi prompt                                                             |
| --------------- | ------------------------------------------------------------------------------ |
| **Rol**         | Actua como desarrollador Java.                                                 |
| **Instruccion** | ...usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| **Contexto**    | ...para gestionar los productos de una tienda.                                 |
| **Ejemplo**     | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).       |
| **Formato**     | Explica primero la estructura de la clase y luego presenta el codigo Java.     |

### Evolución por niveles

- **Nivel 1:** La IA generó un script genérico ("Hola Mundo" o calculadora simple).
- **Nivel 2:** Adoptó el perfil técnico, estructurando el código con mejores prácticas de Java.
- **Nivel 3:** Centró la solución en la temática comercial de gestión de tienda.
- **Nivel 4:** Definió la entidad concreta Producto con los atributos específicos solicitados.
- **Nivel 5:** Separó la explicación teórica inicial del bloque final de código Java con la convención solicitada.v

## Ejercicio 6: Del prompt basico al profesional

### Evaluacion del prompt profesional

| Que revisar                                            | Cumple (Si / No) |
| ------------------------------------------------------ | ---------------- |
| ¿Esta escrito en Java y usa Swing?                     | Si               |
| ¿Pide correo y contraseña?                             | Si               |
| ¿Explica el funcionamiento antes o despues del codigo? | Si               |
| ¿El codigo esta organizado en clases?                  | Si               |
| ¿Valida los datos que ingresa el usuario?              | No               |

### Prompt final e iteracion guardada

```text
Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.

Mejora adicional (iteracion):
Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```
