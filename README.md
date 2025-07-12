# Análisis Retención Alumnos

Este repositorio contiene un cuaderno Quarto que analiza información académica para predecir la fuga de estudiantes. El objetivo es identificar tempranamente a quienes tienen riesgo de abandono y plantear acciones de retención más efectivas.

## Instalación de paquetes de R

Asegúrese de contar con R y, opcionalmente, RStudio. Instale los paquetes requeridos ejecutando:

```r
install.packages(c(
  "readxl", "ggplot2", "tidyverse", "ggdark",
  "skimr", "corrplot", "conflicted",
  "dplyr", "randomForest"
))
```

Si el proyecto incluye un archivo `renv.lock`, puede restaurar el entorno con:

```r
install.packages("renv")
renv::restore()
```

## Dataset `Reporte SIAE.xlsx`

El cuaderno espera un archivo de Excel llamado `Reporte SIAE.xlsx` ubicado en la carpeta raíz del proyecto. Si dispone del reporte, colóquelo en dicha ubicación. En caso contrario, solicítelo al equipo de datos o modifique la ruta en el código:

```r
carga <- readxl::read_excel("ruta/a/Reporte SIAE.xlsx", sheet = "Reporte SIAE", skip = 2)
```

## Renderizar el cuaderno a PDF

Para generar la versión PDF del análisis ejecute:

```bash
quarto render 'Analisis de Retención Alumnos.qmd' --to pdf
```

El documento `PDF` aparecerá en la misma carpeta del cuaderno.
