> ![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image1.png){width="1.9291666666666667in"

> height="0.508332239720035in"}

![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image2.png){width="2.8555555555555556in"

height="0.775in"}

> **ANÁLISIS DE LA CALIDAD DEL AIRE EN NUEVO LEÓN** Una Forma De

> Predecir Para Prevenir

+-----------------------+-----------------------+-----------------------+

| > **Alarcón Acosta    | **Castro Terrazas     | > **Fernández Merino  |

| > Christian**         | Rubén Darío**         | > Pedro**             |

+=======================+=======================+=======================+

| > a00832881@tec.mx    | a00833945@tec.mx      | a01733006@tec.mx      |

+-----------------------+-----------------------+-----------------------+

| > **Montes Raygoza    |                       | > **Orantes Guillén   |

| > Juan José**         |                       | > José Andres**       |

+-----------------------+-----------------------+-----------------------+

|                       | **Ciencia de Datos y  |                       |

|                       | Matemáticas**         |                       |

+-----------------------+-----------------------+-----------------------+

|                       | > Aplicación de       |                       |

|                       | > métodos             |                       |

|                       | > multivariados en    |                       |

+-----------------------+-----------------------+-----------------------+

|                       | ciencia de datos      |                       |

|                       | (Gpo. 101)            |                       |

+-----------------------+-----------------------+-----------------------+

| > a00834630@tec.mx    |                       | a01174130@tec.mx      |

+-----------------------+-----------------------+-----------------------+

|                       | > Dra. Elizondo Amaya |                       |

|                       | > Mónica Guadalupe    |                       |

|                       | > **Responsables del  |                       |

|                       | > Grupo:**            |                       |

|                       | >                     |                       |

|                       | > Dra. Elizondo Amaya |                       |

|                       | > Mónica Guadalupe    |                       |

|                       | > Dra. Ruiz Hernández |                       |

|                       | > Blanca Rosa         |                       |

|                       | >                     |                       |

|                       | > Dra. Ruiz Hernández |                       |

|                       | > Blanca Rosa         |                       |

+-----------------------+-----------------------+-----------------------+

**RESUMEN**

La contaminación del aire es un problema global que afecta la salud

humana, el medio ambiente y el cambio climático. Este informe se enfoca

en la calidad del aire en Monterrey, Nuevo León, y utiliza análisis

factorial y discriminante para comprender cómo varios factores

interconectados impactan en la calidad del aire y desarrollar un modelo

de predicción.

Los factores identificados incluyen variables meteorológicas,

contaminantes atmosféricos, factores climáticos y el tiempo. El análisis

factorial reduce la complejidad de los datos y revela que los gases

contaminantes son factores clave en la calidad del aire. El análisis

discriminante logra una precisión del 70% en la clasificación de la

calidad del aire. Los resultados tienen relevancia para la salud pública

y el bienestar, y pueden ayudar en la toma de decisiones para mejorar la

calidad del aire. Se menciona que otros países han utilizado tecnologías

avanzadas para predecir la calidad del aire y proteger la salud pública.

**CONCEPTOS CCS**\

• R Studio

**PALABRAS CLAVE**

Aire, contaminación, análisis factorial y discriminante.

**1 -- INTRODUCCIÓN**\

La contaminación del aire es un problema global de gran relevancia

debido a sus impactos en la salud humana, el medio ambiente y el cambio

climático. Se origina principalmente a partir de fuentes como la quema

de combustibles fósiles, emisiones industriales, tráfico vehicular y

prácticas agrícolas. En Nuevo León y su zona metropolitana, estas

actividades tienen un impacto

> significativo en la calidad del aire. La contaminación del aire es uno

> de los principales riesgos ambientales para la salud humana, Según la

> Organización de las Naciones Unidades es una causa de enfermedades

> cardiacas, accidentes cerebrovasculares, cáncer pulmonar, asma y otras

> enfermedades, y contribuyendo a 6.7 millones de muertes prematuras

> anualmente \[1\].

> Por otro lado, las estadísticas suministradas por la

> National Weather Service han cuantificado en 150 mil

> millones de dólares anuales los costos económicos asociados

> a la contaminación, solo en los Estados Unidos \[2\]. Queda

> claro, que por el bienestar de la economía y, aún más

> importante, por la preservación de la salud, se torna imperativo

> resguardar la calidad del aire que nos rodea.

> Resulta esencial comprender los aspectos cruciales

> que son considerados al analizar la calidad del aire, y

> familiarizarse con las clasificaciones internacionales de los

> contaminantes más relevantes, así como identificar aquellos

> que poseen un impacto particularmente perjudicial para la

> salud. Dicha información enriquecerá sustancialmente el

> contenido de este reporte. Entre los aspectos fundamentales

> que se destacan para evaluar la calidad del aire figuran:

> **Partículas****suspendidas (PM2.5****y****PM10):** Minúsculas

> partículas dañinas en el aire, con 2.5 micrómetros y hasta 10

> micrómetros de diámetro \[3\].

> **Niveles elevados de ozono (O3):** El ozono, que protege de los rayos

> UV en la estratósfera, puede generar contaminación perjudicial,

> conocida como \"smog\", con consecuencias adversas para la salud

> \[4\].

> ITESM, Ciencia de Datos y Matemáticas

> **Dióxido de nitrógeno:** Este gas contribuye a la formación del

> \"smog\" y está relacionado con problemas respiratorios.

> **Dióxido de azufre:** Emitido principalmente por la quema de

> combustibles fósiles, puede dar origen a la lluvia ácida y otros

> impactos ambientales \[5\].

> **Plomo:** Provoca efectos en la salud y el desarrollo humano, como la

> disminución del coeficiente intelectual, daños auditivos, habilidades

> cognitivas debilitadas y tasas más altas de criminalidad \[6\]. En el

> siglo XX, el plomo contribuyó al deterioro del desarrollo infantil en

> Estados Unidos, destacando su impacto negativo en la sociedad.

La medición de la calidad del aire implica el uso de sistemas de

vigilancia equipados con sensores diseñados para detectar contaminantes,

tanto naturales como antropogénicos, como la quema de combustibles

fósiles \[7\]. Algunos contaminantes clave incluyen PM2.5, PM10, ozono

troposférico, dióxido de carbono, dióxido de nitrógeno y dióxido de

azufre \[8\]. Estos se traducen en un Índice de Calidad del Aire (ICA)

que varía de 0 a 500, con valores superiores a 100 indicando niveles

poco saludables \[9\].

Además de los contaminantes, las estaciones meteorológicas consideran

factores como dirección y velocidad del viento, humedad, temperatura y

precipitación en su análisis. Estos factores meteorológicos influyen en

la dispersión de contaminantes y patrones de contaminación.

A pesar de los avances tecnológicos, la medición de la calidad del aire

enfrenta desafíos debido a la falta de estandarización en los métodos de

medición, variabilidad en lugares y momentos, y la complejidad de los

contaminantes y sus efectos en la salud humana \[10\].

La falta de uniformidad en los enfoques de medición dificulta la

comparación y evaluación de datos, lo que a su vez complica la toma de

decisiones informadas debido a la variabilidad en la calidad del aire,

impulsada por múltiples fuentes de contaminación, condiciones climáticas

cambiantes y características topográficas \[10\].

Además, la amplia gama de contaminantes y sus efectos complejos en la

salud requieren equipos y metodologías especializadas \[10\]. La falta

de requisitos legales para la medición de la calidad del aire en un 37%

de los países, según el PNUMA, limita la disponibilidad de datos

confiables y obstaculiza la formulación de políticas

Alarcón C, Castro R, Fernández P, Montes J, Orantes A.

> efectivas para controlar la contaminación del aire y proteger la salud

> pública \[11\].

> En México, se han establecido programas Pro-Aire, como el programa

> SIMA en Nuevo León (Sistema Integral de Monitoreo Ambiental), para

> abordar las necesidades estatales en cuanto a herramientas preventivas

> y correctivas para la calidad del aire y la protección de la salud

> \[12\]. Estos esfuerzos buscan superar los desafíos mencionados y

> mejorar la comprensión y mitigación de los riesgos asociados con la

> contaminación del aire.

> **2 -- METODOLOGÍA**

> Este proyecto se trabaja bajo la metodología

> CRISP-DM, que ofrece un enfoque estructurado y

> sistemático para la minería de datos: este consta de seis fases

> principales:

> **1. Comprensión del negocio:** Se comprenden los objetivos y

> requisitos.

> **2. Comprensión de los datos:** Se recopilan y exploran los

> datos disponibles para comprender su calidad, relevancia y

> características.

> **3. Preparación de los datos:** Los datos se transforman y se crean

> conjuntos de datos adecuados para el análisis.

> **4. Modelado:** Se seleccionan y se entrenan modelos de minería de

> datos, para abordar los objetivos del proyecto.

> **5. Evaluación:** Se evalúan los modelos generados en

> términos de su rendimiento y se ajustan según sea necesario.

> **6. Despliegue:** Los resultados del modelo se implementan

> en el entorno de producción, y se crean estrategias para el

> seguimiento continuo y la actualización.

> **3 -- COMPRENSIÓN DEL NEGOCIO**

> El programa SIMA, respaldado por el Gobierno del

> Estado de Nuevo León, se enfoca en evaluar la calidad del

> aire mediante la monitorización de las concentraciones

> atmosféricas a las que está expuesta la población.

> Específicamente, en situaciones adversas, el programa

> asume la función de alertar a la población en casos donde los niveles

> de contaminación atmosférica son elevados \[13\].

> Una característica destacada del programa es su

> capacidad para proporcionar información actualizada

ANÁLISIS DE LA CALIDAD DEL AIRE Septiembre de 2023, Monterrey, Nuevo

León Una forma de predecir para prevenir

constantemente sobre la calidad del aire en la región donde opera, con

un enfoque principal en la zona metropolitana de Monterrey. La

Secretaría de Medio Ambiente es la entidad encargada de gestionar este

programa.

A lo largo de este proyecto SIMA toma un papel fundamental al

posicionarse como socio formador académico y otorgarnos la base de

datos, así como su apoyo para realizar con éxito nuestra investigación.

**3.1 -- DESCRIPCIÓN DEL PROBLEMA**

El problema central que abordamos en esta investigación se relaciona con

la contaminación del aire en el estado de Nuevo León, que es

influenciada por una variedad de factores climatológicos y contaminantes

atmosféricos. Nuestro objetivo principal es analizar en

> **Variabilidad del Medio Ambiente:** La relación entre factores

> meteorológicos y contaminantes influye en la variabilidad ambiental.

> **Identificación de Riesgos:** Permite identificar contaminantes

> peligrosos y cuándo alcanzan niveles críticos.

> **Toma de Decisiones Informada:** Facilita la toma de decisiones

> basada en datos para reducir la contaminación y sus efectos.

> **4 -- MARCO TEÓRICO**

> Para llevar a cabo este trabajo, utilizaremos herramientas de análisis

> multivariado, como la exploración de variables, modelos de análisis

> factorial y modelos de análisis discriminante, con el objetivo de

> predecir y evaluar

+-----------------------+-----------------------+-----------------------+

| profundidad           | > cómo estos          | > la calidad del aire |

|                       | > diferentes factores | > de manera efectiva. |

|                       | > están               |                       |

+=======================+=======================+=======================+

+-----------------------+-----------------------+-----------------------+

interconectados entre sí y cómo ejercen un impacto significativo en la

calidad del aire en la región. Posteriormente, planeamos desarrollar un

modelo de predicción que nos permita determinar si la calidad del aire

en un momento dado se encuentra en un estado considerado como bueno,

malo o regular y tomar medidas preventivas.

A lo largo de nuestra investigación, también exploraremos la existencia

de correlaciones entre estos factores climatológicos y los contaminantes

atmosféricos.

---

  Además,        buscaremos     identificar    patrones       de

---

---

comportamiento temporal en la relación entre estas variables, lo que nos

ayudará a comprender mejor cómo evoluciona la calidad del aire en

función de las condiciones meteorológicas y la presencia de

contaminantes.

**3.2 -- JUSTIFICACIÓN**

La elección de nuestro enfoque se basa principalmente en la hipótesis de

que los dos factores principales que contribuyen a la contaminación del

aire son los factores meteorológicos y la presencia de gases

ambientales. Además, nuestra intención es desarrollar modelos

predictivos que nos permitan tomar medidas preventivas tanto a nivel

ciudadano como desde el ámbito de las autoridades gubernamentales. A

continuación, se enumeran algunas razones clave que respaldan esta

elección:

> **Impacto en la Salud:** La contaminación del aire afecta la salud de

> la población, con riesgos de enfermedades graves.

> **4.1 -- ANÁLISIS FACTORIAL**

> El análisis factorial es una técnica estadística que reduce un

> conjunto de variables al extraer todos sus puntos en común en un

> número menor de factores que pueden considerarse como variables

> latentes \[14\].

> El análisis factorial utiliza varios supuestos:

+-----------------------------------+-----------------------------------+

| > ▪\                              | > La relación lineal de las       |

| > ▪\                              | > variables. Ausencia de          |

| > ▪\                              | > multicolinealidad. Relevancia   |

| > ▪                               | > de las variables.               |

|                                   | >                                 |

|                                   | > La existencia de una verdadera  |

|                                   | > correlación entre factores y    |

|                                   | > variables.                      |

+===================================+===================================+

+-----------------------------------+-----------------------------------+

> **4.2 -- ANÁLISIS DISCRIMINANTE LINEAL**

> El Análisis Discriminante Lineal (LDA) es un método de clasificación

> supervisado que se utiliza cuando se conocen previamente dos o más

> grupos y se desea clasificar nuevas observaciones en uno de estos

> grupos según sus características; se basa en el teorema de Bayes para

> estimar la probabilidad de que una observación, dadas sus

> características, pertenezca a cada uno de los grupos. LDA es una

> opción eficaz cuando se tienen múltiples clases \[15\].

> **5 -- COMPRENSIÓN Y PREPARACIÓN DE LOS DATOS**

> La investigación se basa en una base de datos proporcionada por

> nuestro socio formador SIMA, que contiene registros de magnitudes de

> contaminantes y medidas meteorológicas desde el inicio de 2022 hasta

> la

> ITESM, Ciencia de Datos y Matemáticas

fecha actual. Esta base de datos está compuesta por 15 hojas de Excel,

cada una de las cuales contiene registros de diferentes plantas ubicadas

en el estado de Nuevo León. Para nuestros propósitos de investigación,

nos enfocaremos en los registros de la estación ubicada en la zona

Centro, ya que creemos que es una de las estaciones con registros

"promedios" a comparación de estaciones como Apocada que pueden verse

afectado con factores como el aeropuerto; la base de datos cuenta con un

total de 14,255 registros. Estos registros incluyen principalmente 16

variables, todas las cuales son numéricas, a excepción de la variable

\"fecha\", que indica la fecha y hora en que se realizó cada registro en

la planta.

Entre las variables que encontramos en la base de datos se incluyen

gases contaminantes como el monóxido de carbono (CO), el óxido de

nitrógeno (NO), el dióxido de nitrógeno (NO2), los óxidos de nitrógeno

(NOx), el ozono (O3), las partículas suspendidas PM10 y PM2.5, así como

otras variables relacionadas con condiciones meteorológicas como la

temperatura, la humedad, la radiación solar, la precipitación

atmosférica, la velocidad del viento y la dirección del viento.

Esta base de datos proporciona una valiosa fuente de información para

llevar a cabo nuestra investigación y analizar la calidad del aire y las

condiciones meteorológicas en la zona Centro de Nuevo León durante el

período de estudio.

**5.1 -- ANÁLISIS**

Para profundizar en el análisis de nuestros datos, llevamos a cabo una

exhaustiva limpieza de estos. Inicialmente, optamos por eliminar todos

los registros que contenían valores NA o nulos, ya que representaban una

proporción mínima, equivalente al 5.6% del total de

---

  registros.     Posteriormente,   realizamos     escalas        y

---

---

transformaciones necesarias para asegurar que todas las variables se

midieran en las mismas unidades. Una vez completada la limpieza de

datos, procedimos a calcular medidas estadísticas descriptivas, que

incluyen valores únicos para cada variable, medidas de tendencia central

y medidas de dispersión. Estos resultados se encuentran detalladamente

documentados en los anexos de nuestro trabajo.

Durante el proceso, identificamos que la variable \"lluvia\" tenía solo

dos tipos de datos, por lo que decidimos prescindir de ella y eliminarla

de nuestra base de datos. Por otro lado, la variable \"fecha\" fue

modificada por mes y día para observar patrones a lo largo del tiempo.

Alarcón C, Castro R, Fernández P, Montes J, Orantes A.

> Para enriquecer nuestro análisis, recurrimos a la utilización de

> recursos visuales, principalmente histogramas, que nos permitieron

> visualizar que la mayoría de las variables presentaban una

> distribución sesgada hacia la derecha. También empleamos diagramas de

> caja y bigotes (box plots) para identificar la considerable

> variabilidad en muchas de las variables.

> ![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image3.png){width="3.3333333333333335in"

> height="1.5166655730533682in"}

> **Figura 1:** Histogramas de las variables del conjunto de datos.

> En cuanto al análisis de correlación entre variables, descubrimos que

> las variables meteorológicas mostraban correlaciones entre sí, al

> igual que las variables relacionadas con los gases contaminantes. Sin

> embargo, también

---

  observamos     correlaciones   sorprendentes,   como           la

---

---

> correlación entre el ozono (O3) y la humedad relativa, que no

> esperábamos inicialmente.

> ![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image4.png){width="3.095833333333333in"

> height="2.713888888888889in"}

> **Figura 2:** Matriz de correlación entre las variables.

> A medida que avanzamos en nuestro análisis, reconocemos la importancia

> de realizar pruebas de independencia y detectar posibles problemas de

> colinealidad entre nuestras variables predictoras. Esto nos permitirá

> reducir la dimensionalidad de nuestra matriz de datos y simplificar la

> complejidad del problema. Además, debemos evaluar la relación entre

> nuestras variables dependientes o de interés en la investigación.

> Estos pasos adicionales son cruciales para obtener una comprensión más

> profunda de

ANÁLISIS DE LA CALIDAD DEL AIRE Septiembre de 2023, Monterrey, Nuevo

León Una forma de predecir para prevenir

nuestros datos y respaldar nuestras conclusiones de investigación. En

este proyecto, utilizamos variables latentes como "meteorología",

"contaminantes", "clima" y "tiempo" para diseñar una función de análisis

discriminante. Para hacerlo, seguimos los criterios de decisión de

nuestro socio formador, que se detallan en la siguiente tabla.

![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image5.png){width="3.451388888888889in"

height="1.2027777777777777in"}

> **Figura 7:** Normas de regulación de gases (SIMA, N.L)

Hemos decidido seguir con las 5 clases diferentes, basadas

principalmente en el intervalo de PM10, variable sugerida por el

análisis estadístico que la posiciona como la variable de mayor peso. De

forma que las funciones discriminantes son las que a continuación se

presentan.

**6 -- MODELADO**

En esta etapa, se exponen los procesos clave de nuestros modelos

matemáticos, diseñados con el propósito de abordar nuestras preguntas de

investigación. Nuestra meta es alcanzar los resultados óptimos y

personalizarlos para satisfacer nuestras necesidades específicas.

**6.1** -- **ANÁLISIS FACTORIAL**

Después de realizar un análisis factorial en el contexto de nuestro

proyecto de investigación sobre la calidad del aire, hemos obtenido

resultados significativos que nos permiten comprender mejor la

estructura subyacente de las variables involucradas.

En primer lugar, las pruebas de hipótesis como análisis de Bartlett y

KMO respalda el análisis factorial. Luego utilizando métodos como el

gráfico de la varianza explicada acumulada y de los componentes, lo cual

determinamos que el número total de factores es igual a 4, que juntos

explican un porcentaje de variabilidad del 64% de nuestros datos

originales. Además, cada una de las variables tiene una comunalidad

superior a 0.5 cuando se utiliza el método de componentes principales

con una rotación varimax.

![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image6.png){width="3.3333333333333335in"

height="2.058333333333333in"}

> **Figura 3**: Representación gráfica de la proporción de varianza

> explicada por cada factor de los datos originales. Vemos solo 4 de

> ellos es superior al umbral remarcado.

> Los factores identificados se expresan como combinaciones lineales de

> las cargas con sus respectivas variables originales.

> 𝐹1 = 0.67𝑃𝑀10 + 0.74𝑃𝑀2.5 + 0.77𝑁𝑂 + 0.85𝑁𝑂2\

> 𝐹2 = 0.863𝑂3 − 0.74𝑅𝐻 + 0.7𝑆𝑅 + 0.7𝑇𝑂𝑈𝑇 + 0.72𝑊𝑆𝑅

> 𝐹3 = −0.34𝐶𝑂 + 0.32𝑇𝑂𝑈𝑇 + 0.91𝑀𝑂𝑁𝑇𝐻

> 𝐹4 = 0.589𝐶𝑂 − 0.658𝐷𝐴𝑌 − 0.231𝐻𝑂𝑈𝑅\

> (1) Los factores que se presentan están escritos bajo los pesos más

> representativos, se muestran completos en los anexos.

> Este análisis de factores revela que nuestras variables no se agrupan

> simplemente en dos categorías como se esperaba, sino que se

> distribuyen en cuatro grupos distintos.

![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image7.png){width="3.3333333333333335in"

height="3.270832239720035in"}

> ITESM, Ciencia de Datos y Matemáticas

**Figura 4**: Representación vectorial de los factores. Observe que este

grafico limita la interpretación de estos por cuestiones de

dimensionalidad.

> **Variables Meteorológicas (Factor 1):** Este grupo está compuesto por

> variables como la velocidad del viento, la temperatura y la presión

> atmosférica. Estas variables influyen en la calidad del aire al

> afectar la dispersión de contaminantes, la formación de contaminantes

> secundarios y la estabilidad atmosférica.

> **Contaminantes Atmosféricos (Factor 2):** Incluye variables

> relacionadas con contaminantes atmosféricos como monóxido de carbono,

> monóxido de nitrógeno, dióxido de nitrógeno, partículas PM10 y PM2.5,

> dióxido de azufre, junto con la dirección del viento. Este grupo

> representa la presencia y distribución de contaminantes en el aire,

> así como su relación con la dirección del viento.

> **Factores Climatológicos (Factor 3):** Este grupo incluye humedad

> relativa y variación solar, variables cruciales para medir la calidad

> del aire al afectar directamente en la formación de partículas,

> absorción de contaminantes, confort humano, temperatura y reacciones

> fotoquímicas en la atmósfera.

> **Tiempo (Factor 4):** Este factor mide cómo se

---

  comporta       la             contaminación   en             diferentes

---

---

> temporadas y horas del día por medio de las variables mes y día.

---

  Cabe        mencionar   que         estos       grupos      mencionados

---

---

anteriormente son producto de una representación visual de F1 y F2, que

entre estos dos se explica alrededor del 47.6% de los datos originales.

Esto significa que, aunque si nos da una idea general de como se

comportan las variables originales, no se puede decir que es una imagen

completa de sus relaciones en la matriz de datos originales (perdida de

información).

Para poder visualizar el comportamiento de nuestra variable predictora

en los factores obtenidos del análisis, nos vemos a la tarea de obtener

la puntuación de cada observación-de los datos originales- en las nuevas

dimensiones. Esto se realiza con la combinación lineal de cada factor

respecto a las variables originales, como se ilustro en las ecuaciones

(1). En otras palabras, se multiplica el vector de observaciones de cada

variable con su respectivo coeficiente del factor correspondiente.

Alarcón C, Castro R, Fernández P, Montes J, Orantes A.

> ![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image8.png){width="2.8472222222222223in"

> height="3.308333333333333in"}

> **Figura 5:** Tabla de combinación lineal de los factores respecto a

> las variables predictoras

> Una vez obtenidas los puntos en cada dimensión, podemos elegir cada

> par de factores para ver su relación con respecto a la variable

> dependiente creada por nosotros. En la figura 6

> se observa su comportamiento.

> ![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image9.png){width="3.3333333333333335in"

> height="1.6083333333333334in"}

> **Figura 6:** Representación gráfica de la distribución de predicción

> de la calidad con F1 y F2.

> Precisamente, se observa una correlación positiva "aparente" entre

> ambos factores, lo cual puede ocurrir cuando dos variables muestran

> relación aparente debido a una coincidencia temporal o a la influencia

> de una tercera variable no considerada en el análisis. Lo cual tiene

> sentido debido al porcentaje de variabilidad explicada entre los

> primeros dos factores. Del mismo modo, vemos que entre más aumentan

> las puntuaciones de ambos factores, la calidad del aire empeora. Dicho

> lo anterior, podemos graficar cada par de factores como se muestra en

> la figura 7.

ANÁLISIS DE LA CALIDAD DEL AIRE Septiembre de 2023, Monterrey, Nuevo

León Una forma de predecir para prevenir

![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image10.png){width="3.3555555555555556in"

height="1.9041666666666666in"}

**Figura 7:** Representación gráfica de la distribución de predicción de

todos los factores.

Con las siguientes visualizaciones, podemos obtener algunas

interpretaciones de valor para nuestra pregunta objetivo:

> **Relación entre PM10 y PM2.5 con F1:** Entre más incrementan las

> concentraciones de PM10 y PM2.5, los valores de F1 aumentan. Como

> estas variables influyen mucho en el primer factor, podemos inferir

> que la concentración de las mismas partículas influye en la calidad

> del aire.

> **Relación entre RH con F2:** Entre más incrementan los niveles de RH

> (humedad relativa), los valores de F2 disminuyen. Como esta variables

> influye significativamente en el segundo factor, se infiere que sus

> niveles mejoran a la calidad del aire.

> **Relación entre el transcurso del mes y F3:** Se observa una relación

> proporcional entre el numero del mes y el tercer componente.

> **Relación entre la hora y F4:** Se observo que la hora (0:00-24:00

> hrs) tenía una inversamente proporcional con los valores de F4. Se

> puede inferir que entre mas tarde se toma la observación, mejor es su

> calidad del aire.

Dicho lo anterior, se tiene que tener en cuenta la proporción de

varianza explicada por los primeros 4 componentes seleccionados en el

análisis (63.5%), ya que nos indica que mucha información se perdió en

el proceso. Esto nos limita en saber la relación completa entre las

mismas variables; no obstante, como sabemos que F1 y F2 explican gran

parte de los datos originales, podemos afirmar que las variables PM10,

PM2.5 y RH son grandes indicadores para determinar la calidad del aire.

> al abordar nuestro problema. Además, son esenciales para mejorar la

> calidad de nuestros modelos de predicción de la calidad del aire en

> momentos específicos. Esto reduce los problemas de selección de

> variables y el tiempo computacional necesario, al tiempo que aumenta

> la confiabilidad de nuestros modelos. Esto nos permite informar de

> manera más precisa a la sociedad y tomar medidas preventivas

> efectivas.

> 𝐿𝐷1 = 0.0259𝑓1 + 0.0169𝑓2 − 0.0466𝑓3 + 0.0022𝑓4

> 𝐿𝐷2 = 0.0593𝑓1 − 0.0522𝑓2 + 0.0119𝑓3 − 0.1021𝑓4

> 𝐿𝐷3 = −0.0199𝑓1 − 0.0133𝑓2 − 0.1159𝑓3 + 0.0511𝑓4

> 𝐿𝐷4 = 0.0726𝑓1 + 0.0307𝑓2 + 0.1892𝑓3 − 0.1189𝑓4

\(2\) Funciones discriminantes del modelo.

> Se realizaron cálculos previos de probabilidad para cada una de las

> clases utilizando el conjunto de datos. En estos cálculos, se

> determinó que la clase predominante corresponde a la \"Buena\" y

> "Aceptable" de la calidad del aire. Esta información se refleja de

> manera gráfica en los niveles de proporción de cada clase.

> ![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image11.png){width="3.3333333333333335in"

> height="2.072221128608924in"}

> **Figura 8:** Representación gráfica de la separación de clases de la

> función discriminante 1.

> En la figura 8, se puede observar que tanto se separan las clases con

> la primera función discriminante-la cual tiene un porcentaje de traza

> del 99.67%, lo que indica que es la mas significativa para hacer la

> clasificación multiclase dentro de las calidades del aire.

Ca **7 -- EVALUACIÓN**

**6.2** -- **ANÁLISIS DISCRIMINANTE**\

Haber identificado previamente estos factores nos permiten entender cómo

se relacionan las variables entre sí

> Los modelos mencionados en nuestra investigación proporcionan

> información valiosa. Descubrimos que el conjunto de datos original se

> puede expresar de manera

> ITESM, Ciencia de Datos y Matemáticas

efectiva en términos de cuatro factores o variables latentes, lo que

simplifica considerablemente nuestro trabajo de análisis. Esto nos

permite reducir la complejidad de los datos a un conjunto manejable de

dimensiones.

En el análisis factorial, las cargas obtenidas para cada factor son

sólidas, lo que indica una representación efectiva de la estructura

subyacente de los datos. Con estos cuatro factores, logramos capturar el

65.3% de la variabilidad en nuestros datos, lo que demuestra la

capacidad de este enfoque para resumir la información de manera

significativa, es importante mencionar que los resultados de prueba de

hipótesis de la prueba de Bartlett y el coeficiente KMO nos llevaron a

realizar este prueba, con un valor p \< 0 y un coeficiente de 0.65

respectivamente, y que después se realizó un calculo de correlaciones

entre los cuatro factores donde todos resultaron debajo de 0.05.

> Por otro lado, el análisis discriminante resultó ser

Alarcón C, Castro R, Fernández P, Montes J, Orantes A.

> centró en el Análisis Factorial y el Análisis Discriminante, con el

> propósito de profundizar en la comprensión de cómo los diferentes

> factores están interconectados y cómo impactan en la calidad del aire

> en nuestra región.

> **8.1 -- HALLAZGOS DEL ANÁLISIS FACTORIAL**

> Identificamos con éxito cuatro factores latentes clave que

> simplificaron la complejidad de nuestros datos. Estos factores

> proporcionaron una comprensión más profunda de las relaciones entre

> las variables originales. Destacamos que el factor de gases

> contaminantes tiene un peso significativo en la determinación de la

> calidad del aire. Esto resalta la importancia de las acciones humanas,

> como la emisión de CO2 de los vehículos, en la intensidad de la

> contaminación atmosférica. Además, observamos que factores externos,

> como la estación del año, el clima y la dirección del viento, tienen

> un impacto comparativamente menor en nuestras mediciones.

+-----------+-----------+-----------+-----------+-----------+-----------+

| una buena | **8.2**   | --        | **HA      | **DEL**   | > **A     |

| opción    |           |           | LLAZGOS** |           | NÁLISIS** |

| para      |           |           |           |           |           |

| predecir  |           |           |           |           |           |

| a qué     |           |           |           |           |           |

| grupo de  |           |           |           |           |           |

| los cinco |           |           |           |           |           |

| cae       |           |           |           |           |           |

+===========+===========+===========+===========+===========+===========+

| un        |           |           |           |           |           |

| de        |           |           |           |           |           |

| terminado |           |           |           |           |           |

| momento   |           |           |           |           |           |

| basado en |           |           |           |           |           |

| estos     |           |           |           |           |           |

| factores  |           |           |           |           |           |

| latentes. |           |           |           |           |           |

+-----------+-----------+-----------+-----------+-----------+-----------+

|           | >         |           |           |           |           |

|           |  **DISCRI |           |           |           |           |

|           | MINANTE** |           |           |           |           |

+-----------+-----------+-----------+-----------+-----------+-----------+

| El modelo |           |           |           |           |           |

| disc      |           |           |           |           |           |

| riminante |           |           |           |           |           |

| ha        |           |           |           |           |           |

| d         |           |           |           |           |           |

| emostrado |           |           |           |           |           |

| un        |           |           |           |           |           |

| sign      |           |           |           |           |           |

| ificativo |           |           |           |           |           |

+-----------+-----------+-----------+-----------+-----------+-----------+

nivel de eficacia, con una precisión del 70% en la clasificación de las

clases. Este valor es notablemente bueno, especialmente en comparación

con nuestros primeros intentos utilizando selección de variables

iniciales basadas en correlaciones. A continuación, se encuentra la

matriz de confusión obtenida para nuestras predicciones.

> ![](vertopal_f39891c6ca9b4f089606e9265b15e24a/media/image12.png){width="2.573611111111111in"

> height="0.9722222222222222in"}

> **Figura 9:** Matriz de confusión del modelo discriminante.

> Es importante tener en cuenta que, en nuestro

---

  contexto       de             investigación,   enfrentamos    desafíos

---

---

significativos. La naturaleza irregular del tiempo, que varía debido a

diversos factores, introduce una gran alteración en nuestros datos. Esta

variabilidad puede dificultar la predicción precisa de la calidad del

aire. Además, la interpretación de gráficos de cuarta dimensión para

comprender mejor fenómenos como el análisis de vectores puede ser

compleja y limitante.

**8 -- DESPLIEGUE DE RESULTADOS**

En esta sección del informe, presentamos los resultados finales de

nuestro estudio sobre la calidad del aire en el centro de Monterrey,

Nuevo León. Nuestro enfoque se

> El Análisis Discriminante demostró ser eficaz al alcanzar una

> precisión del 70% en la clasificación de las categorías de calidad del

> aire. Esto indica que nuestro modelo tiene un alto potencial para

> respaldar la toma de decisiones y la implementación de medidas

> preventivas.

> **8.3** -- **RELEVANCIA SOCIAL Y AMBIENTAL:**

> Es crucial destacar que la calidad del aire es un factor directamente

> relacionado con la salud y el bienestar de la

---

  población.   Nuestros    resultados   contribuyen   a           la

---

---

> comprensión de cómo los factores subyacentes identificados pueden

> guiar la adopción de medidas proactivas para mantener un aire

> saludable y reducir riesgos para la salud pública.

> En un contexto global, otros países han implementado tecnologías

> avanzadas, como sistemas de monitoreo en tiempo real y modelos

> predictivos, para evaluar y predecir la calidad del aire. Estos

> enfoques han tenido éxito en la planificación y ejecución de

> estrategias para mejorar la calidad del aire y proteger la salud de la

> población. Creemos que nuestro modelo de predicción tiene el potencial

> de seguir el mismo camino y contribuir significativamente a la toma de

> decisiones informadas en nuestra región, especialmente en el estado de

> Nuevo León, donde se requieren acciones efectivas para abordar los

> desafíos ambientales.

> **9 -- CONCLUSIÓN**

ANÁLISIS DE LA CALIDAD DEL AIRE Septiembre de 2023, Monterrey, Nuevo

León Una forma de predecir para prevenir

En este informe, hemos llevado a cabo una exhaustiva investigación sobre

la calidad del aire en el centro de Monterrey, Nuevo León, un problema

de gran relevancia global debido a sus impactos en la salud humana, el

medio ambiente y el cambio climático. A través del uso de técnicas

estadísticas avanzadas como el Análisis Factorial y el Análisis

Discriminante, nuestro objetivo principal ha sido analizar en

profundidad cómo diversos factores, como los

---

  contaminantes   atmosféricos   y              las            condiciones

---

---

meteorológicas, están interconectados y ejercen un impacto significativo

en la calidad del aire en esta región.

En el proceso de análisis factorial, identificamos con éxito cuatro

factores latentes clave que simplificaron la complejidad de los datos y

proporcionaron una comprensión más profunda de la estructura subyacente

de las variables. Estos factores revelaron que los gases contaminantes

tienen un peso significativo en la determinación de la calidad del aire,

destacando la influencia de las acciones humanas, como la emisión de

CO2, la influencia de la humedad relativa para el nivel de

contaminación, la influencia de la hora y el mes en la concentración de

contaminantes, entre otros más.

Por otro lado, el Análisis Discriminante demostró ser una herramienta

eficaz para predecir la calidad del aire en diferentes categorías,

logrando una precisión del 70% en la clasificación de las clases. Esto

sugiere que nuestro modelo tiene un alto potencial para respaldar la

toma de decisiones y la implementación de medidas preventivas, lo que es

esencial para la protección de la salud pública.

Es importante destacar que la calidad del aire tiene un impacto directo

en la salud y el bienestar de la población, y nuestros resultados

contribuyen a una comprensión más profunda de cómo los factores

subyacentes pueden guiar la adopción de medidas proactivas para mantener

un aire saludable y reducir los riesgos para la salud pública.

En un contexto global, observamos que otros países han implementado

tecnologías avanzadas para evaluar y predecir la calidad del aire, lo

que ha resultado efectivo en la planificación de estrategias para

mejorar la calidad del aire y proteger la salud pública. Consideramos

que nuestro modelo de predicción tiene el potencial de contribuir de

manera similar a la toma de decisiones informadas en nuestra región y

abordar el problema de la contaminación del aire en Nuevo León.

**10 -- ANEXOS**

**Documento RMD:**\

https://drive.google.com/file/d/1zV9zWnIZ3WwSDu5Dnd5L0W

ApnBzw7GlO/view?usp=sharing

> **Base de Datos y Diccionario:**\

> https://docs.google.com/spreadsheets/d/1T_qUxVIZoL-\

> 2dbgm7wNcmVjZJzlP0KUH/edit?usp=drive_link&ouid=106200

> 824084043965507&rtpof=true&sd=true

> Esta base de datos es privada, por lo que deberá solicitarse su

> acceso.

> **11 -- REFERENCIAS BIBLIOGRÁFICAS**

> \[1\] OMS. (2023). El mundo entero debe unirse para combatir la\

> contaminación atmosférica, que mata a 7 millones de personas al año.

> OMS.

> Recuperado el 08 de septiembre de 2023 de:\

> [https://mexico.un.org/es/245119-el-mundo-entero-debe-unirse-]{.underline}\

> [paracombatir-la-contaminaci%C3%B3n-atmosf%C3%A9rica-que-mata-7-]{.underline}

> [millones]{.underline}

> \[2\] National Weather Service. (s.f.). Why Air Quality Is Important.

> National Weather Service. Recuperado el 08 de septiembre de 2023 de:

> \[3\] Linares, C. (2008). ¿Qué son las PM2,5 y cómo afectan a nuestra

> salud?. Ecoloxistas en acción. Recuperado el 08 de septiembre de 2023

> de:

> \[4\] Environmental Protection Agency. (2023). What is \"good\" vs.

> \"bad\" ozone?. Environmental Protection Agency. Recuperado el 08 de

> septiembre de 2023 de:

> \[5\] Environmental Protection Agency. (2023). What is SO2 and how

> does it get in the air?. Environmental Protection Agency. Recuperado

> el 08 de septiembre de 2023 de:

> \[6\] Bliss, L. (2016). An American History of Lead Poisoning. The

> Atlantic. Recuperado el 08 de septiembre de 2023 de:

> \[7\] Milenio Digital. (2022). ¡Entérate! Así se mide la calidad del

> aire. Milenio Digital. Recuperado el 08 de septiembre de 2023 de:

> \[8\] Fernandez, L. (2020). Qué es y cómo se mide la calidad del aire.

> Ecología verde. Recuperado el 08 de septiembre de 2023 de:

> \[9\] Programa de las Naciones Unidas para el Medio Ambiente. (2022).

> ¿

> Cómo se mide la calidad del aire?. Programa de las Naciones Unidas

> para el Medio Ambiente. Recuperado el 08 de septiembre de 2023 de:

> \[10\] Instituto nacional de ecología. (s.f.). Manual 1.

> \[11\] Naciones Unidas. (s.f.). Apoyar el desarrollo sostenible y la

> acción climática. Naciones Unidas. Recuperado el 08 de septiembre de

> 2023 de:

> ITESM, Ciencia de Datos y Matemáticas Alarcón C, Castro R, Fernández

> P, Montes J, Orantes A.

\[12\] Gobierno de México. (2023). Programas de Gestión para Mejorar la

Calidad del Aire ProAire. Gobierno de México. Recuperado el 08 de

septiembre de 2023 de:

\[13\] NL Medio Ambiente. (s.f.). Bienvenido. NL Medio Ambiente.

Recuperado el 08 de septiembre de 2023 de

\[14\] TIBCO. (2023). ¿Qué es el análisis factorial?. TIBCO. Recuperado

el

07 de septiembre de 2023. de:

\[15\] Amat Rodrigo, J. (2016). Análisis discriminante lineal (LDA) y

análisis discriminante cuadrático (QDA). Ciencia de Datos. Recuperado el

07 de septiembre de 2023 de:
