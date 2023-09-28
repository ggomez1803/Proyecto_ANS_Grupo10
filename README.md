# Proyecto Aprendizaje No Supervisado - Grupo 10

Integrantes:
Gabriel Gomez,
Daniel Rozo,
Yolanda Franco

## Tabla de Contenido - Propuesta Inicial Proyecto

1. [Resumen](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/README.md#resumen)
2. [Introducción](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/README.md#introducci%C3%B3n)
3. [Revisión Preliminar de la Literatura](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/README.md#revisi%C3%B3n-preliminar-de-la-literatura)
4. [Descripción de los datos](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/README.md#descripci%C3%B3n-de-los-datos)
5. [Propuesta Metodológica](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/README.md#propuesta-metodol%C3%B3gica)
6. [Resultados y Discusión](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/tree/main#resultados-y-discusi%C3%B3n)
7. [Posibles acciones](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/tree/main#posibles-acciones)
8. [Conclusiones](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/tree/main#conclusi%C3%B3n)
9. [Bibliografia](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/README.md#bibliografia)
10. [Anexos y Archivos](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/README.md#anexos-y-archivos)

### Resumen
En este proyecto, se busca desarrollar un modelo de segmentación de donantes para una ONG que ayude a alinear correctamente las estrategias diseñadas dentro de la organización para tener un mejor aprovechamiento de los recursos y llegar a ser costos eficientes en todos los esfuerzos que se ejecutan.

Para desarrollar el modelo de segmentación, primero se debe calcular el “Customer Lifetime Value” o “Donor Lifetime Value” (DLTV) para lograr tener una segmentación basada en el retorno o valor que genera cada uno de los donantes. Posteriormente, según su bajo, medio o alto valor, lo que se quiere es identificar las características principales que representan cada segmento además de su valor con el fin de proponerle a la organización un perfil de donante en el que se deberían enfocar en buscar. Finalmente, se procede a cruzar cada uno de estos segmentos identificados contra la variable de churn y alinear correctamente las estrategias que se ejecutan hoy en día para buscar ser más costos eficientes.

### Introducción
En el núcleo de nuestra misión de transformar vidas, se encuentra Protección Infantil SOS (PI), una ONG dedicada a brindar un hogar con futuro a niños y jóvenes separados de sus familias. Sin embargo, los tiempos cambian, y esta organización enfrenta desafíos cruciales: cambios en el comportamiento de los donantes, la búsqueda de la autosostenibilidad y la necesidad de alinear estrategias. En este proyecto, exploraremos cómo la tecnología y el aprendizaje automático pueden ayudar a Protección Infantil a definir los nuevos perfiles de donantes y personalizar estrategias para retener a aquellos que hacen posible su noble labor.

PI busca responder la siguiente pregunta clave: "¿Cuáles son los nuevos perfiles de donantes teniendo en cuenta las variables externas e internas que afectan su comportamiento a partir de técnicas de Machine Learning?" Esta pregunta pertenece al área del aprendizaje no supervisado, ya que no se busca predecir una variable específica, sino descubrir patrones y segmentar a los donantes en grupos basados en su comportamiento y características. El objetivo es personalizar estrategias de captación y fidelización para mantener el apoyo vital de los donantes y garantizar el cumplimiento de la misión de PI en un entorno cambiante y desafiante.

## Revisión Preliminar de la Literatura

¿Por qué personalizar estas estrategias para cada donante? Cada donante tiene su propia experiencia, y es importante reconocer en qué momento de su camino se encuentra para comunicarse con él adecuadamente y lograr retenerlo ya que se ha demostrado que los donantes recurrentes pueden llegar a generar hasta 3 veces más valor que donantes ocasionales. Esto evidencia una clara relación entre una correcta segmentación para aumentar la tasa de retención.

La donación a causas benéficas es una práctica ampliamente valorada en la sociedad contemporánea. La efectividad de las estrategias de recaudación de fondos y el impacto de las donaciones pueden variar significativamente según cómo se segmente a la audiencia de donantes (Nelson, Schlüter, & Vance, 2017). La investigación de Müller, Fries y Gedenk (2014) destaca la importancia del tamaño de la donación en el contexto del marketing relacionado con causas (CM) y cómo puede influir tanto en la elección de marca como en la imagen de marca. Sus resultados sugieren que el tamaño de la donación puede influir en la elección de los consumidores y en la percepción de la marca. Este estudio subraya la importancia de seleccionar el tamaño de la donación adecuado al considerar la estrategia de recaudación de fondos, lo que implica una forma de segmentación basada en el tamaño de la donación. En un entorno universitario, Durango-Cohen, Durango-Cohen y Torres (2013) proponen un modelo estadístico de mezcla Bernoulli-Gaussiana para segmentar a los donantes. Esto resalta la relevancia de la segmentación para adaptar estrategias de recaudación de fondos. El estudio de Zhu, He y Chen (2017) resalta cómo la presencia de otros consumidores y la presentación de la donación pueden influir en la percepción de la marca y la intención de donación de los consumidores, subrayando la importancia de considerar el contexto y el tipo de apelación en la solicitud de donaciones.
 
Un estudio realizado por Oxley da Rocha et al. (2017) se centró en el perfil demográfico de los solicitantes al Programa de Donación de Cuerpos (BDP) en la Universidad Federal de Ciencias de la Salud de Porto Alegre, Brasil. Los resultados revelaron que el solicitante típico en Brasil es una mujer blanca de más de 60 años, soltera, afiliada a un grupo religioso, de clase media y con educación secundaria y/o título universitario. La motivación principal de los donantes fue un gesto altruista, con el deseo de contribuir a la sociedad y la ciencia. Este estudio resalta la importancia de comprender el perfil demográfico de los donantes potenciales y sugiere que esta comprensión puede ayudar en la dirección de campañas de información sobre la donación de cuerpos hacia audiencias específicas. Aunque se centra en donaciones de cuerpos, esta idea de segmentación basada en características demográficas puede aplicarse a otras formas de donaciones benéficas. Además, destaca la necesidad de considerar la cultura y el contexto regional al diseñar estrategias de recaudación de fondos, ya que las características de los donantes pueden variar según la ubicación geográfica y las costumbres locales. Estos hallazgos tienen importantes implicaciones para las organizaciones benéficas y las empresas que buscan maximizar su impacto a través de estrategias efectivas de recaudación de fondos y marketing relacionado con causas.

## Descripción de los datos
Ver cuaderno de jupyter notebook adjunto para mayor detalle del EDA.
https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/Exploracion_de_Datos_.ipynb

## Propuesta Metodológica
Dentro de un taller de ideación que se realizó con PI, se resaltaron varios “dolores” donde se priorizaron y se buscó llegar a la pregunta de negocio que se buscará resolver por medio de tecnicas de Aprendizaje no supervisado basandonos especialmente en siguiente indicador.
![image](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/assets/84612583/7650cc7d-2a4b-4ff3-abbd-3e14c60b1011)

Este trabajo tiene como objetivo la construcción de perfiles de donantes a través de indicadores internos y externos. En este contexto, resulta relevante la estimación en valor presente de la donación promedio anual.
Para encontrar el mejor modelo que haga sentido al negocio se probaron diferentes modelos teniendo en cuenta variables numéricas y categóricas. Estos modelos fueron los siguientes:

·	Matriz de gower para tener en cuenta variables categóricas y posteriormente un cluster jerárquico 
·	Segmentación con k-prototypes 
·	PCA para reducción de dimensionalidad y K-means 
·	K-means con diferentes grupos de variables

## Resultados y Discusión

#### Clúster Jerárquico

Este modelo se descartó porqué el modelo no arrojó una segmentación balanceada entre los grupos de donantes y los resultados obtenidos no mostraron un perfil claro en los clústeres que permitiera definir alguna estrategia por segmento. 
 
![image](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/assets/84612583/0f637724-a9ea-4deb-bc09-d1257cc7dbe8)

#### Segmentación con k-prototypes
En este modelo se intentaron varias combinaciones de variables categóricas como la edad, estado civil y género, pero los resultados arrojaron que ninguna de estas variables es representativa para caracterizar los segmentos, pues solo el valor del donante (DLTV) es el que predominaba en la segmentación como podemos ver en las siguientes imágenes.

![image](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/assets/84612583/8f936a7b-2a5a-4c5e-86f5-e1173c5cf5e4)

#### PCA para reducción de dimensionalidad y K-means
En el análisis de componentes principales, inicialmente se usaron 6 variables para reducirlas a tres componentes principales, con el fin de ayudar a mejorar la interpretabilidad de los datos, estos tres componentes explicaron el 71% de la varianza. Sin embargo, dentro de las variables utilizadas se encontraban el promedio de cuotas pagadas y no pagadas anuales donde se evidenciaron datos sin sentido en análisis previos.

![image](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/assets/84612583/28bb4214-d041-4650-9e51-ab1cc94a7bf0)


Se hizo un segundo intento con cuatro variables reduciéndolas a tres componentes y explicando el 93% de la varianza, pero los componentes dos y tres eran una combinación lineal de las mismas variables, por lo que se procede a reducirlo a dos componentes principales, explicando el 69% de la varianza. Dentro de este último modelo la variable de canales de donación no parece representar o ser parte de algún perfil especifico dentro de los segmentos, por lo que se decidió quitarla y usar solamente k-means.


![image](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/assets/84612583/2c635088-cb31-4d04-82e4-94689faa9b3b)

#### K-means con diferentes grupos de variables
En este modelo se analizaron la edad, la probabilidad de fuga y el valor del donante. Bajo el coeficiente de silhouette se debía segmentar en tres clústeres, sin embargo, se encontró que en la dimensión de la edad hay una parte donde no se discrimina en términos del valor del donante ni la probabilidad de fuga, por lo que no hace sentido estratégico asignar estrategias de fidelización sin tener en cuenta el presupuesto y el valor que generan los donantes. Dado lo anterior, se elimina del modelo la variable de edad y se calcula nuevamente el coeficiente de silhouette, obteniendo que se debe segmentar en cuatro clústeres con las dos variables restantes.

![image](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/assets/84612583/411d0baf-caec-4e92-812f-fbb1b02fa274)

Los cuatro segmentos obtenidos son:
1.	Segmento en fuga: donantes con bajo valor y alta probabilidad de fuga (Morado)
2.	Segmento potencial: donantes con medio-bajo valor y medio-bajo probabilidad de fuga (Azul)
3.	Segmento en crecimiento: donantes de medio valor y baja probabilidad de fuga (Amarillo)
4.	Segmento estrella: donantes de alto valor y baja probabilidad de fuga (Verde)

## Posibles acciones

Aprovechando la interpretabilidad de esta segmentación, se pueden realizar recomendaciones coherentes sobre qué estrategias enfocar en cada grupo de donantes de la siguiente manera: 

Segmento estrella (Verde): Para estos donantes se pueden dirigir las estrategias más costosas con tal de seguir fidelizándolos tales como el programa de puntos y el club de beneficios 

Segmento en crecimiento (Amarillo): Se puede crear comunicaciones donde se muestre la labor realizada con las donaciones y exaltar su importancia para generar un estado aspiracional y filantrópico para que estos donantes lleguen a hacer parte del segmento de mayor valor 

Segmento potencial (Azul): Se recomienda promover las donaciones ya sea llamando a buscar un incremento de donación o crear nuevos canales para que donen

Segmento en fuga (Morado): Se debe realizar estrategias de concientización y crear sentido de urgencia en la problemática para evitar que dejen de donar.  

## Conclusión
•	Las bases de datos se han convertido en elementos imprescindibles en la estructura de las empresas ya que estas ayudan a tener una propuesta de valor tanto en el manejo interno como externo de la información. Después de procesar las bases de datos suministradas por PI, llegamos a la conclusión de que la información podría ser recolectada a través de medios digitales, esto, con el fin de evitar errores, faltantes, información sin sentido que hace que se pierda la confiabilidad de los datos con los que cuenta la organización.

•	Con el fin de ofrecer una visión adecuada a la organización que busca alinear las estrategias internas para tener un mejor aprovechamiento de los recursos y llegar a ser costo-eficientes y cumplir con su misión; se probaron varios modelos de aprendizaje no supervisado, en los cuales metodológicamente se iban descartando las variables que no aportaban información relevante para la segmentación de donantes. 

Finalmente, el modelo elegido fue K-means con diferentes grupos de variables, en el que se logró segmentar a los donantes en cuatro grupos: segmento estrella, segmento en crecimiento, segmento potencial y segmento en fuga; se eligió este modelo ya que es el que más sentido en términos de estrategia e interpretación, pueden ayudar a orientar a Proyección Infantil en la adecuada toma de decisiones encaminada a fidelizar de forma más personalizada a sus donantes para que puedan seguir desarrollando su labor social de manera eficiente.

•	Los algoritmos de aprendizaje no supervisado que se implementaron en este proyecto y que se vieron a lo largo del curso, nos llevan a concluir que son fundamentales para no sesgar la segmentación de grupos, lo que sí sucede cuando se utilizan otras metodologías o se segmenta con rangos basados en la experiencia. Estas metodologías basadas en experiencia pueden no garantizar una toma adecuada de decisiones debido a este sesgo.


## Bibliografia

https://bloomerang.co/blog/donor-segmentation/
	
https://medium.com/zohero/case-study-using-monthly-giving-to-increase-donors-lifetime-value-41140228a3fc

Nelson, K., Schlüter, A., & Vance, C. (2017). Distributional preferences and donation behavior among marine resource users in Wakatobi, Indonesia. Ocean & Coastal Management. https://doi.org/10.1016/J.OCECOAMAN.2017.09.003.
 
Müller, S., Fries, A., & Gedenk, K. (2014). How much to give? — The effect of donation size on tactical and strategic success in cause-related marketing. International Journal of Research in Marketing, 31, 178-191. https://doi.org/10.1016/J.IJRESMAR.2013.09.005.
 
Durango-Cohen, P., Durango-Cohen, E., & Torres, R. (2013). A Bernoulli-Gaussian mixture model of donation likelihood and monetary value: An application to alumni segmentation in a university setting. Comput. Ind. Eng., 66, 1085-1095. https://doi.org/10.1016/j.cie.2013.08.007.
 
Zhu, L., He, Y., Chen, Q., & Hu, M. (2017). It's the thought that counts: The effects of construal level priming and donation proximity on consumer response to donation framing. Journal of Business Research, 76, 44-51. https://doi.org/10.1016/J.JBUSRES.2017.03.007.
 
Rocha, A., Campos, D., Farina, M., Pacini, G., Girotto, M., & Hilbig, A. (2017). Using body donor demographics to assist the implementation of donation programs in Brazil. Anatomical Sciences Education, 10. https://doi.org/10.1002/ase.1687.

## Anexos y Archivos
Ver Archivos del Cliente en la siguiente [carpeta](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/tree/main/Archivos_Cliente)

En esta carpeta podran encontrar lo siguiente que es la base inicial de datos con la que se va a trabajar el proyecto:

- Base cuentas
- Base Donantes = Base de personas naturales donantes para PI
- Transacciones Juridicos
