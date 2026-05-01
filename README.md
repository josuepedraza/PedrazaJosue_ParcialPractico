# JosuePedraza_ParcialPractico

Parcial práctico de **Detección de Fraude Bancario** desarrollado en **PySpark** para la asignatura **Machine Learning con PySpark y Docker**.

## Objetivo
Construir y comparar modelos de clasificación para detectar transacciones fraudulentas en un dataset altamente desbalanceado, y generar un archivo `submission.csv` con las predicciones finales sobre el conjunto de prueba.

## Estructura del repositorio

```text
JosuePedraza_ParcialPractico/
├── notebooks/
│   └── parcial_JosuePedraza.ipynb
├── docker/
│   ├── Dockerfile
│   └── docker-compose.yml
├── submission.csv
├── reporte.pdf
└── README.md
```

## Contenido del notebook
El notebook incluye:

- **EDA y preparación de datos en PySpark**
- **Modelo 1:** Logistic Regression
- **Modelo 2:** Random Forest
- **Modelo 3:** Stacking Manual
- Tabla comparativa de métricas
- Bitácora de experimentos del modelo asignado
- Análisis de errores específicos
- Generación del archivo `submission.csv`

## Datos utilizados
Se trabajó con tres archivos principales:

- `train.csv`: datos de entrenamiento con variable objetivo `Class`
- `test.csv`: datos de prueba sin labels
- `sample_submission.csv`: formato de referencia para la entrega final

## Modelos evaluados
Se compararon los siguientes modelos:

1. **Logistic Regression** como baseline
2. **Random Forest**
3. **Stacking Manual** como modelo asignado

## Mejor modelo
Después de la comparación de resultados, el **Random Forest** fue seleccionado como mejor modelo final, al mostrar el mejor equilibrio entre detección de fraude y control de falsas alarmas.

## Archivo de entrega
El archivo final generado fue:

- `submission.csv`

con las columnas:

- `id`
- `Class`

y el mismo formato que `sample_submission.csv`.

## Ejecución general
1. Cargar `train.csv`, `test.csv` y `sample_submission.csv`
2. Ejecutar el notebook completo en orden
3. Entrenar y comparar los tres modelos
4. Generar el archivo `submission.csv`

## Notas
- Todas las fases de **EDA y preparación** se realizaron en **PySpark**
- La semilla usada en las divisiones aleatorias corresponde a los últimos 4 dígitos de la cédula del estudiante
- El problema presenta un fuerte desbalance de clases, por lo que se priorizó especialmente el análisis de métricas sobre la clase fraude

## Autor
**Josué Pedraza**
