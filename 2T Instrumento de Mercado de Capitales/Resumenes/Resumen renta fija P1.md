 
# Resumen Renta Fija 
El mercado de renta fija supone diferentes contratos entre partes, en los cuales se busca establecer en el tiempo sumas de pagos. Generalmente esto es la formalización de acuerdos de deuda, donde el valor prestado se amortiza al final y los intereses pueden pagarse en el medio o incluirse al final. Como todo pago diferido en el tiempo, las partes pueden acordar distintas tasas de interes que incorporen no solo el el *timevalue of money*, sino tambien los otros riesgos. 

## Conceptos de instrumentación
El capital del bono, que a nivel individual suele ser 1 o 100, se denomina “principal”. Los bonos pueden ser amortizables, pagando ese capital en cuotas, o “bullet”, pagando todo al final del bono.

Los cupones son el “interés” del bono. Es cupon puede ser fijo en una moneda (USD, ARS, EUR, lo que sea), puede ser fijo en términos reales (CER, TIPS) o puede ser variable, determinado a través de una tasa de referencia (Badlar, Libor).

## Mercado de REPO
El mercado de REPO supone transacciones de corto plazo entre tres agentes, generalmente estan entre 1 dia o un mes. Estas operaciones son generalmente llevadas a cabo por traders que buscan estar *long* en un bono un otra posición

En un primer momento un **trader** compra un bono en **mercado** a un precio $P_t$, el bono que compra es aquel que quiere usar para tener una posición larga. Utiliza ese bono para ir a un **repo dealer**, el cual le entrega cash a cambio del bono como colateral. En esta segunda operación el trader recive menos que el valor del bono, esa diferencia se la conoce como **repo haircut**. En este periodo inicial tambien se establecen los plazos durante los que hace el acuerdo y la tasa.

En el periodo T, donde termina el acuerdo de REPO. El trader obtiene el bono que puso como colateral y lo vende en el mercado al precio $P_T$. Al repo dealer le tiene que pagar el dinero que se le entrego más la tasa de repo que se acordo. La gananacia del trader es entonces

$$
Return=\frac{P_T-P_t-(\text{Repo rate } .(P_t-\text{haircut }))}{haircut}
$$
En este caso la persona que arma el trade esta tomando una posición apalancada. Si el preció del bono cayera tendría que pagar y perderia dinero. Pero tambien existe la posibilidad de que aunque el precio no varie, pueda ganar plata por los interes acumulados. 
- Hay *positive carry* si el *accrued interest* > repo rate 
- Hay *negative carry* si el *accrued interest* < repo rate
- La idea de tener carry negativo o positivo la van a ver en muchas situaciones, y básicamente refleja la idea de que el retorno de la posición larga sea mayor (positivo) al costo de la corta (o el préstamo, misma idea). Hecha para aprovechar el carry negativo, esta operación se llama de reverse repo. 
$$
Return=P_t-P_T-(\text{Repo rate } .(P_t)
$$
## Factores de descuento y pricing
- Supuestos basicos
- Desarrollar Z(t;T)  y r(t;T)
- Relación entre y(t;T) y r(t;T)
- Pricing con cupon y relación con no arbitraje. 

A la hora de valuar los activos de renta fija, intentaremos entender cual es el valor descontado de los pagos futuros. En este sentido trataremos de entender cuales son los pagos, como descontarlos al presenten y como interactuan las tasas de descuento. 

En este caso comenzamos introduciendo un monto $Z(t,T)$ que refiere al precio hoy de un activo que recibimos en el futuro. El valor de $Z$ es una función del tiempo, entre hoy $t$ y $t+T$ cuando se paga o el momento de maturity. Ese pago vamos a suponer que esta descontado a una tasa $r(t,T)$ si es en terminos discretos o $y(t,T)$ si hablamos en terminos continuos. 

#### Como descontamos (La relación entre $Z$ y $r$)
Generalmente los pagos de cupon de los bonos son semi-anules, lo que quiere decir que hay dos momentos donde se capitaliza nuestro bono y tenemos pagos.  En esos caos la relación entre $Z(t;T)$ y $r(t;T)$ se da como 

$$
Z(t;T)=\frac{1}{(1+\frac{r(t;T)}{2})^{2T}}
$$
Se divide la tasa nominal anual por dos para significar que es un activo con capitalización semi anual. Ahora la relación tambien existe de manera inversa. 

$$
r(t:T)= n (\frac{1}{Z(t;T)^\frac{1}{nt}}-1)
$$

Estas relaciones son en tiempo discreto y asumimos que los bonos capitalizan para cada T. Sin  embargo,esto no es lo que observamos en la realidad. Yo puedo adquirir un bono en cualquier momento del tiempo, y cuando lo haga 
voy a estar comprando parte de esa capitalización.  Para eso usamos tasas continuas, expresadas como. 
$$
y(t;T)= -\frac{1}{T} ln(Z(t;T)
$$
Existiendo tambien la relación entre la tasa continua y la tasa discreta. 

#### Relación entre $r$ e $y$
Generalmente llamaremos a la tasa $r$ como tasa *spot* para el periodo que abarquemos. Mientras que la tasa $y$ sería la función de yields cupon cero

$$
e^{y(t;T).T} = \frac{1}{(1+\frac{r(t;T)}{n})^{nT}}
$$
#### Bonos con cupon
Hasta ahora las relaciones vistas nos permiten entender como descontar mediante una tasa pagos futuros o como a partir de valores presentes obtener tasas. Esto en el fondo es trabajar con bonos cupon cero, aunque tambien nos ayuda a enfrentarnos a bonos con cupon. 

Podemos entender un bono con cupones como una sumatoria de valores presentes de bonos cupon cero. Es decir hacer un flujo de pagos y traerlos a valor presente a cada uno de ellos usando su tasa *spot* para cada *t*.

$$
P(t,T_n)= \sum{\frac{c/2}{(1+r(t;T_i)/2)}+\frac{100}{(1+r(t,T_n)/2)^2}}
$$

Esta sería la formula para un bono con capitalización semi-anual. Si fuera una capitalización distinta tendría que cambiar el 2 por el n necesario. 

#### Convenciones 
Los precios de los bonos en los mercados internacionales suelen ser mostrados (quoted) “clean” mientras que localmente son “dirty”. Cual es la diferencia?

- Clean Price: quoted sin el interés devengado. El precio que se paga luego incluye el interés, pero el quote es sin. Luego se le suma a la factura separado. Es como mostrar el precio sin IVA, si bien luego se lo factura
- Dirty Price: es el precio que en realidad se paga, e incluye todo el interés devengado (“IVA incluido”)

El *accrued interesr* es el interes devengado desde el ultimo cupon. 

Convenciones de días. Como contamos los días para calcular intereses. Depende del prospecto de emisión, hay varias convenciones 
- **Actual/Actual** (Correcto/Correcto): Solo se cuentan los días calendarios. 
-  **30/360**. Asume que hay 30 días en un mes y 360 en un año. 
- **Actual/360**. Cada mes tiene la cantidad de días correcta, pero se toma 360 en un año.


### Discount Yield y BEY (mirar CAP 14 libro)
El discount yield y el bond equivalen yield son dos convenciones de mercado que ayudan a comunicarse. En este caso es como pensamos y expresamos la tasa libre de riesgo

$$
d = \frac{100-P}{100}* \frac{360}{n}
$$
Donde $n$ es la cantidad de dias hasta la madurez del bono, vale la pena notar que esto esta calculado como 30/360. En este caso $d$ representa nuesto discount yield para la letra y como nuestra libre riesgo.

Si quisieramos ser más exactos deberiamos usar la *Bond Equivalent Yield* ($BEY$), que se calcula sobre 365 días 
$$
d = \frac{100-P}{100}* \frac{360}{n}
$$


### Forward rates
La tasa forward representa la tasa implicita, en función de las tasas spot, para una inversión hecha entre dos periodos futuros con una letra como vehiculo. Por ejemplo como sería la tasa de una letra entre $t+T_1$ y $t+T_2$. 

- Por notación si usamos una tasa de capitalización semi-anual lo denotamos como $r_f (t,T_1,T_2)$
- Si utilizamos capitalización continua $f_f (t,T_1,T_2)$
- Ejemplo no arbitraje en pagina 39 [[Renta Fija parte 1.pdf]]. Pero fundamentalmente si entrara en $t$ a un contrato a un año y a su vez me comprometo a utilzar esa ganancia para entrar a un contrato de un año en en $t+1$, la ganancia no puede ser superior a la de $t+2$. Igualando llegamos a la formula de la tasa *forward*.

$$
{(1+\frac{r_f (t,T_1,T_2)}{2})}^{2(T_2-T_1)}= \frac{Z(t,T_1)}{Z(t,T_2)}
$$

En este caso es facil sacar la tasa  *forward* cuando uno tiene las tasas spot o cupon cero para cada periodo. Uno tambien podría hacerlo si tuviera una serie de estrumentos iguales, y entre instrumentos no es correcto. 

Tambien podemos necesitar las tasas *forward* bajo capitalización continua, lo que nos puede llevar a plantear:

$$
f(t,T_1, T_2) =\frac{ln(Z(t, T_1))- ln (Z(t,T_2))}{T_2-T_1}
$$

$$
f(t,T_1, T_2) = \frac{y(t, T_2)T_2- y(t,T_1)T_1}{T_2-T_1}
$$

Esto ultimo tambien puede expresarse como la tasa forward instantanea, donde multiplicamos las función continua de entre $t$ y $T_1$ 

$$
f(t,T_1, T_2) = y(t,T_1)+ T_2 *   \frac{y(t, T_2)- y(t,T_1)}{T_2-T_1}
$$
La función de arriba puede ser derivada, en $T+1$ para entender el signo de la pendiente y por lo tanto saber si la tasa *forward* esta por encima de las *spot*. 

==LEER y ENTENDER==


### YTM Uso y confusiones (Total carry)
La $YTM$ o $TIR$, en español, reprensenta la tasa a la que debería descontarse un bono para que su precio sea el valor presente de sus pagos futuros. 

$$
P(t,T_n)= \sum^n_{i=1}{\frac{c/2}{{(1+Y/2)}^{2T_i}}+\frac{100}{(1+Y/2)^{2T_n}}}
$$

- La $YTM$ de un bono esta relacionado directamente con su precio y es otra manera de expresarlo. Aunque hablemos de bonos con la misma maturity, su $YTM$ esta condicionada por su estructura de cupones y puede ser totalmente distintos. 

 Hay varias razones por las cuales la $YTM$ es una mala medida de retornos:
 - Asume que todos los cupones puede reinvertirse a la tasa de la $YTM$ a lo largo de la vida del bono, lo cual no es así. Esto lleva a que se asuma que la curva de rendimientos es plana y que no cambia en el tiempo. Ambos son elementos que no se observan en la realidad. 

El total carry puede pensarse como : A) pure carry (ytm) + B) roll-down (la suba de precio por moverse en la curva). ==Revisar==





### Duration y variantes

En terminos basicos la *Duration* de un activo se define como la sensibilidad del mismo a variaciones en el precio debido aun  cambio **pequeño y uniforme** de la curva de rendimientos. Esto se puede hacer usando la $YTM$ o la formula capitalización continua 

>**Intuición**: La Duration puede pensarse como una elasticidad entre el precio y la tasa. 

Nosotros queremos ver la varía el precio cuando nos movemos de $y_0(t, T)$ a $y_1(t, T) = y_0(t, T) + dy$. En este caso tenemos: 

$$
D_p = -\frac{1}{P}\frac{dP}{dY}
$$
En el caso de un bono cupon cero, su duration es igual al tiempo a maduración. Esta demostración esta en la Slide 48, [[Renta Fija parte 1.pdf]]. Pero como definimos el precio como el valor presente, podemos reescribir esto como: 

$$
\begin{aligned}
D_p = -\frac{1}{Z(t,T)}\frac{dP}{dZ(t,T)}
\end{aligned}
$$
Antes pasar a bonos con cupones, es necesario entender como pensar la duration de un portafolio. Esto es porque podemos pensar a un bono y sus cupones, como un portafolio de bonos cupon cero. Pero antes de ver eso, podemos volver arriba e intentar interpretar la duration y como se usaría. 

> **Ejemplo:** Si tenemos un portafolio de 100 dolares en bonos a plazo T y una duration de 5, podemos plantear que sudede si la tasa aumenta 1 bp (0,01%)
>  $$
-5 * 0,01/100* $100 = -0,05
 $$
 > Esto es una caida de 0,05% en el portafolio portafolio


#### Duration de un portafolio
En el caso de un portafolio, la duration del mismo es el promedio ponderado de la duration de los activos. Esto esta demostrado en la slide 49 de  [[Renta Fija parte 1.pdf]]. Para calcularlo podemos pensar la sifuente forma, pensemos a $\Pi$ como el valor del portafolio y $N$ a las cantidades de los activos:

$$ \begin{aligned} 
\Pi = N_1 P_1 + N_2P_2
\\
D_\Pi = -\frac{1}{\Pi}\frac{d\Pi}{dY}
\end{aligned} $$
Llegamos a: 
$$
\begin{aligned}
D_\Pi= w_1D_1+w_2D_2
\\\\ \text{Con los pesos definidos como}
\\
\\ w_1 =\frac{N_iP_i}{\Pi}
\end {aligned}
$$
#### Bonos con cupon
Ahora podemos pensar como calcular la duration de nuestro bonos con cupones. Primero tenemos que entender como pensar el factor de precio, el cual vamos a plantear como: 

$$
P(t,T) = \sum_{i=1}^n{c(T_i)Z(t,T)}
$$
En este caso $c(T_i) = c/2$ para todos los $i<n$, mientras que en el ultimo periodo es igual a $c_(T_n)=c/2+100$ por el pago de principal. Con eso podemos construir

$$
\begin {aligned}
w_i ==\frac{c(T_i Z(t,T_i))}{P(t,T)}
\\
\\
D = \frac{\sum_{i=1}^n{c(T_i). Z(t,T_1). T_i}}{\sum_{i=1}^n{c(T_i). Z(t,T_1)}}

\end {aligned}
$$

==Resultado de que parece una vida promedio==

### Modified Duration
Uno de los problemas que podemos encontrar es que no tenemos la curva entera de tasas spot, para todos los cupones o bonos. Aunque esta se puede extraer o inferir, como veremos despues, se puede hace un cambio por la $YTM$. Si llamamos a la $YMT$ como $Y$, podemos plantear. 

$$
\begin {aligned}
MD = \frac{1}{(1+Y/2)} \sum_{i+1}^n{w_j.T_j}
\\
w_j=\frac{1}{P_c(0,T)}(\frac{(c/2).100}{(1+Y/2)^{2T_j}})
\\
w_n=\frac{1}{P_c(0,T)}(\frac{(c/2).100}{(1+Y/2)^{2T_n}})

\end{aligned}
$$


#### Macaulay Duration 

La Macaulay Duration elimina el factor de descuento de la modified duration y se concentra solo en los pesos, tal que:
$$
\begin {aligned}
D^{Mc} =\sum_{i+1}^n{w_j.T_j}
\\
w_j=\frac{1}{P_c(0,T)}(\frac{(c/2).100}{(1+Y/2)^{2T_j}})
\\
w_n=\frac{1}{P_c(0,T)}(\frac{(c/2).100}{(1+Y/2)^{2T_n}})

\end{aligned}
$$
#### PVBP 
Sobre todo esto se construyen algunos de los terminos fundamentales de la industria, entre ellos esta ***Price Value of a Basis Point***. 

$$
PVBP = -\frac{dP}{dY} = MD.P
$$
Básicamente captura el cambio en el precio por 1 cada punto básico de tasa, por lo cual nomalmente la llamamos DV01 (dollar value of 0.01)

### ==Trade de Tasas==


## ==Covenxidad== 
En varios casos, el uso de la duratio es una medida pobre para entender los cambios de precio debido a cambios en la tasa. Esto es especialmente cierto cuando las diferencias de Y son muy grandes. **La Convexidad no es un cambio en el tiempo de duration**, sino un termino más que ajusta la aproximación. 

$$
\begin{aligned}
C = \frac{1 d^2P}{Pdy^2}
\\
\frac{dP}{P}=-D.dy+1/2.C.dy^2
\end{aligned}
$$

## Extraer la curva de descuentos
Varias veces es no se puede extrar la curva de descuento cupon cero en el mercado, esto sucede debido a que no existen esos instumentos. Sin embargo, existen maneras de extrae 
### Bootstrap (Fama-Bliss)
==Ejemplo==: Slide 67 [[Renta Fija parte 1.pdf]]
En el metodo de Fama-Bliss buscamos extrar la curva a partir de instrumentos que ya existen en el mercado. 

$$
Z(t,T_i)=\frac{P^i(t,T_i)-c^i/2x\sum_{j=1}^{i-1}{Z(t,T_j)}}{1+c^1/2}
$$
 A partir de extraer el valor presente, podemos luego buscar el $r(t,T_i)$ correspondiente. 


 
### Curve Fitting 
Uno de los problemas con Bootstrapping es que no siempre tenemos datos para todos los vencimientos, por lo que se vuelve complicado usar el metodo.  El metodo de curve fitting busca asumir una forma funcional para los bonos y con ciertos parametros intentar minimizar la distancia entre los precios teoricos y de mercado. 

Las formas funcionales tienden a ser sugeridas de la literatura y luego se minimiza los parametros de la misma con la intención de lograr el menor error cuadratico. 

## Estructura de tasas
En este caso la estructura de riesgo hace referencia a los distintos niveles de tasa de los distintos instrumentos. Esta curva de tasa nos da las expectativas, ajustadas por riesgo, de las tasas hacía adelante. Observando las estructura de tasas se puede intentar inferir la expectativa agregada de los agentes. 

Las formas más comunes que puede tomar la curva de rendimientos es: 
- Pendiente positiva  (upward sloping): Bonos con mayor duration tienen mayor TIR
- Plana:  Todos los bonos tienen similares rendimientos, independientemente de su duración. 
- Pendiente negativa: Bonos con menor duration tienen mayor rendimeinto que bonos de mayor duration.
- Jorobada: Los Bonos de duration medias, tienen mayor rendimiento que los cortos y los largos.

### Analisis de estructura de tasas sin riesgo. 


# (NEXT) Otras cosas

## Estructuras particulares de bonos 
- Bonos Tasa flotante
- Bonos indexados


## Pol Mon y tasas
## Componentes implicitos 
 - Break evens 
- Riesgo de Default
- 