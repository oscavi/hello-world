# Vision AI Edge – Frontend (Public)

Frontend y consumo de modelos para la plataforma de visión artificial.

## Entrada
- guide-complete.html
- model-dashboard.html
- saas-panel.html

## Rol
- Apps web
- Dashboard
- SaaS panel

## Decisiones
TF.js → YOLO → ONNX → ORT Web → INT8 → versionado → AUTO → Dashboard → SaaS

## Estructura modelos
/modelos/{proyecto}/latest/

## Regla
Privado=cerebro · Público=interfaz
