# Seguridad y Percepción Ciudadana en Querétaro (ENVIPE 2021–2025)

## Descripción del proyecto

Este repositorio contiene un análisis exploratorio y descriptivo de la evolución de la percepción ciudadana sobre la seguridad pública, la confianza institucional y la victimización en el estado de Querétaro, utilizando información proveniente de la **Encuesta Nacional de Victimización y Percepción sobre Seguridad Pública (ENVIPE)** publicada por el Instituto Nacional de Estadística y Geografía (INEGI).

El estudio integra información correspondiente al periodo **2021–2025**, permitiendo identificar tendencias, cambios y patrones en diversos indicadores relacionados con la seguridad ciudadana y la confianza en las instituciones encargadas de la prevención y procuración de justicia.

## Indicadores analizados

- Percepción de corrupción en autoridades de seguridad.
- Confianza en la Guardia Nacional.
- Sensación de seguridad al caminar por la noche.
- Confianza entre vecinos.
- Restricción de actividades por temor a la delincuencia.
- Participación en estrategias de prevención comunitaria.
- Percepción general de inseguridad.

## Productos generados

El proyecto genera distintos productos analíticos y visuales, entre ellos:

- Gráficos .
- Mapas temáticos del estado de Querétaro.
- Reportes reproducibles en formato HTML mediante R Markdown.

## Estructura del proyecto (codigo adjuntado como MAR.Rmd)

```text
Repositorio/
│
├── MAR.Rmd
├── qro.csv
│
└── datos/
    ├── 2021/
    │   └── TPer_Vic1.csv
    ├── 2022/
    │   └── TPer_Vic1.csv
    ├── 2023/
    │   └── TPer_Vic1.csv
    ├── 2024/
    │   └── TPer_Vic1.csv
    └── 2025/
        └── TPer_Vic1.csv
```

## Requisitos

### Software

- R 4.2 o superior
- RStudio 

### Dependencias

Instala las librerías necesarias ejecutando:

```r
install.packages(c(
  "dplyr",
  "tidyr",
  "ggplot2",
  "scales",
  "knitr",
  "stringi"
))
```

## Configuración de archivos

Para facilitar la reproducción del análisis en cualquier equipo, se recomienda utilizar rutas relativas dentro del repositorio.

### Directorio de datos

```r
base_dir <- "datos"
```

La carpeta `datos` debe contener los archivos adjuntos llamados bd_envipe_2021-2025 correspondientes a cada año de estudio.

### Archivo cartográfico

```r
mapa_qro <- read.csv("qro.csv")
```

Asegúrate de que el archivo `qro.csv` adjuntado se encuentre en la raíz del repositorio.

## Ejecución

Abre el archivo `MAR.Rmd` en RStudio y ejecuta:

```r
rmarkdown::render("MAR.Rmd")
```

o utiliza el botón **Knit** para generar automáticamente el informe(se adjunta ya el archivo llamado MAR.html).

## Fuente de datos

**Instituto Nacional de Estadística y Geografía (INEGI)**

Encuesta Nacional de Victimización y Percepción sobre Seguridad Pública (ENVIPE)

https://www.inegi.org.mx/programas/envipe/

## Autores

- Wendolyn Sóstenes Gómez
- José Manuel Flores Reséndiz
- Jesús Gabriel Díaz
