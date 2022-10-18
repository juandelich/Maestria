$$
% Macros para hacer más fácil todo
% Arma una derivada parcial
\newcommand{\pd}[2]{\frac{\partial#1}{\partial#2}}
% encloses the argument using stretchable parentheses
\newcommand{\pa}[1]{\left( #1 \right) } 
% encloses the argument using strechable brackets
\newcommand{\br}[1]{\left[ #1 \right] }
% encloses the argument using strechable curly brackets
\newcommand{\llave}[1]{\left\{#1\right\}}
% Define un vector dada una variable,  n
\newcommand{\avector}[2]{(#1_1,#1_2,\ldots,#1_{#2})}
% Real Numbers
\newcommand{\R}{\mathbb{R}}
% leftrightarrow shortcut
\newcommand{\LRA}{\leftrightarrow}
$$
# Resumen sobre VAR
Resumen de la clase y PPT sobre VAR

## Que es el VaR
El VaR intenta presentarse como una cuantificación monetaria de cierto riesgo, respondiendo a la pregunta: En un caso X% probable dentro de este marco de tiempo, cual es nuestra perdida? Esto lleva de por medio multiples supuestos sobre el mercado, como las condicione o lo distribución. 

### Ventajas

- Medida única de riesgo 
- Relativamente libre de modelo y supuestos 
-  No depende de la aversión al riesgo del inversor 
-  Fácil de explicar 
- Permite desviaciones del modelo Normal 
- Captura el comportamiento en las colas de los retornos del portafolio.
- Puede ser estimada robustamente a partir de los datos, no es muy sensible a outliers. Sólo es sensible al cuartil p de la distribución 
-  Se aplica a cualquier tipo de activeo y portafolios complejos

### Desventajas
- Si me equivoco en los supuestos (ejemplo: asumo normalidad pero la distribución de retornos tiene colas anchas) me equivoco en la estimación (no es robusto a cambios de supuestos).
-  No me dice nada sobre lo que puede pasar cuando “quiebro” elVaR (VaR Condicional).


## Metodologías VaR
### VaR historico
Se computa sobre la una serie larga de datos y se busca el peor caso dentro de los percentiles ordenados, comunmente el percentil 1%, 5%, o 10%. La **ventaja** es que no se asume una distribución de probabilidad, mientras que la **desventaja** son: las series largas  que se necesitan para estiamar y la posibilidad de cambios extructurales.

### VaR Covariance 
En el Va(R Covariance asumimos que la distribución de los retornos de los octivos es conocida o que pudo estimarse, por lo que podemos usar una Normal o una T-student. Si se usan retornos diarios asumimos que el retorno medio es igual a cero.
La principal **desventaja** es la probabilidad de tener una distribución equivocada y por lo tanto cometer un error.

==Mirar Ejercicios de VaR==

### VaR X
Este se usa cuando tenemos fat tails, ya que si usamos una normal estariamos subestimado los casos negativos. Para esto podemos usar una distribución t-student que tenga bajos grados de libertadp pero es dificil determinar cuantos. El metodo VaR X propone castigar a las colas anchas para poder cuantificar mejor. (Huisman et all #tesisTech)

## Alternativas VaR
### Condicional VaR (CVaR)
Uno de los problemas a resolver con el VaR, es definir cuan malo es el peor de los casos. Esto es entender que pasa cuando caemos en el umbral negativo de posibilidaes. Si es un VaR Empírico, debo hacer el promedio de los retornos condicional (if) son menores que el VaR (en Excel, averageif( , “. Si es un VaR Covariance y la distribución fuera discreta sería multiplicar cada uno de los retornos por debajo del VaR (peores que el VaR) por su probabilidad de ocurrencia). En el caso de retornos continuos es la integral entre el VaR y – infinito. 

De esta manera podemos capturar el comportamiento en las colas de los retornos de portafolio más allá del p-quantil, es claro que la diversificación reduce el CVaR. 

### VaR Contribution (VaRC)
En este caso queremos medir la contribución de cada instrumento al VaR general del portafolio.

$$
{VaR}_p= w_aVaR_a \rho_{ap}+w_b Var_b\rho_{bp}
$$
En esta ecuación $\rho$ representa el coeficiente de correlación del retorno de cada activo con el portafolio. La contribución de cada activo al VaR del portafolio es: 
$$
\frac{w_a{VaR}_a\rho_{ap}}{VaR_p}
$$
### Marginal VaR
Esta es la derivada parcial del VaR en relación al peso de un activo, nos sirver para entender que sucedece si hay un incremento marginal en el peso de un activo. 

$$
\triangle VaR= \pd{i\rho}{\rho}
$$

$$
Marginal VaR=\triangle VaR /\triangle position
$$
### Incremental VaR
$$
IVaR (a)= VaR(P)- VaR(P-a)
$$
$$
IVaR(a) = VaR(P+a)-VaR(P)
$$
Me dice como se reduce el VaR si remuevo por completo una posición de mi portafolio (y dejo el resto invertido como está) o bien si agrego una posición a mi portafolio.IVaR es usado para determinar los instrumentos (incrementales) que proveeran la mayor cobertura en nuestro portafolio.
