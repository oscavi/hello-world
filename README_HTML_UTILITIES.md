# README – Utilidades HTML/JavaScript

Esta guía reúne las utilidades HTML+JavaScript del repo público y propone un flujo de trabajo centrado en navegador.

## URLs de las utilidades

### Guías
- Guía principal: https://oscavi.github.io/hello-world/guide.html
- Guía completa: https://oscavi.github.io/hello-world/guide-complete.html

### Dataset / entrenamiento en navegador
- ZIP Dataset Trainer: https://oscavi.github.io/hello-world/zip-dataset-trainer.html
- ZIP Dataset Trainer Pro: https://oscavi.github.io/hello-world/zip-dataset-trainer-pro.html
- ZIP Dataset Trainer Ultra: https://oscavi.github.io/hello-world/zip-dataset-trainer-ultra.html
- YOLO Builder Mobile: https://oscavi.github.io/hello-world/yolo-builder-mobile.html
- YOLO Builder Mobile Unique: https://oscavi.github.io/hello-world/yolo-builder-mobile-unique.html
- YOLO Workbench PC: https://oscavi.github.io/hello-world/yolo-workbench-pc.html
- YOLO Converter Workbench: https://oscavi.github.io/hello-world/yolo-converter-workbench.html

### Inferencia / detección
- Vision Detect Ultra: https://oscavi.github.io/hello-world/vision-detect-ultra.html
- Vision YOLO Adaptive: https://oscavi.github.io/hello-world/vision-yolo-adaptive.html
- Vision YOLO Adaptive + ORT: https://oscavi.github.io/hello-world/vision-yolo-adaptive-ort.html
- Vision YOLO Edge Auto: https://oscavi.github.io/hello-world/vision-yolo-adaptive-auto.html

### Gestión
- Dashboard de modelos: https://oscavi.github.io/hello-world/model-dashboard.html
- SaaS Panel: https://oscavi.github.io/hello-world/saas-panel.html

## Proceso recomendado usando las utilidades HTML

## Opción A. Clasificación de imágenes solo con navegador

Esta opción sí puede hacerse prácticamente entera en HTML+JavaScript.

1. Prepara tus categorías con ZIPs separados.
2. Abre uno de estos trainers:
   - `zip-dataset-trainer.html`
   - `zip-dataset-trainer-pro.html`
   - `zip-dataset-trainer-ultra.html`
3. Carga las categorías y ZIPs.
4. Escanea el dataset.
5. Entrena en el navegador.
6. Descarga:
   - `model.json`
   - `weights.bin`
   - `labels.json`
7. Integra ese modelo en una app web compatible de clasificación.

### Cuándo usar cada trainer
- `zip-dataset-trainer.html` → versión simple
- `zip-dataset-trainer-pro.html` → versión recomendada
- `zip-dataset-trainer-ultra.html` → versión más completa con métricas, auto-split y gráficas

## Opción B. Detección tipo YOLO con ayuda de utilidades HTML

Aquí las utilidades HTML cubren dataset, validación, revisión y despliegue visual, pero el entrenamiento YOLO real sigue siendo más adecuado fuera del navegador.

### Paso 1. Crear dataset desde móvil
Usa:
- `yolo-builder-mobile-unique.html`

Motivo:
- evita nombres repetidos al capturar con iPhone
- genera un dataset mucho más fiable que la versión original

Proceso:
1. Crea las clases.
2. Haz fotos o selecciona imágenes.
3. Dibuja cajas.
4. Guarda anotaciones.
5. Exporta `train.zip` y `test.zip`.

### Paso 2. Validar y preparar desde PC
Usa:
- `yolo-workbench-pc.html`

Proceso:
1. Sube `train.zip`, `test.zip` y `classes.txt`.
2. Revisa validación del dataset.
3. Obtén la recomendación de modelo.
4. Genera configuración de entrenamiento.

### Paso 3. Preparar conversión/despliegue
Usa:
- `yolo-converter-workbench.html`

Proceso:
1. Indica el peso entrenado y el perfil objetivo.
2. Genera comandos orientativos de exportación.
3. Descarga la guía de conversión.

### Paso 4. Probar inferencia web
Usa una de estas:
- `vision-yolo-adaptive-ort.html`
- `vision-yolo-adaptive-auto.html`

Recomendación:
- usa `vision-yolo-adaptive-auto.html` como app principal
- si publicas dos modelos (`model.onnx` y `model.int8.onnx`), elegirá el adecuado según dispositivo

### Paso 5. Gestionar modelos publicados
Usa:
- `model-dashboard.html`

Proceso:
1. Introduce la raíz de modelos, por ejemplo:
   - `https://oscavi.github.io/hello-world/modelos/vespas/`
2. Revisa versión activa.
3. Lanza la inferencia desde el propio dashboard.

### Paso 6. Gestionar el backend SaaS
Usa:
- `saas-panel.html`

Proceso:
1. Configura la URL del backend.
2. Crea organización.
3. Genera API key.
4. Crea proyecto.
5. Registra modelo.
6. Activa deployment.
7. Lee `runtime/config/{slug}`.

## Flujo mínimo recomendado para detección

Si quieres ir al grano y usar solo la parte visual/navegador para operar:

1. Dataset:
   - `yolo-builder-mobile-unique.html`
2. Validación:
   - `yolo-workbench-pc.html`
3. Conversión/guía:
   - `yolo-converter-workbench.html`
4. Producción:
   - `vision-yolo-adaptive-auto.html`
5. Gestión:
   - `model-dashboard.html`
6. SaaS:
   - `saas-panel.html`

## Qué utilidades usar ahora mismo

Si ya tienes `train` y `test` hechos:

1. Revisa dataset en `yolo-workbench-pc.html`
2. Usa `yolo-converter-workbench.html` para preparar el despliegue
3. Publica el modelo en la carpeta de modelos del repo público
4. Prueba con `vision-yolo-adaptive-auto.html`
5. Supervisa con `model-dashboard.html`

## Recomendación final

### Para clasificación pura
- `zip-dataset-trainer-ultra.html`

### Para detección YOLO
- `yolo-builder-mobile-unique.html`
- `yolo-workbench-pc.html`
- `vision-yolo-adaptive-auto.html`
- `model-dashboard.html`

## Nota importante

Las utilidades HTML cubren muy bien:
- creación de dataset
- revisión
- preparación
- inferencia
- gestión

Pero el entrenamiento YOLO pesado sigue estando pensado para la parte técnica del entorno privado. Las utilidades HTML te permiten operar y preparar el flujo visual de principio a fin, y son la mejor interfaz de trabajo del sistema.
