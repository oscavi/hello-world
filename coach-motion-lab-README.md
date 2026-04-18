# Coach Motion Lab

Prueba de concepto en un solo archivo `coach-motion-lab.html` para:

- grabar al entrenador haciendo un ejercicio;
- extraer landmarks corporales con un stickman;
- comparar después al alumno frente al patrón grabado;
- mostrar una puntuación aproximada de corrección en tiempo real.

## Cómo usarlo

1. Abre `coach-motion-lab.html` desde un servidor local o una publicación web con HTTPS.
2. Permite el acceso a cámara.
3. Graba la referencia del entrenador.
4. Inicia la evaluación del alumno.

## Limitaciones

- Es una POC, no una métrica clínica.
- Funciona mejor con una sola persona visible y cuerpo entero en cámara.
- La comparación usa remuestreo temporal sencillo, no DTW ni modelos avanzados.
- No guarda vídeos; solo conserva la secuencia de características en memoria.
