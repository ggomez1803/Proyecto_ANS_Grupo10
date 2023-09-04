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
5. Propuesta Metodológica
6. [Bibliografia](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/blob/main/README.md#bibliografia)
7. Anexos y Archivos

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
Ver documento adjunto para mayor detalle de la EDA (Exploración de Datos y analisis preliminar)

## Propuesta Metodológica
![image](https://github.com/ggomez1803/Proyecto_ANS_Grupo10/assets/84612583/342f60d3-2ab6-495d-af4f-32f5e6be5623)


## Bibliografia

https://bloomerang.co/blog/donor-segmentation/
	
https://medium.com/zohero/case-study-using-monthly-giving-to-increase-donors-lifetime-value-41140228a3fc

Nelson, K., Schlüter, A., & Vance, C. (2017). Distributional preferences and donation behavior among marine resource users in Wakatobi, Indonesia. Ocean & Coastal Management. https://doi.org/10.1016/J.OCECOAMAN.2017.09.003.
 
Müller, S., Fries, A., & Gedenk, K. (2014). How much to give? — The effect of donation size on tactical and strategic success in cause-related marketing. International Journal of Research in Marketing, 31, 178-191. https://doi.org/10.1016/J.IJRESMAR.2013.09.005.
 
Durango-Cohen, P., Durango-Cohen, E., & Torres, R. (2013). A Bernoulli-Gaussian mixture model of donation likelihood and monetary value: An application to alumni segmentation in a university setting. Comput. Ind. Eng., 66, 1085-1095. https://doi.org/10.1016/j.cie.2013.08.007.
 
Zhu, L., He, Y., Chen, Q., & Hu, M. (2017). It's the thought that counts: The effects of construal level priming and donation proximity on consumer response to donation framing. Journal of Business Research, 76, 44-51. https://doi.org/10.1016/J.JBUSRES.2017.03.007.
 
Rocha, A., Campos, D., Farina, M., Pacini, G., Girotto, M., & Hilbig, A. (2017). Using body donor demographics to assist the implementation of donation programs in Brazil. Anatomical Sciences Education, 10. https://doi.org/10.1002/ase.1687.
