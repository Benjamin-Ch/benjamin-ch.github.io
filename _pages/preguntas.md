---
title: "Preguntas"
layout: page
permalink: /preguntas/
nav: true
nav_order: 4
---

# Preguntas

<hr class="mb-5">

## 1 - ¿Qué tipos de prestación médica son más frecuentes entre diferentes tramos de edad y género?
Nuestro análisis identifica cómo las necesidades de salud varían según las características demográficas de la población.

### Variables consideradas
- Tramo de edad: Representa los diferentes grupos etarios de la población, segmentados para reflejar etapas de vida (infancia, adolescencia, adultez, vejez).
- Género: Permite observar diferencias en el uso de prestaciones entre hombres y mujeres.
- Tipo de prestación médica: Identifica el servicio o atención recibida (por ejemplo, consultas generales, hospitalizaciones, urgencias, procedimientos específicos).

### Análisis por tramo de edad
Separamos los tramos de edad en 4 grupos etarios principales:

- Grupo 1: los tramos de 00 a 09 años (niñez)
- Grupo 2: los tramos de 10 a 19 años (adolescencia)
- Grupo 3: los tramos de 20 a 59 años (adultez)
- Grupo 4: los tramos de 60 a +99 años (vejez)

#### Niñez (0-9 años):
![Grupo 1]({{ site.baseurl }}/assets/img/grupo1p1.png){: .img-fluid }
![Gráfico de promedio de copagos por edad]({{ site.baseurl }}/assets/img/p5_promedio_copagos_por_edad.png){: .img-fluid }

Predominan consultas pediátricas y generales, enfocadas en el desarrollo infantil y la prevención.

#### Adolescencia (10-19 años):
![Grupo 2]({{ site.baseurl }}/assets/img/grupo2p1.png){: .img-fluid }
Se destacan las consultas generales y pediátricas, además de la aparición de prestaciones como psicoterapia, reflejando una mayor atención a la salud mental.

#### Adultez (20-59 años):
![Grupo 3]({{ site.baseurl }}/assets/img/grupo3p1.png){: .img-fluid }
Lidera la consulta general, junto con especialidades como ginecología y análisis como el perfil hepático, fundamentales para monitorear la salud en esta etapa activa.

#### Vejez (60+ años):
![Grupo 4]({{ site.baseurl }}/assets/img/grupo4p1.png){: .img-fluid }
Se mantiene el predominio de consultas generales, sumándose la atención en oftalmología y procedimientos venosos, reflejando el impacto del envejecimiento en la salud.


### Análisis por género
#### Mujeres:
![Mujeres]({{ site.baseurl }}/assets/img/mujerp1.png){: .img-fluid }
Alta frecuencia en consultas generales y ginecológicas, con análisis como el perfil hepático y bioquímico. También se destacan atenciones específicas como el monitoreo de vitamina D y hemogramas.

#### Hombres: 
![Hombres]({{ site.baseurl }}/assets/img/hombrep1.png){: .img-fluid }
Predomina la consulta general, con presencia notable de especialidades como traumatología y urología. Además, se realizan análisis específicos como el antígeno prostático y creatinina.

### Conclusión
El análisis de las *prestaciones médicas según el rango etario* refleja patrones esperados basados en las necesidades de salud asociadas a cada etapa de la vida:

- En las edades más bajas, predominan las atenciones relacionadas con pediatría y consulta general, lo cual es coherente con el seguimiento del desarrollo infantil, la vacunación y la atención de enfermedades comunes en la infancia.
- La prestación de psicoterapia aparece exclusivamente en el grupo de adolescentes, lo que subraya la relevancia de abordar problemas emocionales y de salud mental en esta etapa crítica de desarrollo.
- Las prestaciones como consulta general, perfil hepático y perfil bioquímico se mantienen frecuentes en todos los grupos etarios. Esto puede explicarse por su uso en chequeos rutinarios o como parte de estrategias preventivas para monitorear la salud general de la población.

El análisis de la *distribución de prestaciones médicas entre géneros* evidencia diferencias notables:

- Las mujeres acceden a más atenciones médicas que los hombres, con una diferencia significativa en la prestación más demandada (10,000 atenciones para mujeres frente a 6,000 para hombres en el top 1).
- Las prestaciones de obstetricia y ginecología son claramente predominantes en las mujeres, lo que refleja necesidades relacionadas con la salud reproductiva y materna.
- El perfil hepático, asociado a chequeos generales o diagnósticos específicos, resulta una prestación común entre ambos géneros, lo que indica su relevancia en el monitoreo de la salud hepática independientemente del género.
- En el caso de pediatría, se observa una mayor cantidad de consultas para hombres que para mujeres. Este patrón podría estar vinculado a diferencias biológicas, sociales o culturales en el acceso o la demanda de estos servicios para niños y niñas.

*En resumen*, el análisis muestra cómo las necesidades de salud evolucionan con la edad, y cómo estas varían entre hombres y mujeres, lo que subraya la importancia de tener en cuenta estas variables al planificar y ofrecer servicios de salud. Además, enfatiza la necesidad de promover la prevención y el cuidado integral en todas las etapas de la vida.

<hr class="mb-5">

## 2. ¿Cómo varía la cantidad y tipo de prestaciones emitidas según el mes del año? ¿Existen patrones estacionales?

```python
meses = True                 # variable que define si vamos a generar el gráfico en base a meses o a estaciones
codigo_prestacion = 101001   # variable para indicar la prestación a analizar
```

![Grafico p2]({{ site.baseurl }}/assets/img/p2-a.png){: .img-fluid }

El análisis de las prestaciones médicas a lo largo del año revela que las cinco principales son: consulta médica general, consulta especializada en obstetricia y ginecología, perfil hepático, extracción venosa en adultos y perfil bioquímico. A nivel temporal, se identifican patrones estacionales claros en la demanda de servicios médicos. Otoño es la estación con mayor volumen de prestaciones, seguida por invierno y verano, mientras que primavera presenta la menor actividad.

Desde una perspectiva de ciencia de datos, estos resultados sugieren la necesidad de implementar modelos predictivos estacionales que optimicen la asignación de recursos sanitarios, ajustando la capacidad de atención según la demanda prevista.


## 3 - ¿Qué tipos de prestación médica son más frecuentes en cada región?
### Elegir qué observar
- Región de emisión: Identifica las regiones donde se emitieron las prestaciones durante 2023.
- Nombre de la prestación: Muestra los diferentes tipos de prestaciones emitidas, facilitando el análisis de su distribución.
- Frecuencia: Indica cuántas veces se emitió cada prestación en cada región, destacando las combinaciones más comunes.

![Tabla prestaciones]({{ site.baseurl }}/assets/img/p3_gra.jpg){: .img-fluid }

### Distribución de los datos
En este análisis, podemos observar que, en todas las regiones, la prestación más solicitada por las personas es la consulta médica general. La frecuencia muestra la proporción de personas que solicitaron esta consulta en cada región.

![Grafico prestaciones]({{ site.baseurl }}/assets/img/p3_bar.png){: .img-fluid }

**¿Qué podemos deducir de esto?**
- Es posible que en las regiones con mayor frecuencia, hay una mayor demanda de esa prestación en particular. Esto indica que un mayor número de personas están solicitando esa prestación, lo que refleja una preferencia o necesidad más alta en esas regiones.
- Es posible que en las regiones con alta frecuencia, probablemente se necesiten más recursos (como personal, infraestructura o equipos) para poder satisfacer esa demanda de manera adecuada. Una mayor frecuencia de solicitudes podría implicar una mayor presión sobre los recursos disponibles en esas regiones.
- Es posible que una menor frecuencia en ciertas regiones indique que no hay suficientes recursos para cubrir la demanda de manera eficiente. Si la demanda es alta, pero los recursos disponibles son limitados, esto podría provocar que la frecuencia observada sea baja.
  
### Distribución geográfica de los datos
Este tipo de análisis representa la misma información que la primera visualización, pero se presenta de manera geográfica.

![Grafico mapa]({{ site.baseurl }}/assets/img/p3_map.png){: .img-fluid }

### Conclusión
En este análisis, se exploró la frecuencia de las prestaciones médicas más comunes en diversas regiones del país, utilizando tanto un gráfico de barras como un mapa geográfico para visualizar los resultados. Se identificó que la prestación médica más frecuente en todas las regiones es la "Consulta Médica General", aunque las frecuencias varían significativamente entre las regiones. La Región Metropolitana de Santiago, por ejemplo, presenta la mayor cantidad de consultas, mientras que otras regiones, como Aysén del Gral. C. Ibáñez del Campo, muestran una demanda mucho menor.

Este patrón de distribución refleja no solo las diferencias en el acceso y la demanda de servicios médicos, sino también posibles disparidades regionales en infraestructura y atención sanitaria. Las regiones más urbanizadas tienden a tener una mayor concentración de consultas, mientras que las zonas más alejadas podrían enfrentar desafíos relacionados con la disponibilidad y el acceso a estos servicios.

En resumen, este análisis destaca la importancia de considerar las diferencias regionales en el acceso a la atención médica y la necesidad de políticas públicas que aborden estas desigualdades para mejorar la cobertura y la calidad de los servicios de salud en todo el país.

<hr class="mb-5">

## 4 - ¿Cómo se relacionan los distintos tramos de Fonasa con la frecuencia y el tipo de prestaciones recibidas?

Queremos estudiar los distintos tramos para poder adquirir contexto de los distintos tramos y sus comportamientos respectos a los distintos tipo de producto de Fonasa que la poblacion estuvo haciendo.

Primero vamos a analizar el contexto de los datos en los que nos encontramos respecto a cierta porcion de la totalidad de la base de datos y luego vamos a poder realizar un estudio normalizado de todos los datos.

De aqui podremos ver ordenada segun la edad y el tramo para adquirir tambien cierta nocion de la forma en que esos datos estan distribuidos en la poblacion segun distintas variables

Ahora vamos a graficar segun el sample que sacamos de la base de datos de MLE para poder adquirir cierta nocion del por un lado el tramo y luego la frecuencia de esta respecto al sample que obtuvimos.

![Grafico 1]({{ site.baseurl }}/assets/img/p4-1.png){: .img-fluid }

Luego aca podemos analizar la distribucion de tipos de prestacion por tramo y poder analizar la porcion que cada distribucion adquiere en nuestro sample.

![Grafico 2]({{ site.baseurl }}/assets/img/p4-2.png){: .img-fluid }

Finalmente aplicamos cierta normalizacion segun la norma para poder adquirir una nocion que trasciende las distribuciones relativas segun el tipo de sample que uno quiera adquirir

Ahora analizando las relaciones y porcentajes entre las variables tenemos:

![Grafico 3]({{ site.baseurl }}/assets/img/p4-3.png){: .img-fluid }

![Grafico 4]({{ site.baseurl }}/assets/img/p4-4.png){: .img-fluid }

Podemos luego terminar analizando y concluyendo los tramos y las distintas distribuciones que son mas consumidas por los clientes de Fonasa, por un lado los Examenes de Diagnostico en la totalidad de los distintos tramos y de la misma forma las atenciones medicas las cuales hacen sentido ya que se podria decir que es lo que la gente mas hace sin necesidad de buscar cierta atencion especial

<hr class="mb-5">


## 5 - ¿Cómo cambia el gasto promedio en copagos a medida que envejecemos?
### Elegir qué observar
- **Tramos de edad**: Al no contar con un historial médico completo de las personas, analizaremos los gastos agrupados por rangos de edad durante el año 2023.
- **Monto de copago**: Esto nos muestra cuánto paga una persona por cada servicio médico recibido.

### La distribución de los datos

![Gráfico de distribución de datos por edad]({{ site.baseurl }}/assets/img/p5_distribucion_datos.png){: .img-fluid }

Aquí, encontramos un patrón interesante: una curva que concentra la mayoría de los casos en edades centrales, mientras que los extremos tienen menos frecuencia. Esto significa que ciertos grupos, como los recién nacidos o los adultos mayores, tienen menos datos representativos.

**¿Qué podemos deducir de esto?**
- **Los recién nacidos** (0-2 años) tienen una alta ocurrencia en comparación con los niños mayores, lo que sugiere mayor atención preventiva en sus primeros años de vida.
- **Los adultos jóvenes** (25-29 años) y los adultos mayores (65-69 años) tienen tasas similares de ocurrencia, posiblemente por razones de rutina médica o tratamientos específicos.
- **Más allá de los 70 años**, la frecuencia baja significativamente, reflejando la disminución de personas que superan esa edad.

Estas observaciones nos ayudan a entender mejor el panorama, pero todavía necesitamos profundizar en los gastos promedio de cada rango.

### El gasto promedio por edad

![Gráfico de promedio de copagos por edad]({{ site.baseurl }}/assets/img/p5_promedio_copagos_por_edad.png){: .img-fluid }

Como era de esperarse, el promedio del monto de copago aumenta con la edad. Pero aquí encontramos algunos puntos intrigantes:

- **El despegue**: Entre los 15 y 19 años, el gasto promedio comienza a crecer notablemente. Esto podría estar relacionado con una menor dependencia de servicios pediátricos y un aumento en las consultas y tratamientos más especializados.
- **El crecimiento sostenido**: El aumento del gasto es casi lineal hasta los 90-94 años. Durante este periodo, el uso de servicios médicos parece mantenerse constante o incluso aumentar ligeramente.
- **La caída intrigante**: A partir de los 95 años, el gasto promedio disminuye. Esto podría deberse a una menor utilización de ciertos servicios médicos.

#### ¿Reflejan estos datos toda la verdad?
Aunque el gráfico es revelador, debemos mirar más allá del promedio. Hay que preguntarnos: ¿existen personas con gastos extremos que están distorsionando esta visión general?

Para encontrar respuestas, sería útil analizar cómo se distribuyen estos valores alrededor del promedio. Por ejemplo, un boxplot nos permitiría identificar si hay personas con gastos inusualmente altos o bajos. Estos extremos, aunque pocos, podrían ser clave para entender la variabilidad real de los costos médicos.


### Profundizando en los datos: ¿Qué nos dicen los Boxplots?
Al analizar el gasto en copagos, encontramos un desafío inicial: existen montos muy elevados (superiores a 1 millón de pesos) que dificultan la visualización general. Para abordar esto, dividimos el análisis en dos grupos:

1. Valores dentro del rango intercuartílico (IQR), es decir, aquellos dentro del 75% de los datos más comunes.
2. Valores por encima del IQR, correspondientes a los gastos más altos.

#### Boxplot del IQR inferior (< Q3)
![Gráfico de boxplot de cuartil <3 de copagos]({{ site.baseurl }}/assets/img/p5_boxplot_q3.png){: .img-fluid }

Este análisis revela el comportamiento de las prestaciones de menor costo:

- **Diversificación con la edad**: A medida que las personas envejecen, los valores del tercer cuartil se dispersan más, reflejando una mayor diversidad en las prestaciones médicas. Este cambio probablemente responde al uso de servicios más costosos como análisis especializados o tratamientos específicos.
- **El promedio constante**: Aunque los valores se diversifican, los montos promedio de los copagos se mantienen en torno a $7,000. Este dato sugiere que ciertos servicios médicos, como consultas generales, dominan las prestaciones en todos los grupos etarios.

#### Boxplot del IQR superior (> Q3)
![Gráfico de boxplot de cuartil >3 de copagos]({{ site.baseurl }}/assets/img/p5_boxplot_q4.png){: .img-fluid }

Este análisis revela el comportamiento de las prestaciones de mayor costo:

- **Uniformidad en los tramos intermedios**: Entre los 15 y 89 años, el promedio de copagos de alto costo se estabiliza alrededor de $60,000. Esto indica una consistencia en el tipo de prestaciones costosas utilizadas por estos grupos.
- **Incremento en valores atípicos**: A partir de los 20 años y hasta los 75, notamos un aumento significativo en los gastos extremadamente altos (superiores a $100,000). Estos gastos suelen estar asociados con procedimientos quirúrgicos, tratamientos especializados u hospitalizaciones prolongadas.

### Explorando con histogramas
Para entender mejor la frecuencia de las prestaciones y cómo varían según la edad, generamos histogramas:

#### Histogramas de Prestaciones de bajo costo

![Gráfico de histograma de copagos segun tramo edad y sexo - Q<3]({{ site.baseurl }}/assets/img/p5_histograma_copagos_sexo.png){: .img-fluid }

Al analizar estos gráficos, se confirman las tendencias previas, pero se puede agregar que:

- **Diferencias por género**: Las mujeres realizan casi el doble de prestaciones en comparación con los hombres, lo que podría explicarse por un mayor uso de servicios relacionados con salud femenina o consultas preventivas.

#### Histogramas Prestaciones de alto costo

![Gráfico de histograma de copagos segun tramo edad y sexo - Q>3]({{ site.baseurl }}/assets/img/p5_histograma_copagos_sexo_q4.png){: .img-fluid }

Con una escala logarítmica, es evidente que las prestaciones de muy alto costo aumentan en frecuencia conforme las personas envejecen, pero a partir de los 80 años, la tendencia se estabiliza. Además, en estos rangos de copagos elevados, las diferencias entre hombres y mujeres tienden a desaparecer.

### Conclusión
¿Cómo cambia el gasto promedio en copagos a medida que los beneficiarios envejecen?

Tras analizar los datos mediante frecuencia, boxplots e histogramas, llegamos a las siguientes conclusiones:

- **Frecuencia de uso**: A medida que las personas envejecen, el número de prestaciones médicas que realizan aumenta hasta los 80 años, creando una curva en forma de campana. Esto refleja un mayor uso de servicios médicos por necesidades asociadas a la edad.
- **Costo promedio por prestación**: Las prestaciones médicas se encarecen con la edad. Aunque el promedio de copagos en servicios básicos es constante ($7,000), los servicios especializados o tratamientos avanzados son más frecuentes y costosos en edades intermedias (30-80 años).

<hr class="mb-5">

## Extra - Modelamiento

### Justificación
Se utilizara una regresion lineal simple, ya que creemos que la relación entre las variables "total1" (variable independiente) y "bene1" (variable dependiente) es es aproximadamente lineal, a continuacion describiremos tabla y atributos:  

El dataframe utilizado es "~presupuestos_fonasa", el cual contiene todos los prepuestos para los distintos tramos de fonasa, en este caso trabajaremos en el tramo B (recordar que tramo A, no tiene beneficios en MLE).  
- "total1" es un monto en pesos que figura el arancel fijo de una prestacion medica para todos los centros medicos, el monton bruto, sin beneficios.
- "bene1" es el valor real que el usuario debe pagar, el descuento es cobrado al prestador de salud, en este caso FONASA.  

Lo que buscamos es predecir el valor "bene1" dado un "total1", dado que el sistema de salud siempre esta en evolucion, el asignar nuevos valores de copago para nuevas prestaciones medicas es necesario, para ello podemos utilizar informacion pasada para reconocer los patrones de asignacion.

**Trabajaremos con montos_totales bajo 1 millon de pesos...**  
Dado que la asignacion de prepuestos para prestaciones de alto costo, deberia ser una desicion humana y con cierto criterio etico.

![Gráfico de Matriz de correlación]({{ site.baseurl }}/assets/img/mode_matriz_cor.png){: .img-fluid }

![Gráfico de puntos]({{ site.baseurl }}/assets/img/mode_pairplot.png){: .img-fluid }

Parece existir una correlacion perfecta entre nuestras variables... Es motivo de decepcion? para nada, vamos a conocer un modelamiento perfecto que revelara en el mejor de los casos y salvo valores atipicos el porcentaje de descuento asignado por fonasa a cada tramo, informacion que no es difundida y que a simple vista y sin conocer todos los datos, seria dificil de intuir.  
**Vamos a continuar...**

## Regresion lineal

![Gráfico de regresión lineal]({{ site.baseurl }}/assets/img/mode_regresion.png){: .img-fluid }

En primera instancia podemos ver la perfecta correlacion, descrita anteriormente.   

**Métricas de Entrenamiento**  
r^2 : 0.9857414269255609  
RMSE 80788876.07357095  
Coeficientes: (np.float64(0.4892123414341468), np.float64(765.0676201920578))  

**Métricas de Prueba**  
r^2 : 0.9979559974049224  
RMSE 11068985.425669638  

**Metricas de Entrenamiento**  
R² (coeficiente de determinacion): 0.9857  
Esto indica que el modelo explica el 98.57% de la variabilidad en "bene1" usando "total1". Es un ajuste excelente.  

RMSE (error cuadratico medio): 80,788,876.07  
Aunque el valor absoluto parece alto, las magnitudes de los datos son grandes.  

Coeficientes:  
Intercepto: 765.0676  
Pendiente: 0.4892. Esto indica que por cada peso que aumenta "total1", "bene1" aumenta en aproximadamente 0.489 pesos.

**Metricas de Prueba**  
R²: 0.9979  
Similar al entrenamiento, el modelo tiene un ajuste excelente en los datos de prueba, explicando el 99.79% de la variabilidad.  

RMSE: 11,068,985.43  
El error en los datos de prueba es mucho menor que en el entrenamiento, lo cual indica un buen rendimiento.