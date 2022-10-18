# Resumen-Unidad 8
El siguiente resuemen cubre los temas de la unidad, incertando distintos elementos que de textos o de ejercicios. Cualquier modelo puntual se desarrolla aparte.

Temas:
- Problemas econométricos en la estimación de un modelo Autocorrelación; multicolinealidad y heterocedasticidad: métodos para detectar su presencia. 
- Análisis de las causas, efectos y soluciones a los problemas econométricos. 
- Aplicaciones: Asset Pricing. CAPM. Modelo Multifactor. Non-frequent Trading. Evaluación de Desempeño. Corporate Finance. Event Study Analysis. Regression Based Analysis

Textos:
- Cap 5 de “Financial Econometrics. From Basics to Advanced Modeling Techniques” Fabozzi Series. 
- Cap II de “Market Risk Analysis II. Practical Financial Econometrics” Alexander Carol 
-  Cap 4 a 6 “The Econometrics of Financial Markets”, Campbell, Lo and MacKinlay


### Correlación
### Modelo lineal
#### OLS
### Modelo general
#### Propiedades
El modelo de Minimos cuadrados tiene algunas propiedades:
**Propiedad 1**: La regresión lineal pasa por la media muestal tanto de X como de Y. 
**Propiedad 2**: La media de la predicción es igual la media muestral de $Y$
**Propiedad 3**: La media y la suma de los errores de predicción es cero
**Propiedad 4**: Los errores de predicción tienen correlación nula con los valores predecidos $\hat {Y_i}$ 
**Propiedad 5**: Los errore sde predicción tienen correlación nula con los valores de $X$
**Propiedad 6**: La estimación de OLS no es más que un promedio ponderado de los valores de $Y$

### Como evaluar las regresiones
### Poder explicativo
Una manera de medir cuan explicativo es un modelo, es calcular el $R^2$ de un modelo. En un modelo tenemos:
$$
\text{Suma de cuadrados total (SST)}= ({Y_1}- \bar{Y})^2+...+({Y_n}- \bar{Y})^2

$$
La $SST$ explica la variabilidad total de los datos, lo cual es independiente del modelo que tengamos y es algo de nuestro input

$$
\text{Suma de cuadrados de regresión(SSR)}=(\hat{Y_1}- \bar{Y})^2+...+(\hat{Y_n}- \bar{Y})^2 
$$
La SSR cumple la función de ser la variabilidad que el modelo explica, es decir la media muestral menos los valores predichos. En un modeo 100% correcto esto seria igual a uno.
$$
\text{Suma de cuadrados del error(SSE)}=({Y_1}- \hat{Y_1})^2+...+({Y_n}- \hat{Y_n})^2 
$$
La suma de cuadrados del error es el contrario, osea lo que no podemos explicar o difiere de lo explicado. Si el modelo ajustara perfecto, entonces este valor sería cero. 

####  $R^2$ y $\bar{R^2}$
Es una medida que usamos para ver la capacidad de explicación que tiene un modelo, de esta manera se expresa como:

$$
R^2 = \frac{SSR}{SST} =1- \frac{SSE}{SST}
$$
En este sentido el $R^2$ es el porcentaje de la variación total de la variable que es explicada en el modelo. 

Pero hay  elementos a tener en cuenta, si agregamos variables el $R^2$ inevitablemente aumentara. Por lo que existen medidas que ponderan esto. Así aparece el $\bar{R^2}$

$$
\bar{R^2} =1-\frac{SSE/(T-K)}{SST/(T-1)}
$$

### Test de significatividad individual
### Test de Significación Global (Test F)
