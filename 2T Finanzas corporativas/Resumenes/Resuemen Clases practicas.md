# Resumen practico Finanzas Corporativas 
Este resumen se concentra en los elementos practicos vistos en las clases practicas de finanzas corpotarivas, e intenta resumir algunos de los conceptos que van a los ejercicios. 

# Clase 1 - Basico
El primer modulo practico funciona como un repaso de los visto en materias previas. Pero vale la pena hacer un paralelismo entre algunos conceptos contables y los conceptos de finanazas corporativas.

Como primer elemento esta la visión sobre como se compone el estado de situación patrimonial. La ecuación tradicional de contabilidad se transforma en :

$$
\begin {aligned}

Activo = Pasivo + PN 

\\

\text{ Valor Compañia} = Deuda + Equity 

\end{aligned}

$$
En este caso cambiamos como pensamos la valuación del activos y pensamos los retornos potenciales de distintos componentes de activo. En este sentido valuamos los activos en sus valores potenciales, mientras que antes los valuabasos en vase a su valor de reposición o su costo de producción. Elemplo Picasso Slide 5 [[Práctica 1 MFin.pdf]]

#### Estructura de Capital
**Activo**

- Cash: Posición de caja 
- Inverciones y otros activos: Inversiones de equity en otras compañias. Tambien puese ser inmuebles vendidos que **NO** afecten las operaciones 
- *Company Value*: Es el valor *core* de la compañia y resume a los activos que estan relacionados con el negocio de la compañia. Esta parte es compleja de valorizar porque requiere varias supocisiones por parte del analista. Dentro de esto esta los varios metodos de valuación como FFC, descuento con WACC y VAN. 

#### WACC
Cuando construimos un flujo de fondos para una empresa, nos vemos forzados a encontrar una manera de traer esos flujos futuros al presente. Para esto utilizamos la tasa **WACC** = Weighted Average Cost of Capital. En este caso la tasa econtrada parte de entender la estructura de la empresa y entender el costo de capital dependiendo de que necesite. Esto requiere entender el costo del equity de la empres y el costo de la deuda. Entonces, aparte de la proporción de equity y de deuda, debemos definir los costos de la misma ($Ke$ y $K_d$)

$$
\begin {aligned}
WACC = K_e * \frac{E}{D+E}+ K_d* \frac{E}{D+E} * (1-T)    
\\
\\
K_e= R_f+Bl * (R_m-R_f)+R_p
\\\\
Bl= Bu * [1+\frac{D}{E}* (1-T)] 
\end{aligned}
$$
En este caso $E$ y $D$ son las cantidades de equity y deuda que una empresa tiene, mientras que $T$ representa el procentaje de impuestos que la empresa debe pagar. $(1-T)$ Representa el escudo fiscal, que es la ventaja impositiva que se tiene de tomar deuda, la cual se puede descargar de los impuestos. El costo de la deuda $K_d$ puede entenderse como la tasa de interes que le cobra el mercado a la firma, la cual puede estimarse mirando empresas comprables o recibiendo ofertas de bancos. 

Dentro del costo del equity tenemos a la tasa libre de riesgo $R_f$, al cual se le suma el *beta* de la acción multiplicado por el exceso de retorno del mercado.

#### EBITDA
#EBITDA = (*Earnings before interest, taxes, depreciation and amortization*). Quiero tener un resultado operativo de cajas, omite la variación/aplicación del capital de trabajo. Quiero tratar de acercarme al cash-flow de la empresa, pero los datos salen del estado de resultado. Los valores del estado de resultado no tienen porque estar en el bolsillo. 

Una critica al EBITDA es la no inclusión del flujo de ingresos necesarios para financiar las necesidades de trabajo. Tal vez tiene EBITDA de 10, pero necesito tanto capital de trabajo que mi flujo de dinero operativo es cero. El capital de trabajo es: Cuentas por cobrar, inventario y cuentas por pagar. La cuenta por cobrar (Activo) necesita financiarse con algun pasivo, muchos activos necestian una contrativo. El EBITDA deja de lados muchos conceptos a cargo de la subjetividad de quien lo arma, esto inclluye disitintos tipos de interes. 

#### Metodo *Up-Bottom*
- Ventas (+)
- Costos (-)*menos*
- Gasto de Administración (-) *menos*
- Gasto de comercialización (-) *más*
- Amotizaciones (Las sumo para anularlas de los elementos costos y gastos)
---
EBITDA

#### Metodo *Bottom-Up*
Tiene que dar igual en los dos metodos y se hace al reves

- Resultado final (+)
- Impuesto a las Ganancias (+)
- Ingresos/Egresos extraordinarios (-/+)
- Resultados inversiones Sociedades controladas (+)
- Gastos Financiero (+)
- Amotizaciones (+)
---
EBITDA

# Clase 2
Una de las precupaciones principales de los inversores, sobre todo en *Venture Capital*, es que entre rondas de inversores sus acciones se vean diluidas. Esto sería porque entre rondas el valor de la compañia cae y  por lo tanto otro inversor podría diluir al inversor original.

Existen para esto, dos metodos: ***Full ratchet*** y ***Weighted Average***.

#### Full Ratchet 
En el metodo Full ratchet el inversor se proteje completamente de la dilución con el uso de acciones preferidas. ESto le permite al inversor original obtener acciones en la segunda ronda, como si fueran al precio de la primera ropnda. 

En terminos practicos los inversores de la primera ronda obtinen acciones preferidas, las cuales pueden transformar en acciones ordinarias en futuras rondas. Luego de la primera ronda el precio de conversión es igual al precio que se pago las acciones preferidas, pero se ajusta luego cuando tenemos una nueva ronda 

> *En un contrarto puede aparecer de la siguiente manera*:  In the event that the Company issues additional securities in the future at a purchase price less than the current Series A Preferred conversion price, such conversion price shall be adjusted in accordance with the following formula: 
>  
> Full-ratchet – the conversion price will be reduced to the price at which the new shares are issued.


El ejemplo practico esta en [[FULL RATCHET ANTI-DILUTION PROTECTION.pdf]], pero a continuación algunos elementos fundamentale. 

- Los tratos se negocian al rededor de puntos porcentuales y se estructuran con acciones. 
- En una ronda de capital con inversores previos y Full Ratched, si las cosas van mal es el fundador el que pierde. 
- Esto es algo que los inversores demandan mucho, pero que puede tener un mal menor. 

#### Weighted Average
Al igual que con *Full Ratched* en este caso el inversor buscar cubrirse de una posible dilución. Pero en esta opción se es menos agresivo, pero al igual que en el ejemplo anterior se usa acciones preferidas para protejerse. En un contraro la protección *weighted average* podría verse de la siguente manera:

>In the event that the Company issues additional securities at a purchase price less than the current Series A Preferred conversion price, such conversion price shall be adjusted in accordance with the following formula: 
>
>$CP_2$ = $CP_1$ * (A+B) / (A+C), where: 
>
>$CP_2$ = New Series A Conversion Price 
>
>$CP_1$ = Series A Conversion Price in effect immediately prior to new issue 
>
>A = Number of shares of Common Stock deemed to be outstanding immediately prior to new issue (includes all shares of outstanding common stock, all shares of outstanding preferred stock on an asconverted basis, and all outstanding options on an as-exercised basis; and does not include any convertible securities converting into this round of financing) 
>
>B = Aggregate consideration received by the Corporation with respect to the new issue divided by $CP_1$ 
>
>C = Number of shares of stock issued in the subject transaction


# Clase 3
La tercera clase se centra en empresas publicas, IPO y metodos de emisión. 

Existen ventajas y desventajas de ser una empresa publica: 

**Ventaja**:
- Usar capital como Moneda de Compra.
- Mecanismo de Retención de Empleados.
- Fuente Adicional de Financiamiento.
- Valuation Benchmark.
- Mecanismo de monetización para el accionista.
- Mayor exposición a fondos e inversores.

**Desventajas**
- Mayores costos administrativos, contables y legales.
- Pérdida de control.
- Mayor formalización del proceso decisorio debido a responsabilidad fiduciaria frente a terceros accionistas.
- Mayor escrutinio de las decisiones por parte de analistas de Research.
- Apertura de los estados contables y otra información crítica.
- Exigencia de resultados a corto plazo por parte de la comunidad inversora. 

#### Tipos de oferta 

**Oferta primaria**
En una oferta primaria, la empresa crea acciones con el fin de ofrecerlas en el mercado. Esto quiere decir que no solo hay más acciones sino que aumenta la relación entre los demas componentes y el equity 

**Oferta secundaria** 
En este caso los accionistas lanzan al mercado acciones ya existentes, de esta manera se le puede dar salida a inversores de rondas inciales y estos pueden monetizar. Por otro lado, la relación entre capital y otros elementos se mantiene igual. 

**Oferta combinada**
Es cuando se realiza tanto una oferta primaria como una ofeta combinada, de esta manera se crean nuevas acciones y se da salida a accionistas anteriores. En estos casos el precio de lanzamiento debe ser igual en los dos tramos, no se hace diferencia en las acciones. 

#### IPO Discount 
Cuando salimos al mercado necesitamos compenzar a los inversores por la incertidumbre que puede tener una nueva compañia, por lo tanto se tiende a presentar un descuento sobre las acciones. 

# Clase 4 
En varios casos, las firmas se ven obligadas a reestructurar sus pasivos. Esto puede suceder por varios motivos: 

- La estructura de pagos no se ajusta al flujo de caja del negocio. 
- Las restricciones de los convenat son muy estrictos. 
- La empresa puede querer reestructurar un papel que se encuentra con poca liquidez, con el fin de hacer otra emisión. 
- Obtener una ganancia de capital si la emisión se negocia a un precio muy bajo. 
- Para frenar el avance de acreedores hostiles. 

La empresa puede negociar una serie de movimientos con sus acreedores, o puede intentar reesctructurar la deuda con un nuevo pasivo (deuda o equity). 

#### Tender offer
Una tender offer es cuando la empresa intenta reestructurar un pasivo mendiante la emisión de otro. Esto puede ser bien a un precio determindo por la empresa o aun precio que determina el mercado. 

En el caso de que sea el mercado quien determine el precio, la empresa tiene varias opciones para intentar encontrar el precio. 

- ***Pure Dutch Auction***:  
- ***Modified Dutch Auction***: Se determina un precio unico de las ofertas a partir de las recabadas por el mercado. Ordenamos las ofertas de orden creciente en precio/decreciente en yield. A su vez tambien marcamos el orden por si tiene que haber prioridad, el metodo de corte se hace de todas maneras primero por precio. 


#### Opciones
- **Cash Tender Offer / Pago Upfront** =  Se realiza un pago en efectivo, usualmente aportado por el Accionista, al momento T=0 de la reestructuración. Usualmente reestructura la Deuda Elegible a un bajo valor nominal.  
- **Deuda Mediano Plazo**= Se reemplaza la deuda vieja, por nueva deuda a un plazo medio en el tiempo (ej. 5 años). Generalmente se modifican los términos económicos (plazo y tasa) afectando el valor nominal (o “face value”) del crédito y el valor de recupero.
- **Deuda Largo Plazo** = Se reemplaza deuda vieja, por nueva deuda a un plazo largo en el tiempo (ej. 7 o 10 años). Generalmente no se modifican términos económicos (plazo y tasa), no afectando el valor nominal, aunque si se afecta el valor de recupero (valor en el tiempo del dinero).
