# Calculadora de composición corporal — Fitdays + perímetros (v6)

Aplicación de una sola página (`index.html`, sin backend) para llevar el seguimiento de tus mediciones de la báscula **Fitdays** (8 electrodos, bioimpedancia de 20 y 100 kHz) junto con tus **perímetros corporales** (cintura, cadera, cuello, brazo, muslo) tomados con cinta métrica.

Abre `index.html` en Chrome, Edge, Firefox o Samsung Internet. No necesita instalación ni servidor.

## Qué hace

1. **Importa el informe Fitdays** (PDF o PNG): extrae texto directamente del PDF o aplica OCR (PDF escaneado / PNG), y valida los datos cruzando kg ↔ % ↔ peso para detectar errores típicos de OCR.
2. **Perímetros corporales**: en la pestaña "Circunferencias" añades a mano cintura, cadera, cuello, brazo y muslo (no vienen en el informe Fitdays).
3. **Tres estimaciones de grasa corporal, combinadas**:
   - **Fitdays (BIA)**: el % de grasa que reporta la báscula.
   - **RFM**: a partir de cintura y altura.
   - **Perímetros (método Navy)**: a partir de cuello, cintura y altura (y cadera en mujeres) — independiente de la bioimpedancia.
   - La **estimación combinada** mezcla las tres (50/25/25%, repartiendo el peso si falta algún dato). Si cargas un resultado de DXA, la app calibra el sesgo individual de cada método frente a tu DXA.
4. **Seguimiento**: gráficas de composición corporal, impedancia de extremidades y perímetros corporales, más una tabla de historial editable.
5. **Respaldo**: guarda todo el historial y la configuración en un `.json` para restaurarlo en otro teléfono o navegador. También admite exportar/importar en `.csv`.

Los datos se guardan en `localStorage` del navegador — por eso el respaldo en `.json` es la forma segura de no perder el historial al cambiar de dispositivo o borrar datos del navegador.

## Aviso

Seguimiento personal; no sustituye una DXA, antropometría ISAK ni evaluación clínica.
