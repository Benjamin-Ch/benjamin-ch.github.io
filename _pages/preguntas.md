---
title: "Preguntas"
layout: page
permalink: /preguntas/
nav: true
nav_order: 4
---

## ¿Cómo cambia el gasto promedio en copagos a medida que envejecemos?

### Elegir qué observar

- Tramos de edad: Al no contar con un historial médico completo de las personas, analizaremos los gastos agrupados por rangos de edad durante el año 2023.
- Monto de copago: Esto nos muestra cuánto paga una persona por cada servicio médico recibido.

### La distribución de los datos

![Gráfico de distribución de datos por edad](assets/img/p5_distribucion_datos)

Aquí, encontramos un patrón interesante: una curva que concentra la mayoría de los casos en edades centrales, mientras que los extremos tienen menos frecuencia. Esto significa que ciertos grupos, como los recién nacidos o los adultos mayores, tienen menos datos representativos.

**¿Qué podemos deducir de esto?**

- Los recién nacidos (0-2 años) tienen una alta ocurrencia en comparación con los niños mayores, lo que sugiere mayor atención preventiva en sus primeros años de vida.
- Los adultos jóvenes (25-29 años) y los adultos mayores (65-69 años) tienen tasas similares de ocurrencia, posiblemente por razones de rutina médica o tratamientos específicos.
- Más allá de los 70 años, la frecuencia baja significativamente, reflejando la disminución de personas que superan esa edad.

Estas observaciones nos ayudan a entender mejor el panorama, pero todavía necesitamos profundizar en los gastos promedio de cada rango.

### El gasto promedio por edad

![Gráfico de promedio de copagos por edad](assets/img/p5_promedio_copagos_por_edad)

Como era de esperarse, el promedio del monto de copago aumenta con la edad. Pero aquí encontramos algunos puntos intrigantes:

- El despegue: Entre los 15 y 19 años, el gasto promedio comienza a crecer notablemente. Esto podría estar relacionado con una menor dependencia de servicios pediátricos y un aumento en las consultas y tratamientos más especializados.
- El crecimiento sostenido: El aumento del gasto es casi lineal hasta los 90-94 años. Durante este periodo, el uso de servicios médicos parece mantenerse constante o incluso aumentar ligeramente.
- La caída intrigante: A partir de los 95 años, el gasto promedio disminuye. Esto podría deberse a una menor utilización de ciertos servicios médicos.

#### ¿Reflejan estos datos toda la verdad?

Aunque el gráfico es revelador, debemos mirar más allá del promedio. Hay que preguntarnos: ¿existen personas con gastos extremos que están distorsionando esta visión general?

Para encontrar respuestas, sería útil analizar cómo se distribuyen estos valores alrededor del promedio. Por ejemplo, un boxplot nos permitiría identificar si hay personas con gastos inusualmente altos o bajos. Estos extremos, aunque pocos, podrían ser clave para entender la variabilidad real de los costos médicos.


### Profundizando en los datos: ¿Qué nos dicen los Boxplots?

Al analizar el gasto en copagos, encontramos un desafío inicial: existen montos muy elevados (superiores a 1 millón de pesos) que dificultan la visualización general. Para abordar esto, dividimos el análisis en dos grupos:

1. Valores dentro del rango intercuartílico (IQR), es decir, aquellos dentro del 75% de los datos más comunes.
2. Valores por encima del IQR, correspondientes a los gastos más altos.

#### Boxplot del IQR inferior (< Q3)

![Gráfico de boxplot de cuartil <3 de copagos](assets/img/p5_boxplot_q3)

Este análisis revela el comportamiento de las prestaciones de menor costo:

- Diversificación con la edad: A medida que las personas envejecen, los valores del tercer cuartil se dispersan más, reflejando una mayor diversidad en las prestaciones médicas. Este cambio probablemente responde al uso de servicios más costosos como análisis especializados o tratamientos específicos.
- El promedio constante: Aunque los valores se diversifican, los montos promedio de los copagos se mantienen en torno a $7,000. Este dato sugiere que ciertos servicios médicos, como consultas generales, dominan las prestaciones en todos los grupos etarios.

#### Boxplot del IQR superior (> Q3)

![Gráfico de boxplot de cuartil >3 de copagos](assets/img/p5_boxplot_q4)

Este análisis revela el comportamiento de las prestaciones de mayor costo:

- Uniformidad en los tramos intermedios: Entre los 15 y 89 años, el promedio de copagos de alto costo se estabiliza alrededor de $60,000. Esto indica una consistencia en el tipo de prestaciones costosas utilizadas por estos grupos.
- Incremento en valores atípicos: A partir de los 20 años y hasta los 75, notamos un aumento significativo en los gastos extremadamente altos (superiores a $100,000). Estos gastos suelen estar asociados con procedimientos quirúrgicos, tratamientos especializados u hospitalizaciones prolongadas.

### Explorando con histogramas

Para entender mejor la frecuencia de las prestaciones y cómo varían según la edad, generamos histogramas:

#### Histogramas de Prestaciones de bajo costo

![Gráfico de histograma de copagos segun tramo edad y sexo - Q<3](assets/img/p5_histograma_copagos_sexo)

Al analizar estos gráficos, se confirman las tendencias previas, pero se puede agregar que:

- Diferencias por género: Las mujeres realizan casi el doble de prestaciones en comparación con los hombres, lo que podría explicarse por un mayor uso de servicios relacionados con salud femenina o consultas preventivas.

#### Histogramas Prestaciones de alto costo

![Gráfico de histograma de copagos segun tramo edad y sexo - Q>3](assets/img/p5_histograma_copagos_sexo_q4)

Con una escala logarítmica, es evidente que las prestaciones de muy alto costo aumentan en frecuencia conforme las personas envejecen, pero a partir de los 80 años, la tendencia se estabiliza. Además, en estos rangos de copagos elevados, las diferencias entre hombres y mujeres tienden a desaparecer.

### Conclusión

¿Cómo cambia el gasto promedio en copagos a medida que los beneficiarios envejecen?

Tras analizar los datos mediante frecuencia, boxplots e histogramas, llegamos a las siguientes conclusiones:

- Frecuencia de uso: A medida que las personas envejecen, el número de prestaciones médicas que realizan aumenta hasta los 80 años, creando una curva en forma de campana. Esto refleja un mayor uso de servicios médicos por necesidades asociadas a la edad.
- Costo promedio por prestación: Las prestaciones médicas se encarecen con la edad. Aunque el promedio de copagos en servicios básicos es constante ($7,000), los servicios especializados o tratamientos avanzados son más frecuentes y costosos en edades intermedias (30-80 años).
