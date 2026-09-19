Desigualdad social en Bogotá: Gini, pobreza y localidades

Proyecto final de la materia DataXperience — análisis de ciencia de datos sobre la relación entre la desigualdad de ingresos (Coeficiente de Gini) y la pobreza monetaria en las 20 localidades de Bogotá.

Nombre: Johan David Pinto Martín Carrera: Ingeniería de Sistemas Docente: Camila Silva Gómez Materia: DataXperience Grupo: 1 · Ciclo: 3

Contexto

Bogotá es una ciudad con enormes contrastes territoriales: mientras algunas localidades tienen niveles de pobreza monetaria menores al 10%, otras superan el 55%. Este proyecto usa datos oficiales de la Secretaría Distrital de Salud (con base en la Encuesta Multipropósito DANE-SDP) para entender cómo se relacionan la desigualdad interna (Gini) y la pobreza por localidad, y para construir un modelo simple que prediga la pobreza extrema a partir de esas dos variables.

Pregunta principal (método C.L.A.R.A.)

¿Qué relación existe entre la desigualdad de ingresos (Coeficiente de Gini) y la incidencia de pobreza monetaria en las 20 localidades de Bogotá, y qué tan bien predice el Gini el nivel de pobreza extrema de una localidad?

Entregable

El análisis completo está en el notebook Proyecto_Final_DataXperience_Desigualdad_Bogota.ipynb, estructurado en tres etapas:

Etapa 1 — Selección, exploración y limpieza de datos
Carga del dataset oficial directamente desde Datos Abiertos Bogotá
Exploración inicial: tipos de variables, nulos, indicadores disponibles
Limpieza: filtrado de indicadores relevantes y transformación de formato largo a tabla analizable
Etapa 2 — Estadística descriptiva
Medidas de tendencia central (media, mediana, moda)
Medidas de dispersión (rango, varianza, desviación estándar)
Boxplots y detección de outliers (método IQR)
Etapa 3 — Visualización, modelo predictivo y storytelling
Gráfico de barras (pobreza monetaria por localidad), dispersión (Gini vs. pobreza) y serie histórica 2003-2021
Modelo de regresión lineal para predecir pobreza extrema (R² y MAE)
Storytelling con hallazgos y aplicación profesional
Dataset

Fuente: Secretaría Distrital de Salud de Bogotá — "Pobreza y desigualdad en Bogotá D.C", portal Datos Abiertos Bogotá, con datos provenientes de la Encuesta Multipropósito (DANE - SDP). Licencia Creative Commons Attribution 4.0.

Se incluye también desigualdad_pobreza_bogota_localidades.csv como respaldo local por si la descarga en línea no funciona al ejecutar el notebook.

Stack tecnológico
Python 3
pandas, numpy — manipulación de datos
matplotlib, seaborn — visualización
scikit-learn — modelo de regresión lineal
Cómo ejecutar
Abrir el notebook en Google Colab (subir el archivo o abrirlo directamente desde este repositorio).
Ejecutar todas las celdas en orden (Entorno de ejecución > Ejecutar todas).
Si la descarga desde la URL oficial falla por restricciones de red, cargar el CSV de respaldo incluido en el repositorio.
Estructura del repositorio
proyecto-dataxperience-bogota/
├── Proyecto_Final_DataXperience_Desigualdad_Bogota.ipynb   # Notebook principal (entregable)
├── desigualdad_pobreza_bogota_localidades.csv              # Dataset de respaldo
├── README.md
└── video/
    └── enlace_video.md                                     # Enlace al video de sustentación (2-5 min)
Hallazgos principales
La pobreza monetaria varía muchísimo entre localidades: 7.9% en Teusaquillo vs. 57.8% en Usme.
Santa Fe tiene el Gini más alto (0.65): conviven allí extremos de riqueza y pobreza dentro de la misma localidad.
Hallazgo clave: el Gini casi no se correlaciona con la pobreza monetaria (r ≈ -0.01) — ser internamente desigual no significa ser más pobre en promedio. Son fenómenos distintos.
La pobreza monetaria sí predice bien la pobreza extrema (r ≈ 0.89; modelo de regresión con R² ≈ 0.50).
A nivel ciudad, entre 2003 y 2017 el Gini bajó pero la pobreza monetaria subió, lo que amerita seguimiento.
Aplicación profesional

Este flujo (cargar → limpiar → explorar → visualizar → modelar) es el mismo que sustentaría un dashboard de política pública o un sistema de apoyo a la decisión para una Secretaría Distrital, útil para priorizar subsidios o monitorear el impacto de programas sociales por localidad.

Video de sustentación

📹 (https://youtu.be/X_fWBOpH1bg)

Referencias

Secretaría Distrital de Salud de Bogotá. (2026). Pobreza y desigualdad en Bogotá D.C [Conjunto de datos]. Datos Abiertos Bogotá. https://datosabiertos.bogota.gov.co/dataset/pobreza-y-desigualdad-en-bogota-d-c# proyecto-final-dataxperience-bta
