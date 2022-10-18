# Resumen-Unidad 1 
El siguiente resuemen cubre los temas de la unidad, incertando distintos elementos que de textos o de ejercicios. Cualquier modelo puntual se desarrolla aparte.

Temas:
- Estadísticas Descriptivas / Technical Analysis
- Medición de retornos en finanzas. 
- Medidas de riesgo: desvío estándar, coeficiente de variación, VaR Empírico, beta CAPM, índice de Sharpe, índice de Treynor. 
- Introducción al Análisis técnico.

---

## Estadistica descriptiva 

### Basico
En la parte de estadistica descriptiva aparecen ciertos conceptos ya vistos integrados al analisis de activos. El uso de medidas como la media y mediana como estimadores del rendimiento. 

*La mediana*: Me permite eliminar los outliers ya que nos da el valor que se encuentra en la mitad de los datos. Su relación con la media depende de la asimetria de la distribución de resultados: Si la asimentria de los resultados es negativa, la media sera menor a al mediana y a la inversa si la asimetria es postiva. 

==IMAGEN==

Dentro de las mediciones de la media esta la media Aritmentica y la media Geométrica 

*Media Aritmetica*: $$\overline{X}= \frac{x_1+x_2+x_3+...+x_n}{n}=\frac{\sum^{n}_{i=1} x_i}{n}$$
Media aritmética del retorno bruto es el retorno que ocurrió más seguido (estimador del “valor esperado”)

*Media Geometriaca*: $$\overline{X}=\sqrt[n]{x_1.x_2...x_3}=\sqrt[n]{\prod^{n}_{i=1}(x_i)}$$
La media geometria me permite medir efectivamente cuales fueron mis retornos en un periodo. Si en $T_1$ obtuve 7%, en $T_2$ obtuve 6% y en $T_3$ obtuve 6%. Entonces en total mi tasa de retorno promedio efectiva fue de:
$$
\overline{X}=\sqrt[3]{1,07.1,06.1,06} = 1.0633= 6,33\%
$$
Media geométrica del retorno bruto es el retorno efectivo que obtuvo en el período un inversor que entró en el día 0 y se fue en el día T.

Estan tambien la *media ponderada* y la *media movil*. La primera se utiliza comunmente para cuando se trabaja con portafolios y se necesita ponderar por los distintos componentes.  La *media movil* es tipicamente algo utilizado en analisis tecnico para seguir la evolución de un precio. 

Por utlimo esta la *media movil exponencial* en la cual se le asigna un valor exponencial a los valores más cercanos para que los mismos tengan más pesos. $s$ sería un factor de ajuste o para suavizar, $d$ son los dias en el moving average. Se usa en las bandas de boilinger o en bandas de soporte.

$$
\overline{X_{e,t}}= \alpha X_{t-1} + (1-\alpha) \overline{X_{m,t-1}}  \space \space\space \alpha=\frac{s}{1+d}
$$

### Precios 
El precio de pizarra marca (*Closing Price*) el precio de cierre, es importante tener en cuenta que se puede ver afectado por elementos como pago de dividendos. Por lo tanto no siempre es recomendable su uso, para trabajo estadistico es mejor el precio ajustado (*Adjusted Price*).

El precio ajustado puede reflejar variaciones en el precio por division de la acción (split) o por pago de dividendos. En el caso de un split se divide el preció hacía atras por la misma cuatia que el split. En el caso del pago de dividendos se hace un multiplicador por dividendos.

*Dividend multiplier*: Se utiliza para multiplicar todos los valores anteriores de la serie, y se construye como.
$$
DM= \frac{1-\text{Dividendo}}{\text {Precio de pizarra}}
$$
Cada vez que se paga un dividendo se debe volver a multiplicar a toda la serie. 

### Retornos
El retorno es la medida con la que capturamos el exito de las deciones financieras. Tenemos distintas medidas de retorno debido a que no siempre es igual los datos o elementos que usaremos. Se tiende a utilizar los precios ajustados porque expresan correctamente la ganancia de capital, o lo ganado por la capitalización del portafolio.

*Retorno Total*: El Retorno total tiende a realizarse sobre el precio ajustado ya que incluye el pago de dividendos y se expresa como:
$$
R_t=\frac{P_t=P_{t-1}+D_t}{P_{t-1}}
$$
*Retornos Discretos:*
$$
R= (P_1/P_0)-1
$$
*Retornos Continuos:*
$$
R= ln(P_1/P_0)
$$


### Portafolios y promedio ponderados

==PAJA y  hay cosas más relevantes ahora==


### BEHAVIORAL FINANCE
### ÍNDICES DE MERCADO
Es un portafolio que buscar mostrar la evolución de un mercado para lo cual debe escoger qué acciones incluir y cuánto ponderar a cada una.Pueden ser “value weighted” donde el peso se pone en función del pasado reciente de las acciones en términos de volumen transado. Pueden tener pesos fijos (equal weighted portfolio) donde al estar fijo el peso no tenemos efecto momentum que pesen más las que suben más, siempre todas pesan igual.

### Normalidad
Los retornos diarios de varias acciones tienden a tener retornos que se distribuyen de manera normal. 

### Riesgo
El riesgo es el intento de estimar o cuantificar la cantidad o magnitud de los estados negativos sobre los retornos. Para esto existen diferentes elementos que pueden ayudar a determinar el riesgo al que uno esta expuesto. 

- Rango: riesgo como amplitud de retornos posibles 
- Rango intercuartil: riesgo como amplitud de retornos posibles eliminando extremos. 
- Varianza / Desvío Estándar: riesgo “absoluto” de “errar a la media” (si me alejo mucho o poco de la media) 
- Coeficiente de Variación: riesgo “relativo” de errar a la media (si me alejo mucho o poco en porcentaje de esa media

Algunos elementos para medir el riesgo son:

*Coeficiente de Variación Muestral*: 
$$
CV=\frac{s}{\overline{X}}
$$
Distintos activos pueden tener medias y varianzas distintas, por lo que comparar los devios estandar de los portafoliios puede no ser la mejor medida para comparar riesgo. El coeficiente de variación mensual peromite ponderar la varianza muestral sobre la media muestral.

*Ratio de Sharpe*
El ratio de Sharpe trata de mostrarle al inversor la relación entre el riesgo y el retorno de una inversión.

$$
Sh_i = \frac{\overline{R_i}- r_{rf}}{s_i}
$$
El Ratio de Sharpe plantea una suerte de inversa del coeficiente de varición, pero le resta al retorno esperado la tasa libre de riesgo(*risk free*). Cuando se comparan dos inversiones la inversión con el Ratio de Sharpe más alto proporciona mayor rendimiento para un mismo nivel de riesgo.

*Ratio de Treynor*

$$
Treynor = \frac{\overline{R_i}- r_{rf}}{\beta_i}
$$
El ratio de treynor aplica la misma idea quel rartio de sharpe pero sobre el beta de activo al mercado, basandose en el modelo CAPM.

#### VaR
El VaR es la abreviatura del concepto *Value at Risk*, que intenta determinar que porción de mi portafolió estaría perdiendo en el peor de los casos. Es decir cual es la peor caida posible con probabilidad de X%. Esto se conoce como VaR empirico y es usualmente al 1% o 5%

#### Asimetria 
La asimetria aparece como una medida descriptiva de la distribución de los datos respecto de la media. Dos funciones pueden tener la misma media y asimetrias distintas. Una función que sigue la distribución normal tiene un coeficiente de asimentria igual a cero.

Una función con un coeficiente de asimetria negativo tendra la mayor parte de sus puntos de datos a la derecha de la media, es decir que seran mayores que la misma. Una función que tenga una asimetria positiva, tendra mayor cantidad de datos a  la izquiera y significa que son menores. 

En el casos de las finanzas el coeficiente de asimetria permite ver como se distrubuyen los datos y saber si la media o la mediana es más representativa. Entre mayor sea la asimetria más distinta son la medía y la mediana. 

#### Kurtosis 
La curtosis es una medida de riesgo que refiere a los riesgos de resultados extremos. Dos funciones pueden tener medias y varianzas iguales, sin embargo curtosis distintas. Si nuestra función de retornos tiene un valor de curtosis muy negativo, esto significa que estaremos más expuestos a resultados extremos o distantes de la media.

### Análisis Técnico

