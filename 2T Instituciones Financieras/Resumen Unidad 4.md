# Unidad 4
## El efecto de la tasa de interes en los prestamos 
Existen otros intentos de explicar la crisis financiera del 2008, la gran recesión, en las cuales se intenta buscar si causas macro pudieron influir en la toma de riesgos de los bancos. 

Una de las teorias es la conección entre las bajas tasas de interes y los incentivos al riesgo de los agentes financieros. Epocas de bajas tasas de interes pueden haber conducido a que los bancos esten más incentivados a tomar riesgos. Esto significa dar más prestamos más altos a personas con menos probabilidad de repago.  Para esto se presenta un paper empirico

### Credito y politica monetaria en españa
#### Motivación y metodo 
España es un país donde los bancos son los jugadores dominantes del mercado de financiero y del mecado de prestamos. Ademas podemos considerar la decisión de tasa como exogena, ya que esta se decide en conjunto con los otros paises de la union.

>A low short-term interest rate makes riskless assets less attractive, and may lead to a search for yield by financial intermediaries with short-term horizons 

Para esto se tomo data de prestamos bancarios a firmas  desde 2002 a 2008. A su vez se separo a los bancos en bancos con altos ratios de capital y a otros de bajos ratios de capital. A partir de esto se busco capturar dos efectos a partir de una caida de la tasa: 1) Cuantos prestamos se otorgaban y 2) las caracteristicas del prestamos otorgado. 

#### Resultados 
De una caida del 1% en la tasa de pases (*overnight rate*) estiman: 
- En promedio un banco de baja capitalización es 8% más probable que entregue un prestamo bancario. 
- El monto comprometido en el prestamos es un 18% más alto 
- Las posibilidades de default incrementan un 5% y las posibilidades de que sea colateralizado cae un 7%.

Las implicacias de politca de estos elementos son importantes para los banqueros centrales y otros policy makers. Esto es porque muestra como la politica economica induce cambios en la composición crediticia de los bancos. Sobre todo porque esto es más fuerte en bancos de baja capitalización que estan más expuestos a los shocks y ven un aumento en la posibilidad de default de su cartera.  


## Riesgo de tasa de interes
Como vimos antes las instituciones financieras estan expuestas a las subas de tasa de interes. 

### Repricing Model
El modelo de repricing intenta evaluar el efecto de los cambios de la tasa de interes en los activos y pasivos de un banco. Para esto intentamos encontrar el GAP.

$$
\text{GAP} = \text{Rate Sensitive Assets (RSA)} - \text{Rate Sensitive Libilities(RSL)}
$$
*Rate sensitive* se refiere a un activo que es sensible a variaciones de la tasa de interes en un periodo determinado. Generalmente se calcula el *GAP* para un periodo especifico entre 6 meses y 3 años. 

A partir del *GAP* podemos tener tambien la variación neta de ingreso, debenida de un cambio en la tasa de interes. 

$$
\triangle NII= GAP*\triangle I=(RSA-RSL)*\triangle I
$$

|Caso|GAP|$\triangle I$ |$\triangle NII$|
|---|---|---|---|
|1|+|$\triangle \downarrow$|$\downarrow$|
|2|+|$\triangle \uparrow$|$\uparrow$|
|3|-|$\triangle \downarrow$|$\downarrow$|
|4|-|$\triangle \uparrow$|$\uparrow$|

A partir de estos casos podemos señalar dos escenarios negativos para las entidades financieras. Si las madurez de los activos es muy distinta nos exponemos a que los cambios de tasa afecten la valuación de activos o pasivos. De esto aparecen dos riesgos: El **riesgo de refinanciación** y el **riesgo de reinversión**. 

- **Riesgo de refinanciación**: Si el *GAP* es negativo y tenemos una suba de tasas podemos tener un caso donde la refinanciación de los pasivos sea más grande que el ingreso de activos ya establecidos
- **Riesgo de reinversión**: El riesgo de reinversión es cuando una caida en las tasas de interes afecta negativamente los *RSA* y de esta manera cae el *NII*

Algunas de las devilidades de este modelo es que no tiene en cuenta los efectos que tienen las tasas en otros activos, que pueden cambiar de valuación frente a cambios en la tasa. **Tambien se concentra en *Book Value* en vez de en *Market Value***

### The Maturity/duration Model


## Shocks de credito


