# Instalación del entorno

Esta guía explica cómo crear un entorno virtual de Python e instalar las librerías del curso usando `requirements.txt`.

## Requisitos

- Tener instalado Python >=3.10 .
- Acceso a una terminal.
- El archivo `requirements.txt` en la carpeta raíz del proyecto.

Comprueba la versión de Python:

```powershell
python --version
```

Se recomienda utilizar Python 3.10 para mantener compatibilidad con las versiones definidas en el proyecto.

## 1. Crear el entorno virtual

Abre PowerShell o una terminal en la carpeta del proyecto y ejecuta:

```powershell
python -m venv .venv
```

## 2. Activar el entorno

En Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

En Windows mediante CMD:

```bat
.venv\Scripts\activate.bat
```

Cuando el entorno esté activo, aparecerá `(.venv)` al inicio de la línea de comandos.

Si PowerShell bloquea la activación por la política de ejecución, abre PowerShell como usuario y ejecuta:

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

Después, vuelve a ejecutar el comando de activación.

## 3. Actualizar pip

```powershell
python -m pip install --upgrade pip
```

## 4. Instalar las librerías

```powershell
python -m pip install -r requirements.txt
```

El archivo incluye librerías para:

- procesamiento numérico y tabular;
- lectura y escritura de archivos Excel, Parquet, XML y HTML;
- procesamiento de imágenes;
- visualización;
- estadística y aprendizaje automático;
- JupyterLab y widgets interactivos.

## 5. Registrar el entorno en Jupyter (Opcional)

```powershell
python -m ipykernel install --user --name lpd_curso_2026 --display-name "Python (LPD 2026)"
```

Después, abre JupyterLab:

```powershell
jupyter lab
```

Si usas VS Code, abre un notebook `.ipynb`, selecciona **Select Kernel** y elige `Python (LPD 2026)`.

## 6. Verificar la instalación

Ejecuta el siguiente comando:

```powershell
python -c "import numpy, pandas, scipy, openpyxl, xlrd, matplotlib, seaborn, plotly, sklearn, statsmodels, PIL, cv2, skimage, imageio; print('Instalación correcta')"
```

También puedes comprobar las versiones instaladas:

```powershell
python -m pip list
```

## Desactivar el entorno

Cuando termines de trabajar:

```powershell
deactivate
```
