# Vision AI Platform (YOLO Web)

Sistema completo de visión artificial desde dataset hasta detección en tiempo real.

## 🔥 Componentes

### 📱 Mobile
- yolo-builder-mobile.html → crear dataset YOLO

### 💻 PC
- yolo-workbench-pc.html → validar dataset + generar entrenamiento
- yolo-converter-workbench.html → convertir modelo a web

### 🌐 Web
- vision-yolo-adaptive.html → detección en tiempo real adaptativa

---

## 🚀 Flujo completo

1. Crear dataset (móvil)
2. Validar dataset (PC)
3. Entrenar modelo (YOLO)
4. Convertir modelo
5. Detectar en web

---

## ⚙️ Entrenamiento

```bash
pip install ultralytics
yolo detect train data=data.yaml model=yolov8n.pt epochs=80
```

---

## 🔄 Conversión

```bash
yolo export model=best.pt format=onnx
```

---

## 🌐 Uso final

Cargar en:

- vision-yolo-adaptive.html

---

## 🧠 Adaptación automática

- móvil → modelo ligero
- PC → modelo potente

---

## 📦 Resultado

- detección en tiempo real
- sistema escalable
- compatible móvil + PC

---

## 🚀 Futuro

- optimización WebGPU
- quantization
- modelos personalizados
