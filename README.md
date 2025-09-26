# 🦾 Proyecto: Model Fitness Gym – Análisis de Pérdida de Clientes

Análisis predictivo y segmentación de clientes para una cadena de gimnasios, con el objetivo de anticipar el abandono (churn) y diseñar estrategias de retención basadas en datos.

---

## 🏢 Contexto Empresarial

Model Fitness es una cadena de gimnasios enfocada en innovación y experiencia del cliente. Uno de sus principales desafíos es la pérdida silenciosa de usuarios: clientes que dejan de asistir sin cancelar formalmente su membresía.  
Este proyecto busca detectar patrones de abandono, predecir el churn y segmentar perfiles para diseñar estrategias de retención personalizadas.

---

## 🎯 Objetivos del proyecto

- Predecir la probabilidad de abandono de clientes usando datos históricos.  
- Identificar variables clave que influyen en el churn.  
- Segmentar perfiles mediante clustering para diseñar acciones específicas.  
- Generar recomendaciones estratégicas basadas en evidencia analítica.

---

## 📂 Estructura del repositorio

```
├── gym_churn_us.csv         # Dataset ficticio con perfiles y comportamiento de clientes
├── ModelFitness_Churn.ipynb # Notebook con análisis, modelado y segmentación
├── images                   # Visualizaciones de analisis
├── .gitignore               # Exclusión de archivos temporales y entornos locales
└── README.md                # Documentación del proyecto
```

---

## 🧠 Descripción del dataset

El archivo `gym_churn_us.csv` contiene 4000 registros y 14 columnas, todas numéricas.  
Incluye variables demográficas, comportamiento de uso, tipo de contrato y cancelación (`churn`).  
No hay valores nulos, y los nombres de columnas fueron estandarizados para facilitar el procesamiento.

---

## 📊 Exploración inicial

- El 27% de los clientes han cancelado su membresía.  
- La mayoría vive cerca del gimnasio (85%) y dejó su número de teléfono (90%).  
- Edad promedio: 29 años.  
- Contratos cortos predominan (mediana de 1 mes).  
- Gasto adicional muy disperso, con outliers por encima de 500.  
- Frecuencia promedio de visitas semanales: ~1.8

---

## 🧪 Modelado predictivo

Se entrenaron dos modelos:  
- **Regresión Logística** (con escalado y pipeline)  
- **Random Forest** (sin escalado)

Ambos fueron evaluados con exactitud, precisión y recall.  
La Regresión Logística mostró mejor desempeño y mayor interpretabilidad, por lo que fue seleccionada como modelo final.

---

## 🔍 Segmentación de clientes

Se aplicaron dos técnicas:

1. **Clustering jerárquico** para diagnóstico exploratorio  
2. **KMeans** para segmentación final (`n_clusters=5`)

Se identificaron cinco perfiles distintos con patrones de comportamiento y riesgo de cancelación diferenciados.

---

## 📈 Perfiles estratégicos detectados

- **Cluster 0 – Usuarios en riesgo**  
  Baja frecuencia, poca antigüedad, alta cancelación.

- **Cluster 1 – Clientes estables**  
  Alta frecuencia, antigüedad elevada, baja cancelación.

- **Cluster 2 – Contratos largos, bajo churn**  
  Periodos extensos, alta retención.

- **Cluster 3 – Promocionales activos**  
  Uso intensivo de promociones, cancelación intermedia.

- **Cluster 4 – Jóvenes indecisos**  
  Frecuencia baja, cancelación alta.

---

## 📌 Recomendaciones estratégicas

- Activar clientes en riesgo con retos, clases gratuitas y beneficios por permanencia.  
- Recompensar la lealtad con programas de fidelización y referidos.  
- Potenciar promociones grupales para consolidar hábitos.  
- Personalizar la comunicación según perfil usando automatización de marketing.

---

## 🛠️ Tecnologías utilizadas

- Python 3  
- Jupyter Notebook  
- Pandas / NumPy / Scikit-learn  
- Matplotlib / Seaborn  
- Técnicas: Regresión Logística, Random Forest, Clustering jerárquico, KMeans

---

## ⚙️ Requisitos

1. Tener instalado Python 3.9+  
2. Instalar librerías necesarias:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

3. Abrir el notebook en Jupyter:

   ```bash
   jupyter notebook ModelFitness_Churn.ipynb
   ```

---

> Los datos utilizados son ficticios y se incluyen en el repositorio para fines educativos.
