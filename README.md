## <h1 align=center> Proyecto Individual No. 3. Data Analytics
## <h1 align=center> Etapa de LABs - Carrera: Data Science

<p align="center">
<img src=https://user-images.githubusercontent.com/109157476/213493684-d39b7139-403c-4dac-873f-2505d3ec7fd9.png>

# <h1 align=center> Por: Janice Rico

<p align="center">
<img src=https://user-images.githubusercontent.com/109157476/215916812-bb335304-f6f5-4efd-ba33-166781f9c336.png>

## <h1 align=center> TEMA:
# <h1 align=center> Análisis de los MOOCs: Massive Open Online Courses
  
## <h1 align=center> INTRODUCCIÓN
 
En esta era de la comunicaciones y donde la tecnología permite conectarse de forma remota, el área educativa y de aprendizaje no se queda atrás. Los Cursos Masivos Abiertos Online están siendo la mejor manera de reunir tanto a instructores/instituciones como a estudiantes de distintas partes del mundo, con distintos trasfondos, con algo en común para todos: Conocimientos (unos impartiendo, los otros recibiendo)!!! Casi cualquier tema puede ser enseñado de forma online, haciendo de esta modalidad un negocio con alta rentabilidad por parte de las plataformas que lo ofrecen.
  
En esta ocasión, asumiendo el rol de Data Analyst, se tiene la tarea de realizar un análisis de tres plataformas educativas, para sacar conclusiones tomando en cuenta los precios de los cursos que ofrecen, los idiomas disponibles, niveles de enseñanza y ratings por parte de los consumidores de estos productos. Esto, con el fin de dar recomendaciones a una Startup de tecnología que desea invertir en el mercado de los cursos en línea.

## <h1 align=center> DATOS

4 Tablas contenidas en archivos .csv correspondientes a las Plataformas: Coursera, edX y Udemy (Coursera_courses.csv, Coursera_reviews.csv, edx_courses.csv, udemy_courses.csv).
  
Se pueden extraer del siguiente link: https://drive.google.com/drive/folders/1i0Xx_ArNgErwc9mPeL1TtKEPRlBf3yaC?usp=share_link
 
## <h1 align=center> TRANSFORMACIONES REQUERIDAS (Procesos de EDA y ETL)

Se tomó una extensa porción de tiempo para adentrarse en los datos que contenían las tablas, detectando tipos de datos, cantidad de filas y columnas, datos nulos y posibles outliers.
  
A partir de allí se realizó el proceso de ETL en un cuaderno de Jupyter, donde se descartaron columnas no útiles para este estudio, relleno de campos con valores nulos, eliminación de registros duplicados, separación de información de una columna donde se necesitaba extraer precios de cursos y normalización de nombres de columnas para su posterior comparación.
  
Esta labor quedó plasmada en el archivo: EDA - MOOCs.ipynb

## <h1 align=center> WORDCLOUD

Se solicitó la creación de una Nube de Palabras con las que más se repetían en los títulos de los cursos, con la finalidad de tener una idea generalizada del contenido presente en las plataformas.
  
Dicho objeto se generó a través de Python, para lo cual se puede consultar el siguiente cuaderno de Jupyter: WordCloud.ipynb, y el resultado final se guardó en: wordcloud.png (Carpeta WordCloud)
  
## <h1 align=center> ANÁLISIS

Ya teniendo a disposición la información de los datasets más clara para su lectura e interpretación, se exportaron a nuevos archivos .csv (coursera_reviews_NEW.csv, edx_courses_NEW.csv, udemy_courses_NEW.csv), de igual forma ubicados en el drive descrito arriba, para usarlos en las gráficas del análisis. Para ello se escogió la plataforma de Power BI, donde se cargaron las nuevas bases de datos, y se realizaron unos pequeños retoques a los datos (cambio de tipo de dato de la columna 'n_enrolled' de la tabla de edX, y luego el reemplazo de datos nulos con el promedio de la misma columna). Se hicieron gráficos respecto al precio, idioma, nivel y rating de los cursos.
  
El archivo donde se resumieron dichas labores es: Dashboard.pbix (ubicado en el siguiente drive: https://drive.google.com/drive/folders/1zCyTQ4Hjx9d0aC3tlOflcKKVKRpzcXog?usp=share_link)
  
**Idioma**: Se pudo apreciar que el idioma inglés es el que predomina en casi todos los matriculados.
 
**Rating**: Se detectó que los ratings máximos (5 puntos) se le otorgaron a menor cantidad de cursos, pero con mayor demanda.
  
**Nivel y Precio**: Los cursos menos costosos son los Introductorios, en segundo lugar los Intermedios, y los que tienen precios más altos corresponden a los Avanzados.

 ## <h1 align=center> KPIs

De acuerdo a los datos suministrados y sacando conclusiones de los mismos, se plantearon básicamente 2 KPIs:

1. De la plataforma Coursera, el Rating promedio de acuerdo a la cantidad de suscriptores que dejaron su opinión/crítica por curso, lo que indica su grado de satisfacción.

2. De las plataformas edX y Udemy, el Cálculo de Ganancias Promedio por Suscriptores que pagaron por un Certificado. Como muchos de estos cursos son gratuitos y se paga es por la certificación, asumí que sólo el 25% paga para obtenerla.
  
## <h1 align=center> RECOMENDACIONES

De acuerdo a lo observado en los gráficos se realizaron las siguientes Recomendaciones:

- Ofrecer cursos en Inglés en su mayoría.
- Mejorar cursos con menos rating.
- Establecer planes de precios híbridos: Por curso y por mes, más competitivos.
- Conocer las preferencias del público.
- Ofrecer capacitaciones a todo el equipo de un área específica en empresas/instituciones.
 
