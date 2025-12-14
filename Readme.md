# TFM – Predicción de Clientes mediante Machine Learning

**Autor:** Leopoldo Ripoll Vitini  
**Trabajo Fin de Máster (TFM)**  
**Área:** Machine Learning / Data Science  

---

## Descripción general

Este repositorio contiene el desarrollo completo del **Trabajo Fin de Máster**, cuyo objetivo es la **construcción y evaluación de modelos de Machine Learning para la predicción de comportamiento de clientes**.

El proyecto está diseñado para ser **reproducible y eficiente**, evitando reentrenamientos costosos mediante el uso de:
- datasets intermedios persistidos,
- modelos entrenados almacenados,
- resultados parciales reutilizables.

El flujo principal del proyecto se ejecuta desde un **único notebook central**, que orquesta todo el pipeline de datos, entrenamiento y evaluación.

---

## Estructura del repositorio

```text
.
├── TFM_RipollVitiniLeopoldo_ML.ipynb
├── TFM_RipollVitiniLeopoldo_ML.html
├── src/
├── results/
├── CatBoost_LightGBM_MetaLogR_Stacking/
├── env/
├── doc/
├── README.md
└── LICENSE
```

## Descripción de carpetas y archivos

### `TFM_RipollVitiniLeopoldo_ML.ipynb`

Notebook principal del proyecto.

Contiene todo el flujo de trabajo:

- carga de datos  
- preprocesamiento  
- entrenamiento de modelos  
- evaluación  
- selección del modelo final  

El notebook se alimenta de datasets y modelos persistidos para evitar reentrenamientos largos.

Es el **punto de entrada principal** para reproducir el trabajo.

---

### `TFM_RipollVitiniLeopoldo_ML.html`

Versión exportada del notebook principal en formato HTML.

- Permite la lectura completa del trabajo sin necesidad de ejecutar código.
- Pensado para revisión académica, evaluación o consulta rápida.
- Refleja el contenido del notebook en el estado final del proyecto.

---

### `src/`

Contiene los datasets utilizados en el proyecto:

- datos iniciales proporcionados como punto de partida,
- datasets intermedios generados durante el preprocesamiento y la ingeniería de características,
- archivos preparados específicamente para las fases de entrenamiento.

---

### `results/`

Contiene resultados persistidos del proyecto:

- modelos entrenados intermedios,
- métricas y evaluaciones,
- salidas que permiten evitar recalcular procesos costosos.

Estos resultados permiten ejecutar el notebook completo sin necesidad de repetir entrenamientos largos.

---

### `CatBoost_LightGBM_MetaLogR_Stacking/`

Contiene el modelo final del TFM, basado en una arquitectura de *stacking* que combina:

- CatBoost  
- LightGBM  
- Regresión Logística como meta-modelo  

Incluye los modelos entrenados y los artefactos necesarios para la evaluación final.

---

### `env/`

Definición del entorno de ejecución del proyecto:

- `environment.yml`: entorno Conda utilizado durante el desarrollo.
- `requirements.txt`: dependencias en formato pip.

Permite reproducir el entorno de forma controlada y consistente.

---

### `doc/`

Documentación adicional del proyecto:

- documentación inicial proporcionada para la realización del TFM,
- material de referencia y apoyo metodológico.

---

## Reproducibilidad

El proyecto está diseñado para ser reproducible sin necesidad de reentrenar modelos desde cero.

### Creación del entorno

**Opción Conda:**
```bash
conda env create -f env/environment.yml
conda activate <nombre_del_entorno>
```

### Opción pip

```bash
pip install -r env/requirements.txt

```
## Ejecución del proyecto

1. Abrir el notebook `TFM_RipollVitiniLeopoldo_ML.ipynb`.
2. Ejecutar las celdas en orden.

El notebook detecta y reutiliza:

- datasets previamente generados,
- modelos entrenados,
- resultados almacenados en `results/`

---

## Licencia

Este proyecto se distribuye bajo la licencia indicada en el archivo `LICENSE`.

