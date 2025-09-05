<!-- GIF HEADER -->
<img src="https://michaelwashburnjr.com/hubfs/Imported_Blog_Media/python.jpg">

# Descripción

El lenguaje de programación Python es un lenguaje de alto nivel, interpretado y de propósito general, reconocido por su sintaxis clara y legible. 
Gracias a su versatilidad, facilidad de enseñanza y vasta colección de librerías, se considera una piedra angular en variadas aplicaciones tales como: desarrollo web, análisis de datos y aprendizaje automático, automatización de tareas, compitación científica y visualización de datos. 

## Dataset
El dataset utilizado en este proyecto trata de una base de datos relacionada a la prevalencia de diabetes en mujeres jóvenes. En específico, se encuentra en este **link** y contiene las siguientes columnas:

Pregnancies: Número de embarazos
Glucose: Concentración de glucosa en plasma 2 horas después de una prueba de tolerancia oral a la glucosa
BloodPressure: Presión arterial diastólica (mm Hg)
SkinThickness: Grosor del pliegue cutáneo del tríceps (mm)
Insulin: Insulina sérica de 2 horas (mu U/ml)
BMI: Índice de masa corporal (peso en kg / (altura en m)^2)
DiabetesPedigreeFunction: Función del pedigrí de diabetes
Age: Edad (años)
Outcome: Variable de clase (0 o 1)

## Análisis
Se importaron las librerías pandas, kagglehub, numpy, seaborn y matplotlib para el análisis del proyecto.

Se conectó directamente el dataset con el path de kaggle **path = kagglehub.dataset_download("mathchi/diabetes-data-set")**.

Una vez importado el dataset y creado el dataframe, se comienza con un análisis EDA para conocer los datos y la base.
En primer lugar, se analizan los tipos de variables y se confirma que todas son numéricas. En segundo lugar se revisa si existen valores faltantes en el dataset para confirmar de manera programática y visual que no existen valores faltantes
