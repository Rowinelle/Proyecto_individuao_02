# Repositorio del Proyecto Individual 02

### Presentación
Aquí en contrarás el desarrollo del proceso de de Data Analytics, en el marco de los proyectos individuales de Henry.  En esta ocasión, se nos ha solicitado explorar las características de los productos ofrecidos en los MOOCs (Massive On Line Open Courses), analizando la oferta de tres empresas ya consolidadas, como  son Coursera, Edx y Udemy. 
Pasaré a desarrollar los pasos realizados.


####ETL
Los datasets provistos fueron tratados con Pandas, se realizaron las modificaciones correspondientes y luego se descargaron los archivos ya limpios para utilizarlos en el análisis exploratorio.
Los criterios utilizados fueron:
- conversión de las fechas a Timestamp;
- extracción y creación de columnas para Mes y Fecha;
- conversión a Categorías de las variables nominales; 
- conversión de datos booleanos a variables dicotómicas;
- discretización de variables continuas con el fin de poder operar sobre ellas. Se ha calculado la cantidad de intervalos y la amplitud de los mismos, y se agregó una columna para la marca de clase;
- se eliminaron columnas que no serían utilizadas en el EDA;
- se agregaron índices cuando era necesario para su posterior tratamiento;
- se unieron los datasets de Coursera;
- se eliminaron datos duplicados cuando se valoró que afectaría las operaciones;
A continuación, se encuentra el detalle del etl realizado:

`ETL` : <https://github.com>

####EDA
El análisis exploratorio se realizó con Pandas, Matplotlib y Seaborn. Comenzó con una revisión general de las características de los datasets y cuestiones de forma. 
Previo a pasar al análisis de las cuestiones de contenido, se indagó un poco mas sobre las características principales de los MOOCs, su funcionamiento, problemáticas que enfrentan, etc. En el presente documento se detallan las fuentes utilizadas. 
A partir de ahí, se decidió guiar el EDA, con el fin de explorar cuáles son los factores mas determinantes a la hora de planificar este negocio, y si además de los factores materiales propios de la diversidad de cursos, podríamos lograr un acercamiento a, algo mas intangible, como son los factores psicosociales.
Se decidió entonces trabajar sobre dos conductas medibles de los usuarios: la suscripción a un curso y el open feedback, ya que ambas son medidas que queremos ver crecer en nuestro negocio. 

En el caso del open feedback tal vez sea menos evidente su rol, pero a partir de la investigación realizada, se define como una medida indirecta del nivel de engagemente del usuario, ya que se ha estudiado entre aquellos usuarios con mayor nivel de engagement se observaron con mas frecuencia acciones como participar en los foros del curso, o brindar open feedback sobre el mismo. Por eso se cree que a partir de su análisis, se puede inferir qué porcentaje de usuarios inscriptos a un curso, finalizarán el mismo, o inclusive, cuántos pueden volver  a tomar un curso en el futuro. 

Se utilizaron los datasets facilitados por Henry, y además se usaron datos de la Open University y un dataset extra de Coursera, disponible en Kaggle.




#####Análisis univariado
Se valoró las características generales de los productos ofrecidos y de las reviews emitidas por los usuarios.
Se datallan algunos de los hallazgos mas importantes: 
- Udemy publicó 3.678 cursos en el período estudiado, desde 2011 a 2017. En ese período, contó con un total de 11.759.120 incriptos;
- la media del precio de los cursos para Udemy ronda entre los 40 y 50 UDS, mientras que los de Edx rondan los 100 UDS. La cantida de cursos pagos es significativamente mayor a la cantidad de cursos gratuitos;
- estudiando los meses de publicación de los cursos, se observa una leven tendencia a descender durante los meses de receso académico en el hemisferio norte y durante el receso navideño,
- la cantidad de cursos ofrecidos de nivel básico/principiante supera ampliamente la oferta para los niveles intermedios y avanzados;
- entre las áreas que cuentan con mayor oferta de cursos, se destacan el rubro IT y Business/finanzas;
- en general, los cursos ofrecidos por las plataformas estudiadas, cuentan con un número significativamente mayor de reseñas positivas (4 o 5 puntos de rating), por sobre las reseñas negativas; 
- el número de reseñas obtenidas por cursos de Coursera aumentó significativamente durante el año 2020, indicando posiblemente un aumento de suscriptos en el contexto de pandemia;
- entre los adjetivos utilizados para las reseñas positivas de los cursos, se encuentran: easy, amazing, awesome, interesting, helpful, great, excellente, useful, informative, best, challenging, clear, entre otros.
- el número de cursos ofrecidos en inglés es significativamente mayor que para el resto de los idiomas, contando 777 cursos en dicho idioma en la plataforma EDX. En segundo lugar se encuentra el idioma español, con una oferta de 176 cursos;



#####Análisis multivariado
Se valoraron resultados obtenidos de analizar el interjuego de distintas variables entre sí.
Algunas de las conclusiones son:
- los usuarios eligen los cursos pagos por sobre los gratuitos. No se observan variaciones en esta conducta en función del nivel del curso; 
- la cantidad de inscriptos en cursos básicos es significativamente mayor que para el resto de la oferta. Para Udemy se observó que la cantidad de inscriptos en cursos de nivel básico fue de 4.051.843 en el período analizado, mientras que para los niveles intermedio y avanzado fue de 742.005 y 50196, respectivamente. Esta tendencia se mantiene independientemente del área del curso; 
- la cantidad de cursos ofrecidos para las áreas IT y Business/finanzas es similar, sin embargo  la cantidad de inscriptos es significativamente mayor en IT;
- los cursos en idioma italiano tuvieron una gran cantidad de incriptos, resultado en un ganancia promedio de 3.449.416 por curso, superando a la ganancia promedio obtenida por los cursos en español;
- los cursos de nivel avanzado resultan en una ganancia mayor, por encima de los básicos e intermedios;



`EDA y KPIs` : <https://github.com>


#####Fuentes
- Dropout: MOOC participants’perspective. T. Liyanagunawardena, Patrick Parslow, S. Williams.
- The MOOC dropout phenomenon and retention strategies. Joselyn GoopioORCID Icon &Catherine Cheung.
- Understanding Dropouts in MOOCs. Wenzheng Feng, Jie Tang and Tracy Xiao Liu.
- Open University Learning Analytics dataset. Jakub Kuzilek, Martin Hlosta & Zdenek Zdraha.
