# Resumen Unidad de Asset Pricing 
## Retornos
### Diferencia entre Retornos discretos y continuos
### Distribución de los retornos 
### Log retornos 
## Sharpe ratio 
El ratio de Sharpe es una manera con la cual los inversores intentan capturar la relación entre riesgo y retorno que hay en sus portafolios. 

$$
\begin {aligned}
\text{Sharpe Ratio} = \frac{\text{Prima de Riesgo}}{\text{Desv Est de Retorno Excedente}}
\\
\\
\text{Prima de riesgo}= \text{Retorno esperado}-\text{Tasa Libre de riesgo}
\\
\\
\text{Retorno excedene}= \text{Retorno observado}-\text{Tasa libre de riesgo}
\end {aligned}
$$

## PCA
Cuando miramos un  portafolio, el mismo parece tener distintos elementos los cuales influyen sus retornos. Principal component analysis (PCA) es el método estadistico mas comúnmente usado justamente para reducir la dimensión de las variables a analizar.

## Valuación de Activos
El riesgo idiosincrático no genera correccion por riesgo. 

En Finanzas nos importan fundamentalmente los riesgos sistémicos, y NO los idiosincráticos. Esto es así por que el riesgo idiosincrático se puede diluir al diversificar. Pero el sistémico, NO. 

Que es el riesgo sistémico? Justamente es un riesgo que al diversificar no se puede eliminar. En nuestro ejemplo de formula de valuación, lo que implica eso es que si un activo NO tiene riesgo sistémico, pero SI idiosincrático, podemos descontar su flujo esperado a la tasa libre de riesgo. Fijense que eso me dice que en un mercado, un activo que paga 100 seguro en un año tiene que valer lo mismo que uno que paga 200 con probabilidad 50% y 0 con probabilidad 50%, asumiendo que esos escenarios no se correlacionan con factores sistémicos (como el retorno de mercado o el consumo).