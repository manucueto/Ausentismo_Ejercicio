# Proyecto de Predicción de Ausentismo

## Descripción

Este proyecto en Python tiene como objetivo predecir el ausentismo de empleados en una empresa utilizando modelos de aprendizaje automático. Incluye un módulo que permite cargar, limpiar y preprocesar datos, así como realizar predicciones sobre el ausentismo.

## Contenido

El proyecto incluye el archivo `absenteeism_module.py`, que contiene:

- **Clases**:
  - `CustomScaler`: Una clase personalizada que extiende `BaseEstimator` y `TransformerMixin` de Scikit-learn para normalizar columnas específicas de un DataFrame.
  - `absenteeism_model`: Clase principal que maneja la carga de modelos y datos, así como la predicción del ausentismo.

## Requisitos

Asegúrate de tener instaladas las siguientes bibliotecas:

- numpy
- pandas
- scikit-learn

Puedes instalarlas usando pip:

```bash
pip install numpy pandas scikit-learn
```

## Uso

### Inicialización del Modelo

Para utilizar el modelo, crea una instancia de `absenteeism_model` pasando los archivos del modelo y del escalador:

```python
model = absenteeism_model('model_file.pkl', 'scaler_file.pkl')
```

### Cargar y Limpiar Datos

Usa el método `load_and_clean_data` para cargar y preprocesar un archivo CSV:

```python
model.load_and_clean_data('data_file.csv')
```

### Predicciones

Puedes obtener la probabilidad de ausentismo y la categoría de predicción usando los siguientes métodos:

- Para obtener la probabilidad:
  ```python
  probabilities = model.predicted_probability()
  ```

- Para obtener la predicción:
  ```python
  predictions = model.predicted_output_category()
  ```

- Para obtener un DataFrame con las predicciones añadidas:
  ```python
  results = model.predicted_outputs()
  ```

## Estructura del Código

- **Importación de Bibliotecas**: Se importan las bibliotecas necesarias.
- **CustomScaler**: Escalador personalizado para manejar la normalización de datos.
- **absenteeism_model**: Clase que gestiona la carga de datos, la limpieza y las predicciones.

## Contribuciones

Las contribuciones son bienvenidas. Si deseas mejorar este proyecto, por favor abre un issue o envía un pull request.

## Licencia

Este proyecto está bajo la licencia MIT. Puedes usarlo y modificarlo bajo los términos de esta licencia.

---

Si tienes alguna pregunta o necesitas ayuda, no dudes en contactar al autor del proyecto.
