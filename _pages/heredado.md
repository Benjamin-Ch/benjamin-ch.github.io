## P5 - ¿Cómo cambia el gasto promedio en copagos a medida que los beneficiarios envejecen?

Es sabido que a medida que uno envejece suele ir con mayor frecuencia al medico y por implicancia sus gastos medicos deben aumentar, pero la pregunta es... Que tanto aumentan estos gastos, existe un punto de quiebre o es gradual?.  


**Elección de variables**  
Como buscamos medir los gastos medicos promedio a medida que una persona envejece, pero tomando en cuenta que no tenemos el historial medico completo de una persona (Lo ideal) usaremos:
1. La "EDAD_TRAMO", puesto que analizaremos un promedio en gastos, para todo el tramo edad del año 2023.
2. El "MONTO_COPAGO" para conocer el monto a pagar por cada prestacion.  
3. Opcional: El "SEXO" para especificar el analisis, pero podria ser cualquiera; "TRAMO_FONASA", "REGION_EMISION", "MES_EMISION", etc...

**Distribución de los datos**  
En primera instancia, veremos la distribución de los datos por tramo de edad.

![Gráfico de distribución de datos por edad](assets/images/p5_distribucion_datos)

Observando la distribucion vemos que estos forman una campana de Gauss. Esto significa que los valores centrales concentran la mayor cantidad de datos, mientras que los valores extremos tienen menos ocurrencias, por lo tanto y aportado a la pregunta Aportando *¿Cómo cambia el gasto promedio en copagos a medida que los beneficiarios envejecen?*, en si, las personas suelen ir con mayor frecuencia a realizar consultas medicas u otras prestaciones. Ahora toca saber el valor de estas.  

He de añadir.  
Esto ocasiona un sesgo de la distribución, puede tener implicaciones para la posible creacion de un modelo predictivo. Al haber menos datos en las colas de la distribución, el modelo pueden tener dificultades para aprender patrones robustos en estas regiones, a tomar en cuenta.  
En concreto:  
- Infantes de "0 a 2 años" tiene mayor ocurrencia que su edad posterior "3 a 4 años", evidenciandose en mayor prevencion en recien nacidos y uso de consultas mas especificas a dicha edad.
- Entre los "25 a 29 años" y "65 a 69" años la ocurrencia es muy similar.
- A partir de los "70 a 79 años" la ocurrencia empieza a bajar, probablemente por la menor tasa de personas que viven mas alla de 70 años.  

![Gráfico de promedio de copagos por edad](assets/images/p5_promedio_copagos_por_edad)

**Analisis grafico**  
Como era de esperar, el promedio del monto de copago aumenta a medida que se incrementa la edad. En concreto, a partir de los 15-19 años se observa un aumento en el gasto medio, probablemente debido al incremento en el número de consultas realizadas por la misma persona y al mayor costo de prestaciones que no son del tipo "pediátricas".

El aumento del gasto es lineal hasta el tramo de los "90 a 94 años", desde donde comienza a disminuir, probablemente debido a una reducción en el uso de ciertos servicios médicos por parte de personas de edad avanzada.

**¿Son estos valores anteriores "correctos"?**  
Es necesario tener en cuenta:  
Por análisis previos, sabemos que en cada tramo de edad existen prestaciones significativamente más costosas, como operaciones, tratamientos o días de hospitalización, y otras más económicas, como consultas médicas o análisis de laboratorio.

Por un lado, combinar prestaciones más económicas y de mayor frecuencia con aquellas más costosas y de menor frecuencia es representativo de la realidad, ya que, aunque no todos enfrentan gastos médicos elevados, nadie está completamente exento de experimentar algún accidente, enfermedad hereditaria o consecuencias de malos hábitos. Por ende, esta "mezcla" de ambos tipos de prestaciones médicas refleja adecuadamente el espectro de costos en la vida de una persona.

Dicho lo anterior y solo con el grafico anterior
Aún no es posible si los valores son "correctos"; no solo nos interesa conocer el promedio, sino también cómo se distribuyen los valores alrededor de él, *es necesario realizar un BoxPlot*, ya que los cuartiles ayudan a detectar si existen personas con gastos excesivamente altos o bajos en comparación con la mayoría, lo que podría distorsionar los resultados.  

**Creacion de BoxPlot**  
En primer intento se busco crear el box plot con todos los valores de "MONTO_COPAGO" pero existian valores muy atipicos sobre 1 millon que dificultan la visualizacion del boxplot, por ende se calculara el IQR para analisar 2 graficos:  
1. "MONTO_COPAGO" Bajo el IQR original  
2. "MONTO_COPAGO" Sobre el IQR original

![Gráfico de boxplot de cuartil <3 de copagos](assets/images/p5_boxplot_q3)

En el cuartil bajo el 75% tenemos el analisis de los siguientes subcuartiles (Todo con el fin de una mayor visualualizacion)  
- En Edad tramo 0 a 2 años, los copagos estan muy concentrado, su 2do y 3er cuartil es muy estrecho, alrededor 7000 pesos por copago.  
- A medida que la edad aumenta, el 3er cuartil tienden a estar menor concentrado, reflejando una mayor variedad de montos de copago y por ende, de tipos de prestaciones. Aun asi la media siempre suele estar en los 7000, he de existir una consulta medica demasiado frecuente que este ese valor, lo mas probable sea una "Consulta medica general".  
- Ahora sumando a nuestra pregunta *¿Cómo cambia el gasto promedio en copagos a medida que los beneficiarios envejecen?*, se infiere que a medida que la persona tiene mayor edad, el tipo de prestacion y su copago tienden a valores mas altos, evindenciando en el 3er cuartil de los datos.

![Gráfico de boxplot de cuartil >3 de copagos](assets/images/p5_boxplot_q4)

Respecto al cuartil superior al 75% de los datos, prestaciones con copago superior a 25000 pesos, los box plot suelen ser muy similares entre los "15 a 19 años" hasta los "85 a 89 años", la media esta en 60000 pesos, por otro lado los extremos aun tiene copagos mas reducidos.  
Ahora bien para responder nuestra pregunta, resulta muy interesante conocer que entre los tramos de "20 a 24 años" hasta los "75 a 79 años" las prestaciones de muy alto costo sobre los 100000 pesos, considerados valores atipicos, tienen muchos datos que si bien no se refleja en los cuartiles, si se puede ver que los datos atipicos aumentan, y por ende el inesperado gasto medico

**Ahora, crearemos un histograma para cada tramo de edad, donde:**  
- Eje x: "MONTO_COPAGO"  
- Eje y: Frecuencia de prestaciones

![Gráfico de histograma de copagos segun tramo edad y sexo](assets/images/p5_histograma_copagos_sexo)

Al entrar en detalle del histograma segun "TRAMO_EDAD" podemos confirmar las conclusiones del boxplot:  
- La media suele estar en 7000
- A medida que aumenta la edad, la frecuecia de prestaciones de mayor valor aumenta
- Las prestaciones alrededor de 15000, aumentan constantemente a medida que el tramo de edad aumenta, hasta llegar a los 85 a 80 años

- Con la nueva variable "SEXO" agregada al HUE, podemos decir que las prestaciones totales para mujeres es casi el doble que de hombres.

![Gráfico de histograma de copagos segun tramo edad y sexo](assets/images/p5_histograma_copagos_sexo)


Al analizar el cuartil superior a q3, y utilizando una escala logaritmica vemos que el numero de prestaciones de muy alto valor empiezan a ser mas frecuente a mayor "edad_tramo" de las personas.  
He de notar que las prestaciones de alto valor entre hombre y mujeres parece equiparse en estos tramos de costo.

### Conclusión

**¿Cómo cambia el gasto promedio en copagos a medida que los beneficiarios envejecen?**  
En base a los 3 tipos de analisas hechos: Frecuencia, boxplot e histogramas para cada tramo de edad. Podemos responder que El gasto promedio aumenta por dos motivos. El mayor numero de frecuencia de prestaciones medicas emitidas por persona a medida que aumenta la edad, generando una campana de gauss con valores bajos en edades cercanas a 0 - 10 años y para 80-100+ años.  

El tipo de prestaciones medicas usadas son mas caras en si, el valor promedio de cada prestacion aumenta con la edad, debido a naturalmente la consulta, operaciones, tratamiento de enfermedades mas propensas en edades mas avanzadas, esto es especialmente notables con operaciones de muy alto coste que suelen ser mas frecuente en edades intermedias hasta avanzadas 30-80 años, pero curiosamente en edades sobre 80 años baja.  

El gasto medico, aumenta linealmente con la edad hasta probablemente el fallecimiento de la persona, y baja sobre los 80 años meramente por la menor cantidad de personas que supera dicha edad.