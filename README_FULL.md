# 📘 Vision AI Edge Platform – Documentación Completa

## 🧠 Descripción

Plataforma completa de visión artificial que cubre todo el ciclo:

- Dataset (móvil)
- Entrenamiento (PC/GPU)
- Exportación
- Optimización
- Deploy automático
- Inferencia en navegador
- Gestión con dashboard

---

# 🚀 1. Arquitectura

## 🔒 Repo privado
- Entrenamiento YOLO
- Scripts pipeline
- Exportación ONNX
- Quantization
- CI/CD

## 🌐 Repo público
- Apps web
- Dashboard
- Modelos desplegados

---

# 📱 2. Crear dataset

Abrir:

👉 yolo-builder-mobile.html

Genera:
- train.zip
- test.zip
- classes.txt

---

# 💻 3. Entrenamiento

```bash
python scripts/pipeline.py
```

---

# 🔄 4. Optimización

```bash
python scripts/quantize_onnx.py --input exports/web/model.onnx
```

---

# 🚀 5. Deploy automático

```bash
python scripts/deploy_versioned_and_push.py --public-repo /ruta/repo
```

---

# 🌐 6. Uso en web

Abrir:

- vision-yolo-adaptive-auto.html

Usar:

/modelos/vespas/latest/

---

# 📊 7. Dashboard

Abrir:

- model-dashboard.html

Funciones:
- ver versiones
- lanzar modelo
- copiar URLs

---

# 🧠 Buenas prácticas

- usar INT8 en móvil
- usar latest para producción
- versionar siempre

---

# 🔥 Pipeline completo

```bash
pipeline → quantize → deploy → listo
```

---

# 🚀 Estado

✔️ Sistema completo funcional
✔️ CI/CD activo
✔️ Edge AI optimizado

---

# 🔮 Futuro

- SaaS
- multiusuario
- métricas
