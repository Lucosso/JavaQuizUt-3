# JavaQuiz-UT3

Aplicación de consola en Java que consiste en un concurso de **seis preguntas** sobre conceptos básicos de Java, divididas en **dos rondas de tres preguntas**. Al terminar, el programa muestra el total de aciertos.

Proyecto realizado por parejas para la **Práctica Integradora UT3: Control de versiones con Git y trabajo colaborativo con GitHub**.


## Autores

| Integrante | Nombre | Usuario de GitHub | Aportación |
|------------|--------|-------------------|------------|
| A | Lucas Rodriguez | _@Lucosso_ | Estructura inicial, contador de aciertos y preguntas 1 a 3 (Ronda 1) |
| B | Alex tofan tofan | _@aaleextf_ | Preguntas 4 a 6 (Ronda 2), resultado final y documentación |

## Descripción

Al ejecutar el programa:

1. Se muestra el título del concurso y las instrucciones.
2. **Ronda 1** (preguntas 1 a 3) y **Ronda 2** (preguntas 4 a 6).
3. Cada pregunta muestra un enunciado y tres opciones (A, B y C). El usuario escribe una letra y el programa indica si la respuesta es **«¡Correcto!»** o **«Incorrecto»**.
4. Un único contador de aciertos, compartido por ambas rondas, aumenta solo con las respuestas correctas.
5. Al final se muestra el resultado, por ejemplo: `Respuestas correctas: 5 de 6`.

Las respuestas se aceptan en mayúsculas o minúsculas (se usa `equalsIgnoreCase`). Se asume que el usuario introduce siempre una letra válida, por lo que no se validan entradas incorrectas.

## Ejemplo de ejecución

```
========== JAVAQUIZ ==========
Concurso de preguntas sobre Java
Responde escribiendo A, B o C.

--- RONDA 1 ---
Pregunta 1. ¿Qué tipo de dato almacena números enteros?
A) double
B) int
C) String
Respuesta: B
¡Correcto!

[...]

--- RONDA 2 ---
Pregunta 4. ¿Cuál es el primer índice de un array en Java?
A) 1
B) -1
C) 0
Respuesta: A
Incorrecto.

[...]

========== RESULTADO ==========
Respuestas correctas: 5 de 6
Fin del concurso.
```

## Requisitos

- **JDK 17 o superior** (cualquier JDK reciente es válido).
- **Visual Studio Code** con el *Extension Pack for Java* (opcional, recomendado).
- **Git** para clonar el repositorio.

## Instrucciones de ejecución

### 1. Clonar el repositorio

```bash
git clone https://github.com/<usuario>/JavaQuiz-UT3.git
cd JavaQuiz-UT3
```

También se puede clonar desde VSCode: `Ctrl+Shift+P` → **Git: Clone**.

### 2. Ejecutar desde VSCode

1. Abrir la carpeta del proyecto en VSCode.
2. Abrir `JavaQuiz.java`.
3. Pulsar **Run** (▶) sobre el método `main`, o usar `F5`.
4. Responder en la terminal integrada escribiendo A, B o C y pulsando Enter.

### 3. Ejecutar desde la terminal

Si `JavaQuiz.java` está en la raíz del proyecto:

```bash
javac JavaQuiz.java
java JavaQuiz
```

Si está dentro de la carpeta `src`:

```bash
cd src
javac JavaQuiz.java
java JavaQuiz
```

> Los archivos `.class` generados al compilar **no se suben** al repositorio: están excluidos en el `.gitignore`.

## Estructura del proyecto

```
JavaQuiz-UT3/
├── src/
│   └── JavaQuiz.java    # Única clase, con todo el código en main
├── README.md
└── .gitignore
```

El código está organizado en `main` con zonas comentadas para facilitar el trabajo colaborativo sin conflictos:

- `INICIO / FIN RONDA 1 - INTEGRANTE A`
- `INICIO / FIN RONDA 2 - INTEGRANTE B`
- `RESULTADO FINAL - INTEGRANTE B`

## Flujo de trabajo con Git

- Rama única de trabajo: `main`, con turnos coordinados entre ambos integrantes.
- Antes de editar: `pull` para descargar los cambios del compañero.
- Cada integrante realiza commits propios con mensajes descriptivos y los publica con `push`.
- El historial de commits permite identificar la aportación de cada autor.

## Archivo .gitignore

Excluye archivos compilados, temporales, registros, salidas de Maven y configuración privada:

```
*.class
*.tmp
*.log
target/
.env
```

## Tecnologías

- Java (proyecto *No Build Tools*, sin Maven)
- `Scanner`, `String`, condicionales y estructuras de control
- Git y GitHub
- Visual Studio Code