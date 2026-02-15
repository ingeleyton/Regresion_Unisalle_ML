# README

Este README describe exclusivamente el cuaderno `taller_regresion_prostata_sklearn.ipynb`.

## Objetivo del cuaderno

Resolver un problema de regresion supervisada para predecir `lpsa` (log del PSA) usando:

1. Regresion lineal sin regularizacion (OLS).
2. PCA + regresion lineal.
3. Comparacion de metricas y conclusiones.

## Archivos requeridos (misma carpeta)

- `taller_regresion_prostata_sklearn.ipynb`
- `prostate_data.txt`
- `prostate_info.txt`

## Requisitos de Python

- Python 3.11+ (recomendado: entorno `.venv` del proyecto)
- Paquetes:
  - `numpy`
  - `pandas`
  - `scikit-learn`
  - `matplotlib`
  - `seaborn`
  - `notebook`
  - `ipykernel`

Instalacion rapida:

```bash
source .venv/bin/activate
python -m pip install -U notebook ipykernel numpy pandas scikit-learn matplotlib seaborn
```

## Ejecucion del cuaderno

### Opcion 1: Jupyter Notebook

```bash
source .venv/bin/activate
jupyter notebook
```

Abrir `taller_regresion_prostata_sklearn.ipynb` y ejecutar todas las celdas en orden.

### Opcion 2: VS Code / Antigravity

1. Abrir el archivo `taller_regresion_prostata_sklearn.ipynb`.
2. Seleccionar kernel: `.venv (Python 3.13.7)` o el de tu entorno activo.
3. Ejecutar `Run All`.

## Estructura del notebook

1. Carga de librerias y datos.
2. Analisis exploratorio.
3. Preparacion `train/test` segun columna `train`.
4. Modelo OLS sin regularizacion.
5. Modelo PCA(95%) + OLS.
6. Comparacion de metricas (`MSE`, `RMSE`, `MAE`, `R2`).
7. Conclusiones finales.

## Resultados esperados en prueba

- OLS:
  - `MSE = 0.5213`
  - `RMSE = 0.7220`
  - `MAE = 0.5234`
  - `R2 = 0.5034`
- PCA(95%) + OLS (`k=7`):
  - `MSE = 0.4483`
  - `RMSE = 0.6696`
  - `MAE = 0.5259`
  - `R2 = 0.5729`

Interpretacion: en este caso, PCA+OLS mejora la generalizacion en test (menor RMSE y mayor `R2`).

## Problemas comunes

- Error `No se encontro prostate_data.txt`:
  - Ejecuta el notebook desde la carpeta donde esta el archivo.
- Error de kernel en VS Code:
  - Verifica que el kernel seleccionado sea el de `.venv`.
  - Confirma que `notebook` e `ipykernel` esten instalados en ese mismo entorno.
