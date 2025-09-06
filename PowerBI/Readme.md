<!-- GIF HEADER -->
<img src="https://www.vuepilot.com/wp-content/uploads/2021/02/power-bi-banner.jpg">

# Descripción

Power BI es una plataforma de inteligencia de negocios (Business Intelligence) de Microsoft que transforma datos sin procesar en información comprensible, visualmente atractiva y fácil de usar. Es una herramienta poderosa para el análisis de datos y la visualización que permite a los usuarios conectar, modelar y visualizar datos de diversas fuentes.
Dentro de sus funcionalidades destaca la conectividad, modelado (DAX) y visualización de datos además de su colaboración y compartición de fácil acceso con cuentas gratuitas.

## Dataset
Se utilizó el dataset ["ATP Tennis 2000 - 2025 Daily update"](https://www.kaggle.com/datasets/dissfya/atp-tennis-2000-2023daily-pull/data) para analizar y visualizar distintos partidos de tenis llevados a cabo desde 2000 hasta la actualidad. 
A modo de preparación de los datos, se tradujeron algunas variables y sus valores para que fuese más comprensible el dashboard para el público hispanoparlante. Esto se realizó desde el transformador de datos de Power BI reemplazando los datos. Además, se cambió el formato de la columna "Date" a fecha ya que venía como texto.
Adicionalmente, se creó una variable con lenguaje DAX que permite conocer la diferencia de ranking entre finalistas de un torneo (considerando el ranking del ganador como base). La semántica de la fórmula es la siguiente:
```
Diferencia de Ranking = 
IF(
    'atp_tennis'[Winner] = 'atp_tennis'[Player_1],
    'atp_tennis'[Rank_1] - 'atp_tennis'[Rank_2],
    'atp_tennis'[Rank_2] - 'atp_tennis'[Rank_1]
)```
## Informe
El informe cuenta con 3 hojas y contienen diferente infomración:

### 1.- Detalle de Finales:
El usuario podrá controlar mediante segmentadores, la categoría del torneo (ATP 250, ATP 500, ATP 1000, Masters, Grands Slam), el nombre del torneo y el año del mismo.
Una vez seleccionados los valores, el dashboard mostrará los jugadores que disputaron la final y el ganador del torneo con el score y diferencia de ránking.
Un detalle estético es que el color de tipografía para el tipo de superficie varía según sea arcilla, hierba o pista rápida. A continuación unos ejemplos de estas combinaciones:
![Ejemplo1_Finales](Muestras)  
