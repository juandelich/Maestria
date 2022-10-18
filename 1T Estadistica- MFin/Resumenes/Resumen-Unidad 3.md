# Resumen-Unidad 3
El siguiente resuemen cubre los temas de la unidad, incertando distintos elementos que de textos o de ejercicios. Cualquier modelo puntual se desarrolla aparte.

##### Temas:
- Teoría de la Utilidad Esperada. 
- Prima por riesgo y seguros. 
- Teoría de Portafolio. 
- Cobertura y cross hedging.

##### Textos:
- “Utility Analysis in Decision Trees” Luban F., en New Logics for the New Economy 
-  “A Simplified Perspective of the Markowitz Portfolio Theory” Myles Mangram, Global Journal of Business Research, vol 7, January 2013. Un resumen intuitivo del tema.


## Riesgo 
### Como mido el riesgo
Cuando tratamos de cuantificar el riesgo intentamos darle un valor al escenario que se desvia del resultado esperado. Esto valor puede ser la posibilidad de que suceda o el costo de que suceda:
- **Varianza/Desvia Estándar**: Es esl riesgo absoluto de errarle a la media o valor esperado.
- **Coeficiente de variación**: Es el riesgo relativo de errarle a la media.
- **Value at Risk (VaR)**: Es el valor que se puede perder en el caso extremo, el cual se define como el peor porcentaje de la distribución. 
- **Riesgo de Asimetria**: Es el riesgo de que los valores esten sesgados en torno a un valor 
- **Riesgo de Curtosis**: La media puede ser favorable pero los resultados se acumulan en las colas.
- **Beta CAPM**: Es la correlación del activo con el mercado, cuan expuesto estoy al riesgo de mercado.


### La relación del inversor con el riesgo
Es relevante tambien entender la relación que los distintos agentes tienen con el riesgo, para eso catalogamos a los distintos agentes en distintas categorias. Podemos decir que son:

- **Aversos al riesgo**
- **Neutral al riesgo**
- **Amante al riesgo**
- **Actitud frente al riesgo cambiante con riqueza (Friedman-Savage)**

Mientras que existen distintas maneras de concer o medir la aversión al riesgo y en que categoria caen:
1. Laboratorio, dándole a la persona a elegir entre distintas loterías para ir construyendo la u(x): Se van presentado loterias abstractas, segun la elección de los agentes se va calibrando una función de utilidad.
2.  Calibrando una función (e.g. Exponential Utility Function) 
3. Psicometric tests 
4. Neurociencia (right inferior frontal gyrus)
5. Econometrics estimar con datos de la realidad

Esta tambien los coeficientes de Arrow-Pratt que se utilizan para medir la aversión al riesgo una vez que se tiene la función de utlidad

$$
A(c)=-\frac{u''(c)}{u'(c)}
$$
$$
A(c)=-\frac{-cu''(c)}{u'(c)}
$$
## Teoría del portafolio
La teoria del portafolio y la frontera eficiente de Marlkowitz intenta ser una respuesta a la pergunta de como puedo minimizar mi varianza manteniendo constante mi varianza. 

$$
min_{[w]} var(Rp) \space \space sa \space E(Rp) = constante
$$
Esta regla no da como resultado un portafolio sino multiples portafolios con distinto retorno y varianza, pero que son finitos y más optimos que los otros. La preferencia del inversor estara determinada por sus preferencias, es decir si quiere más retorno a cambio de más riesgo. Pero nunca eligira un portafolio suboptimo.
