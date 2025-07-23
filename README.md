# TelecomX-2

---

## Preparación de Datos

### Clasificación de Variables

- **Numéricas:** antigüedad_meses, Cuentas_Diarias, cargos_monthly, etc.
- **Categóricas:** tipo_contrato, soporte_técnico, películas_streaming, etc.
### Preprocesamiento
- Se aplicó **one-hot encoding** a las variables categóricas para convertirlas a formato numérico.
- Se normalizaron variables numéricas relevantes como `antigüedad_meses`, `Cuentas_Diarias` y `cargos_monthly`, ya que se usaron modelos sensibles a la escala (como Regresión Logística).
- Se manejaron valores nulos y columnas irrelevantes fueron eliminadas para evitar ruido en el modelo.
---
### División del Dataset
- Se dividieron los datos en:
  - **Conjunto de entrenamiento (80%)**
  - **Conjunto de prueba (20%)**
- Esta separación permite evaluar la capacidad de generalización de los modelos entrenados.
---
## Modelos y Justificaciones
Se desarrollaron dos modelos:
1. **Regresión Logística:**  
   Requiere normalización. Se eligió por su interpretabilidad y rendimiento en clasificación binaria.
2. **Random Forest:**  
   No requiere normalización. Se seleccionó por su capacidad de manejar relaciones no lineales y su alta precisión.
Se evaluaron los modelos con métricas como **accuracy**, **precision**, **recall**, **f1-score** y **matriz de confusión**.
> **Resultado:** Random Forest obtuvo una precisión cercana al 99.7%, aunque se evaluó cuidadosamente para detectar posible overfitting.
---
## Análisis Exploratorio (EDA)
Durante el EDA se generaron visualizaciones para explorar la relación entre las variables y la cancelación:

- **Boxplots y scatterplots**: para observar patrones entre el gasto total, antigüedad y churn.
- **Matriz de correlación**: para analizar relaciones entre variables numéricas.
- **Distribuciones**: para detectar clases desbalanceadas y características dominantes.
---
## Insights Clave

- Clientes con **menos antigüedad** y **gastos mensuales altos** son más propensos a cancelar.
- La falta de servicios complementarios (como soporte técnico o respaldo en línea) se asocia con mayor churn.
- La cancelación está más concentrada en contratos a corto plazo.
